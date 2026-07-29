Add a research paper to this repo's learning index and chronological list.

The user provides a paper URL (e.g. an arXiv link) as input: $ARGUMENTS

If no URL is provided, ask for one.

## Steps

### 1. Parse the paper URL
Extract the paper URL from the input. Support at least:
- arXiv abstract pages: `https://arxiv.org/abs/XXXX.XXXXX`
- arXiv PDF links (normalize to the abstract URL — never use versioned `...vN.pdf` links)
- Other direct links (conference, author page) if needed

### 2. Fetch paper metadata
Use the URL to obtain:
- **Title**
- **Authors** (short form for citation, e.g. "FirstAuthor et al.")
- **Publication date** (for arXiv, the submission month is authoritative: ID `YYMM.NNNNN` → `20YY.MM`)
- **Abstract** (to decide placement)

### 3. Discover learning areas and choose placement
**Do not hardcode topic names.** Instead:

- List all `.md` files in the `learning/` directory (exclude `glossary.md`).
- For each topic file, read the **Overview** (and the section headers) to understand what that area covers.
- Using the paper's title and abstract, choose the **single best-fit topic file** and the **best-fit section** within it.
- Present to the user in one short block:
  - **Paper:** [title]
  - **Proposed area:** `learning/<filename>.md`
  - **Proposed section:** [section name from that file]
  - **Date for index:** YYYY.MM

Ask the user to confirm or request a different area/section before making any edits.

### 4. Add to the topic file
Once confirmed, append a new entry with the next number in the section:

```markdown
N. [Full Paper Title](https://arxiv.org/abs/XXXX.XXXXX) (Authors et al., YYYY)
   - *Why*: One or two concise sentences on why the paper matters and what the reader learns.
```

Conventions (enforced by the validator — see CONTRIBUTING.md "Entry Format Reference"):
- Research papers carry **no emoji**; 📄 is reserved for policy documents (policy area only)
- Paywalled papers get a `🔒 ` prefix before the link
- Continuation bullets align under the title (3 spaces for 1-digit entry numbers, 4 for 2-digit)
- Prefer the arXiv abstract URL; follow the existing "Why" style (specific, 1–2 sentences)

### 5. Add to chronological index
Edit `by-date.md`:

- Ensure `## YYYY` and `### YYYY.MM` headings exist for the paper's date (reverse chronological, newest first).
- Insert a new bullet at the top of that month's list, **including the area back-link**:

```markdown
- [Full Paper Title](https://arxiv.org/abs/XXXX.XXXXX) (Authors et al., YYYY) — [Area](learning/<area>.md)
```

- Policy documents also get a `📄 ` prefix; paywalled papers get `🔒 ` and the ` - *Paywalled*` suffix.

### 6. Validate
Run the repo validator — it updates every derived artifact (README badges, per-area table counts, totals, the generated Coverage-by-Topic block, and the by-date footer stats + paywalled list). **Never hand-edit counts.**

```bash
python3 scripts/validate.py --fix
python3 scripts/validate.py   # must report 0 errors before committing
```

Fix any remaining ERROR lines (each ends with a fix hint) before proceeding.

### 7. Branch, commit, PR, and merge
Do not commit directly to `main`. Instead:

1. Create a new branch from `main` named `add-<short-kebab-title>` (e.g. `add-agents-of-chaos`).
2. Commit the changed files (typically the topic file, `by-date.md`, and `README.md` from the count updates) with a clear message, e.g. `Add paper: Title (YYYY)`. The pre-commit hook re-runs the validator; a blocked commit means step 6 was skipped.
3. Push the branch and create a pull request into `main` using `gh pr create`.
4. Merge the PR using `gh pr merge --merge --delete-branch`.
5. Switch back to `main`, pull to sync, and delete the local branch if it remains.
