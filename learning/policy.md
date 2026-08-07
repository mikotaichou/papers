# Policy, Safety & Societal Impact

[← Back to Learning Path](../learning-path.md) | [← Prev: Human-AI Interaction](human-ai-interaction.md) | [📖 Glossary](glossary.md)

**Overview**: Technical capabilities alone don't determine AI's impact on society—policy, governance, and ethical considerations are equally critical. This area steps back to examine the bigger picture: how should AI systems be regulated, what are the existential and near-term risks, how do we ensure equitable access and prevent misuse, and what frameworks exist for responsible AI development? Whether you're building AI systems, advising organizations, or simply want to be an informed citizen, understanding these policy and safety considerations is essential as AI becomes increasingly central to society.

---

## Financial Services & Model Risk Management
**Goal**: Understand regulatory frameworks for AI in financial services

**Why this matters**: Financial institutions were among the first to systematically regulate AI/ML models. The frameworks developed here—particularly around model validation, governance, and risk management—have influenced AI regulation across industries.

1. 📄 [OCC 2011-12: Supervisory Guidance on Model Risk Management](https://web.archive.org/web/20240616095814/https://www.occ.gov/news-issuances/bulletins/2011/bulletin-2011-12a.pdf) (Office of the Comptroller of the Currency, 2011)
   - *Why*: **Foundational regulatory guidance** - establishes the three lines of defense for model risk management; defines what constitutes a "model" and requirements for validation
   - *Key concepts*: Model development, implementation, use; ongoing monitoring and validation; model inventory and governance
   - *Relevance*: Still the primary reference for ML model governance in banking; applicable beyond finance
   - *Note*: OCC and Federal Reserve removed these pages from their live sites; archived copy linked. The FDIC's [adoption notice](https://www.fdic.gov/news/inactive-financial-institution-letters/2017/adoption-supervisory-guidance-model-risk-management) remains live and covers the same joint guidance

2. 📄 [SR 11-7: Guidance on Model Risk Management](https://web.archive.org/web/20250103073254/https://www.federalreserve.gov/supervisionreg/srletters/sr1107.htm) (Federal Reserve, 2011)
   - *Why*: Federal Reserve's companion guidance to OCC 2011-12; emphasizes board and senior management oversight
   - *Key addition*: Focuses on governance structure and accountability frameworks
   - *Note*: Identical substantive content to OCC 2011-12 but targets bank holding companies; archived copy linked

3. 📄 [Model Risk Management Handbook](https://web.archive.org/web/20241220200407/https://occ.gov/publications-and-resources/publications/comptrollers-handbook/files/model-risk-management/index-model-risk-management.html) (OCC, Updated 2021)
   - *Why*: Comprehensive implementation guide; covers AI/ML-specific considerations including explainability, data quality, and bias
   - *Practical value*: Real-world procedures for model validation, documentation standards, and audit practices
   - *Updates*: 2021 version explicitly addresses machine learning models and alternative data

4. 📄 [Principles for the Sound Management of Operational Risk](https://www.bis.org/publ/bcbs195.pdf) (Basel Committee on Banking Supervision, 2011)
   - *Why*: International framework for operational risk including model risk
   - *Global perspective*: Harmonizes regulatory expectations across jurisdictions

---

## Data Protection & Privacy Law
**Goal**: Navigate privacy regulations affecting AI systems

**Why this matters**: AI systems are data-hungry, but data collection and use are heavily regulated. Understanding GDPR, CCPA, and related frameworks is essential for legal AI deployment, especially for systems processing personal data.

1. 📄 [General Data Protection Regulation (GDPR)](https://gdpr-info.eu/) (EU, 2018)
   - *Why*: **The global gold standard** for data protection; extraterritorial application affects most AI systems serving EU users
   - *Key AI provisions*: 
     - Article 22: Right to explanation for automated decisions
     - Article 35: Data Protection Impact Assessments for high-risk processing
     - Data minimization and purpose limitation principles
   - *Penalties*: Up to €20M or 4% of global revenue
   - *Note*: [Official text](https://eur-lex.europa.eu/eli/reg/2016/679/oj) | [Practical guide](https://gdpr.eu/)

2. 📄 [California Consumer Privacy Act (CCPA) / California Privacy Rights Act (CPRA)](https://oag.ca.gov/privacy/ccpa) (California, 2020/2023)
   - *Why*: Strongest US state privacy law; CPRA adds specific AI/automated decision-making provisions
   - *AI-specific*: Rights regarding automated decision-making; risk assessments for certain AI systems
   - *Influence*: Model for other US state privacy laws

3. 📄 [AI and Data Protection Convention (Modernized Convention 108+)](https://www.coe.int/en/web/data-protection/convention108-and-protocol) (Council of Europe, 2018)
   - *Why*: First binding international treaty on data protection; addresses AI explicitly
   - *Global scope*: Open to non-European countries

4. 📄 [Framework Convention on Artificial Intelligence and Human Rights, Democracy and the Rule of Law (CETS No. 225)](https://www.coe.int/en/web/artificial-intelligence/the-framework-convention-on-artificial-intelligence) (Council of Europe, 2024)
   - *Why*: **First binding international treaty on AI itself** - extends the Convention 108+ model from data protection to the full AI lifecycle; obliges parties to ensure AI activities are consistent with human rights, democracy and the rule of law
   - *Scope*: Open to non-member states; signatories include the UK, France, Norway and the EU
   - *Status*: Opened for signature 5 September 2024; entered into force 1 November 2025; ratified by the EU on 15 May 2026
   - *Contrast*: Sets state-level obligations rather than product requirements, so it complements rather than duplicates the EU AI Act

---

## AI-Specific Legislation & Executive Action
**Goal**: Understand emerging AI-specific regulatory frameworks

**Why this matters**: Unlike sector-specific rules, these frameworks regulate AI systems directly based on risk, use case, or capability level. They represent the future of AI governance.

> **Dates move.** Effective dates in this section have shifted repeatedly — the EU deferred its high-risk deadlines, Colorado repealed a law before it took effect, and New York rewrote one after signing. Everything below is stated as of **July 2026**; verify against the primary source before relying on it.

### European Union

1. 📄 [EU Artificial Intelligence Act (Regulation (EU) 2024/1689)](https://eur-lex.europa.eu/eli/reg/2024/1689/oj) (EU, 2024)
   - *Why*: **World's first comprehensive AI law** - risk-based regulatory framework that has become the reference point most other jurisdictions define themselves against
   - *Risk tiers*:
     - Unacceptable risk: Banned (social scoring, real-time biometric surveillance)
     - High risk: Strict requirements (hiring, credit scoring, law enforcement)
     - Limited risk: Transparency obligations (chatbots must disclose they're AI)
     - Minimal risk: No requirements
   - *Key obligations*: Risk assessment, data quality, documentation, human oversight, accuracy requirements
   - *Foundation models*: Additional requirements for General Purpose AI (GPAI) and systemic risk models
   - *Application timeline* (as of July 2026):
     - Prohibited practices and AI literacy duties: 2 February 2025
     - GPAI model obligations: 2 August 2025 (models already on the market have until 2 August 2027)
     - Article 50 transparency duties: 2 August 2026 — **not deferred**
     - Annex III standalone high-risk systems: deferred to 2 December 2027
     - Annex I high-risk AI embedded in regulated products: deferred to 2 August 2028
   - *Digital Omnibus on AI*: Commission proposal of 19 November 2025 to simplify and delay parts of the Act; provisional trilogue agreement reached 7 May 2026, deferring the high-risk deadlines above and adding an Article 5 prohibition on AI generating non-consensual intimate imagery and CSAM. Formal adoption and Official Journal publication were still pending at time of writing — verify current status before relying on these dates
   - *Resources*: [Commission overview](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) | [Article explorer](https://artificialintelligenceact.eu/ai-act-explorer/) (unofficial)

2. 📄 [General-Purpose AI Code of Practice](https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai) (European Commission, 2025)
   - *Why*: The practical bridge between the AI Act's GPAI obligations and what providers actually have to do; signing it earns streamlined compliance and more predictable enforcement
   - *Structure*: Three chapters — Transparency, Copyright, and Safety and Security
   - *Status*: Published 10 July 2025, ahead of GPAI obligations applying on 2 August 2025; voluntary, with signatories published by the Commission

### United States — Federal

US federal AI policy reversed direction in January 2025. The entries below are ordered chronologically so the shift is legible; two are retained despite being rescinded because the successor orders are written against them.

3. 📄 [National AI Initiative Act](https://www.ai.gov/) (US, 2021)
   - *Why*: Establishes national AI strategy, funding, and coordination
   - *Key bodies*: National AI Initiative Office; National AI Advisory Committee

4. 📄 [Blueprint for an AI Bill of Rights](https://bidenwhitehouse.archives.gov/ostp/ai-bill-of-rights/) (US, 2022)
   - *Why*: Non-binding principles for AI design and deployment in the US
   - *Five principles*: Safe and effective systems; algorithmic discrimination protections; data privacy; notice and explanation; human alternatives
   - *Practical tools*: [Full text and technical companion (PDF)](https://bidenwhitehouse.archives.gov/wp-content/uploads/2022/10/Blueprint-for-an-AI-Bill-of-Rights.pdf)
   - *Status*: **Withdrawn** - removed from whitehouse.gov in January 2025; archived copy linked. Retained here for historical context, as it shaped several state laws that outlived it

5. 📄 [Executive Order 14110 on Safe, Secure, and Trustworthy AI](https://www.federalregister.gov/documents/2023/11/01/2023-24283/safe-secure-and-trustworthy-development-and-use-of-artificial-intelligence) (US, 2023)
   - *Why*: The most comprehensive US federal AI policy to date; established reporting requirements for large models and set the 10^26 FLOP threshold that state frontier-AI laws later adopted
   - *Key mandates*:
     - Safety testing for models trained with >10^26 FLOPs
     - Red-teaming requirements
     - Watermarking for AI-generated content
     - Standards development via NIST
   - *Status*: **Revoked** 20 January 2025 by EO 14148; superseded by EO 14179. Downstream agency work it triggered (AI use-case inventories, NIST standards activity) largely survived the revocation
   - *Note*: Federal Register copy linked; the original White House page is gone

6. 📄 [Executive Order 14179: Removing Barriers to American Leadership in Artificial Intelligence](https://www.federalregister.gov/documents/2025/01/31/2025-02172/removing-barriers-to-american-leadership-in-artificial-intelligence) (US, 2025)
   - *Why*: **The pivot point in US federal AI policy** - replaces EO 14110's safety-and-equity framing with an innovation-and-competitiveness mandate; directs agencies to review and roll back prior AI policies
   - *Consequences*: Triggered removal of EEOC and DOL AI guidance; mandated an AI action plan within 180 days
   - *Date*: Signed 23 January 2025

7. 📄 [OMB M-25-21: Accelerating Federal Use of AI through Innovation, Governance, and Public Trust](https://www.whitehouse.gov/wp-content/uploads/2025/02/M-25-21-Accelerating-Federal-Use-of-AI-through-Innovation-Governance-and-Public-Trust.pdf) (Office of Management and Budget, 2025)
   - *Why*: The operative rulebook for how federal agencies actually adopt AI - matters more day-to-day than the executive orders it implements
   - *Scope*: Agency AI governance structures, minimum practices for high-impact AI use cases, Chief AI Officer responsibilities

8. 📄 [Winning the AI Race: America's AI Action Plan](https://www.ai.gov/action-plan) (US, 2025)
   - *Why*: The policy blueprint EO 14179 ordered; sets the administration's AI agenda across innovation, infrastructure and international diplomacy
   - *Notable*: Recommends withholding federal AI funding from states with regulation deemed burdensome - the seed of the preemption fight that followed
   - *Date*: July 2025

9. 📄 [Executive Order 14365: Ensuring a National Policy Framework for Artificial Intelligence](https://www.federalregister.gov/documents/2025/12/16/2025-23092/ensuring-a-national-policy-framework-for-artificial-intelligence) (US, 2025)
   - *Why*: **Opens a direct federal-versus-state conflict over who regulates AI** - declares a policy of a "minimally burdensome" national standard and moves to displace inconsistent state law
   - *Key mechanisms*:
     - DOJ AI Litigation Task Force, operational from 10 January 2026, to challenge state AI laws in federal court
     - Conditions certain federal funding on state regulatory posture
   - *Carve-outs*: Expressly does not target state laws on child safety, AI compute and data-center infrastructure, or state procurement and government use of AI
   - *Legal caveat*: Preemption ordinarily flows from congressional statute, not executive order; commentators widely expect the EO to guide federal conduct rather than independently displace state law. Litigation outcomes were unresolved at time of writing
   - *Date*: Signed 11 December 2025

### United States — State Laws

With federal AI-specific legislation stalled, states became the primary source of binding US AI law. The entries below are the first-of-kind statutes that other states are modelling; see the trackers under [Practical Compliance](#practical-compliance--implementation) for the full and fast-moving picture.

10. 📄 [California SB 53: Transparency in Frontier Artificial Intelligence Act (TFAIA)](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202520260SB53) (California, 2025)
    - *Why*: **First US state statute targeting frontier AI safety and transparency** - the template New York and others followed
    - *Key requirements*:
      - Publish a frontier AI framework describing safety practices
      - Publish a transparency report before releasing a new frontier model
      - Transmit catastrophic-risk assessments to the California Office of Emergency Services
      - Report critical safety incidents to Cal OES
      - Whistleblower protections for covered employees
    - *Scope*: "Frontier model" = foundation model trained on >10^26 integer or floating-point operations, including subsequent fine-tuning or material modification
    - *Status*: Signed 29 September 2025; effective 1 January 2026

11. 📄 [California SB 243: Companion Chatbots](https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=202520260SB243) (California, 2025)
    - *Why*: **First US law imposing safety duties on companion AI**, enacted in response to incidents involving minors and conversational AI; the model for a wave of 2026 chatbot bills
    - *Key requirements*: Disclose that the user is interacting with AI; for known minors, break reminders at least every three hours; maintain a protocol addressing suicidal ideation and self-harm content with referral to crisis services; annual reporting
    - *Status*: Signed 13 October 2025; effective 1 January 2026

12. 📄 [Texas HB 149: Responsible Artificial Intelligence Governance Act (TRAIGA)](https://capitol.texas.gov/BillLookup/History.aspx?LegSess=89R&Bill=HB149) (Texas, 2025)
    - *Why*: A deliberately narrower alternative to the EU-style risk framework - **intent-based** prohibitions rather than impact-based duties, which makes it the reference point for states resisting the Colorado model
    - *Key provisions*: Bans AI intended for behavioral manipulation, unlawful discrimination, incitement to violence, or CSAM generation; largely limits affirmative obligations to government use; first-in-nation AI regulatory sandbox
    - *Enforcement*: Attorney General exclusively, with notice and a 60-day cure period; no private right of action; preempts local AI ordinances
    - *Status*: Signed 22 June 2025; effective 1 January 2026

13. 📄 [Illinois HB 3773: AI in Employment (amending the Illinois Human Rights Act)](https://www.ilga.gov/Legislation/BillStatus?DocNum=3773&GAID=17&DocTypeID=HB&LegID=157807&SessionID=112) (Illinois, 2024)
    - *Why*: Makes discriminatory AI use in employment a civil rights violation under existing state anti-discrimination machinery, rather than building a separate AI regime - a materially different regulatory strategy worth contrasting with Colorado and Texas
    - *Key requirements*: Prohibits AI use that discriminates against protected classes across hiring, promotion, discipline and discharge; requires notice to applicants and employees when AI is used
    - *Status*: Effective 1 January 2026

14. 📄 [Utah SB 149: Artificial Intelligence Policy Act](https://le.utah.gov/~2024/bills/static/SB0149.html) (Utah, 2024)
    - *Why*: **First US state law specifically regulating generative AI** - a minimal disclosure-based approach that predates the comprehensive frameworks
    - *Key requirements*: Disclose generative AI use on request; 2025 amendments (SB 226, SB 332) added proactive disclosure for high-risk interactions involving health, financial or biometric data
    - *Status*: Effective 1 May 2024; amended 2025

15. 📄 [Colorado SB 26-189: Automated Decision-Making Technology](https://leg.colorado.gov/bills/sb26-189) (Colorado, 2026)
    - *Why*: **The cautionary tale of the group** - Colorado passed the first comprehensive US state AI law (SB 24-205, 2024), delayed it twice, then repealed and replaced it before it ever took effect. Reading the two together shows what proved unworkable about impact-assessment-based regulation
    - *What changed*: Replaces the "high-risk AI system" reasonable-care and impact-assessment regime with a narrower transparency and disclosure framework built on "covered automated decision-making technology" that materially influences consequential decisions
    - *Key requirements*: Pre-use disclosure; explanation of adverse outcomes within 30 days; meaningful human review; documentation of training data categories and system constraints
    - *Status*: Signed 14 May 2026; substantive obligations commence 1 January 2027, with AG rulemaking due by that date. Subject to pending litigation at time of writing

16. 📄 [New York S6953B/A6453B: Responsible AI Safety and Education (RAISE) Act](https://www.nysenate.gov/legislation/bills/2025/S6953) (New York, 2025/2026)
    - *Why*: The second state frontier-AI statute; its 2026 rewrite pulled it substantially toward California's SB 53, making the pair a good study in state-law convergence
    - *Key requirements*: Safety and security protocols for frontier models; incident reporting; annual protocol review; published transparency documentation with trade-secret redactions
    - *Scope*: Developers with annual revenue over $500M, for models trained with >10^26 operations and over $100M in compute cost
    - *Oversight*: Rulemaking assigned to a new office within the New York Department of Financial Services
    - *Status*: Originally signed 19 December 2025; the operative text is the **chapter amendment signed 27 March 2026**. Effective 1 January 2027 - one year after SB 53

### Other Jurisdictions

17. 📄 [China's Generative AI Regulations](http://www.cac.gov.cn/2023-07/13/c_1690898327029107.htm) (China, 2023)
    - *Why*: First national regulation specifically for generative AI
    - *Requirements*: Content filtering, factual accuracy, labeling of AI-generated content
    - *Philosophical approach*: Content-focused vs. Western risk-focused frameworks
    - *English summary*: [Stanford HAI](https://hai.stanford.edu/policy/chinas-generative-ai-regulations)

18. 📄 [Measures for Labeling AI-Generated Synthetic Content](https://www.cac.gov.cn/2025-03/14/c_1743654684782215.htm) (Cyberspace Administration of China, 2025)
    - *Why*: Turns AI content labeling from principle into a concrete build requirement - **both visible labels and embedded metadata/watermark provenance**, which is further than any Western regime has gone in binding law
    - *Status*: Effective 1 September 2025
    - *Context*: Pairs with algorithm registration and security self-assessment obligations already in force

19. 📄 [Framework Act on Artificial Intelligence Development and Trust Base Creation](https://www.law.go.kr/LSW/eng/engLsSc.do?menuId=2&query=ARTIFICIAL+INTELLIGENCE) (South Korea, 2025)
    - *Why*: **Second jurisdiction after the EU with a comprehensive horizontal AI statute** - the clearest test of whether the EU model travels
    - *Key requirements*: Obligations for high-impact AI across designated sectors; fairness and non-discrimination duties; AI-generated content labeling
    - *Status*: Effective 22 January 2026, with a grace period through 2026 during which administrative fines are generally deferred except in serious cases

20. 📄 [India AI Governance Guidelines](https://www.indiaai.gov.in/) (Ministry of Electronics and IT, 2025)
    - *Why*: The most prominent **light-touch** alternative - explicitly declines a standalone AI act, relying on existing law plus voluntary measures; useful contrast to the EU and Korean approaches
    - *Status*: Released November 2025. Not enforceable law; AI is governed through the Digital Personal Data Protection Act and sector rules
    - *Note*: Verify the current guideline URL on the IndiaAI portal, which reorganizes frequently

21. 📄 [Brazil PL 2338/2023: Proposed AI Framework](https://www25.senado.leg.br/web/atividade/materias/-/materia/157233) (Brazil, introduced 2023; pending)
    - *Why*: Closely tracks the EU AI Act's risk-based structure; the leading test of whether that model is adopted across Latin America
    - *Status*: **Not yet law.** Approved by the Senate 10 December 2024; under consideration in the Chamber of Deputies at time of writing. Included here as pending legislation, not a binding instrument

---

## Risk Management Frameworks & Standards
**Goal**: Learn structured approaches to AI risk management

**Why this matters**: Regulations tell you what to do; frameworks tell you how. These voluntary standards provide practical implementation guidance and are increasingly referenced by regulators.

1. 📄 [NIST AI Risk Management Framework (AI RMF)](https://www.nist.gov/itl/ai-risk-management-framework) (NIST, 2023)
   - *Why*: **The definitive US AI risk management framework** - voluntary but increasingly expected by regulators
   - *Structure*: Four core functions: Govern, Map, Measure, Manage
   - *Risk types*: Covers technical, societal, legal, reputational risks
   - *Practical tools*: [Playbook](https://airc.nist.gov/AI_RMF_Knowledge_Base/Playbook)
   - *Companion docs*: Addresses trustworthiness (fairness, robustness, transparency, etc.)

2. 📄 [NIST AI 600-1: Generative AI Profile](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) (NIST, 2024)
   - *Why*: **The companion profile that makes the AI RMF usable for generative systems** - the framework alone predates the GenAI risk surface
   - *Risks addressed*: Confabulation, harmful content generation, privacy, cybersecurity, intellectual property
   - *Structure*: Suggested actions organized around governance, content provenance, pre-deployment testing and incident disclosure, mapped back to the RMF's GOVERN/MAP/MEASURE/MANAGE functions
   - *Date*: Published 26 July 2024

3. 📄 [Center for AI Standards and Innovation (CAISI)](https://www.nist.gov/aisi) (NIST, 2025)
   - *Why*: The US government's technical AI evaluation body; its outputs feed the standards regulators reference
   - *Note*: Renamed from the US AI Safety Institute in mid-2025 - the rename tracked the broader federal shift from safety framing to standards-and-innovation framing
   - *Recent work*: AI Agent Standards Initiative, announced February 2026

4. 📄 [ISO/IEC 42001: AI Management System](https://www.iso.org/standard/81230.html) (ISO/IEC, 2023)
   - *Why*: International certifiable standard for AI management systems
   - *Scope*: Organizational governance, not individual models
   - *Certification*: Organizations can be ISO 42001 certified
   - *Note*: [Purchase required](https://www.iso.org/standard/81230.html) | [Overview available](https://www.iso.org/artificial-intelligence/ai-management-systems)

5. 📄 [ISO/IEC 42005: AI System Impact Assessment](https://www.iso.org/standard/44545.html) (ISO/IEC, 2025)
   - *Why*: Gives the impact-assessment step a standardized shape - increasingly the mechanism regulations point to when they require one
   - *Relationship*: Designed to be used alongside ISO/IEC 42001
   - *Note*: Purchase required

6. 📄 [ISO/IEC 23053: Framework for AI Systems Using ML](https://www.iso.org/standard/74438.html) (ISO/IEC, 2022)
   - *Why*: Technical standard for ML system development lifecycle
   - *Coverage*: Data quality, model development, deployment, monitoring
   - *Note*: [Purchase required](https://www.iso.org/standard/74438.html)

7. 📄 [IEEE 7000 Series on AI Ethics](https://standards.ieee.org/initiatives/autonomous-intelligence-systems/standards/) (IEEE, 2021, ongoing)
   - *Why*: Technical standards for embedding ethics into system design
   - *Key standards*:
     - IEEE 7000: Systems engineering for ethical concerns
     - IEEE 7001: Transparency of autonomous systems
     - IEEE 7002: Data privacy
   - *Approach*: Values-based engineering

8. 📄 [OECD AI Principles](https://oecd.ai/en/ai-principles) (OECD, 2019)
   - *Why*: First intergovernmental AI policy standards; adopted by 40+ countries
   - *Five principles*: Inclusive growth; human-centered values; transparency; robustness; accountability
   - *Implementation*: [National AI policies dashboard](https://oecd.ai/en/dashboards)

---

## Sector-Specific AI Guidance
**Goal**: Navigate industry-specific AI regulations

**Why this matters**: Healthcare AI faces different requirements than financial AI. Understanding sector-specific rules is essential for practical deployment.

### Healthcare & Life Sciences

1. 📄 [FDA's Artificial Intelligence/Machine Learning (AI/ML) Software as a Medical Device Action Plan](https://www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-and-machine-learning-aiml-enabled-medical-devices) (FDA, 2021)
   - *Why*: Regulatory pathway for AI medical devices in the US
   - *Key innovation*: "Predetermined Change Control Plans" for continuously learning models
   - *Requirements*: Clinical validation, performance monitoring, algorithm change protocols

2. 📄 [EU Medical Device Regulation (MDR) & In-Vitro Diagnostic Regulation (IVDR)](https://health.ec.europa.eu/medical-devices-new-regulations_en) (EU, 2017/2022)
   - *Why*: AI diagnostic tools must comply; high scrutiny for "black box" algorithms
   - *Risk classification*: Most AI diagnostics are Class IIa or higher

3. 📄 [HIPAA Privacy Rule and AI](https://www.hhs.gov/hipaa/index.html) (US, 1996, ongoing interpretation)
   - *Why*: Governs use of protected health information in AI training and deployment
   - *Key concerns*: De-identification requirements, minimum necessary principle

### Employment & HR

4. 📄 [EEOC Guidance on AI and Title VII Adverse Impact](https://web.archive.org/web/20240527151347/https://www.eeoc.gov/laws/guidance/select-issues-assessing-adverse-impact-software-algorithms-and-artificial) (EEOC, 2023)
   - *Why*: Clarifies how US employment discrimination laws apply to AI hiring tools
   - *Key point*: Employers liable for discriminatory AI, even from third-party vendors
   - *Requirements*: Validation studies, adverse impact analysis
   - *Companion*: [ADA and AI guidance](https://web.archive.org/web/20240529055014/https://www.eeoc.gov/laws/guidance/americans-disabilities-act-and-use-software-algorithms-and-artificial-intelligence) (EEOC, 2022)
   - *Status*: **Withdrawn** - both documents were removed from the EEOC site in 2025 following EO 14179; archived copies linked. The underlying law did not change: Title VII, the ADEA and the ADA still apply to AI-assisted employment decisions. Several states legislated into the resulting federal gap (see Illinois HB 3773 above)

5. 📄 [NYC Local Law 144 (Automated Employment Decision Tools)](https://www.nyc.gov/site/dca/about/automated-employment-decision-tools.page) (NYC, 2023)
   - *Why*: First US law specifically regulating AI in hiring
   - *Requirements*: Annual bias audits, notice to candidates, alternative evaluation process

### Criminal Justice

6. 📄 [Algorithmic Accountability in Criminal Justice (Various state laws)](https://www.ncsl.org/technology-and-communication/artificial-intelligence-2025-legislation) (NCSL tracker, 2025)
   - *Why*: Many states restrict or require transparency for risk assessment tools
   - *Examples*: California AB 2542, Wisconsin's Loomis decision

---

## Dual-Use AI & National Security
**Goal**: Understand national security considerations for AI

**Why this matters**: Advanced AI models have both beneficial and harmful uses. Export controls, dual-use regulations, and open vs. closed debates shape what can be built and shared.

1. 📄 [Dual-User Foundation Models with Widely Available Model Weights](https://www.ntia.gov/sites/default/files/publications/ntia-ai-open-model-report.pdf) (NTIA, 2024)
   - *Why*: Government perspective on open model policies and dual-use concerns
   - *Note*: Official NTIA government report - freely available

2. 📄 [Export Controls on AI & Emerging Technologies](https://www.bis.doc.gov/index.php/policy-guidance/advanced-computing-and-semiconductor-manufacturing-items) (US Bureau of Industry and Security, 2022, ongoing)
   - *Why*: Controls on exporting AI chips (GPUs), training techniques, and potentially models
   - *2022 updates*: Restrictions on advanced chip exports to China
   - *Ongoing*: Potential controls on model weights, training data

3. 📄 [NSCAI Final Report](https://web.archive.org/web/20240104154550/https://www.nscai.gov/2021-final-report/) (National Security Commission on AI, 2021)
   - *Why*: Comprehensive US national security strategy for AI
   - *Key recommendations*: Defend democratic values; invest in R&D; build international partnerships
   - *Length*: 750+ pages
   - *Note*: The Commission's domain was decommissioned after it sunset; archived copy linked

4. 📄 [Blueprint for an AI Bill of Rights Concerning National Security Systems](https://www.dni.gov/index.php/newsroom/reports-publications) (US, 2023)
   - *Why*: Principles for AI use in intelligence and defense

---

## Responsible AI & Industry Best Practices
**Goal**: Understand voluntary frameworks and industry initiatives

**Why this matters**: Many organizations operate ahead of regulation. These frameworks represent current best practices and often foreshadow future requirements.

1. 📄 [Partnership on AI Guidelines](https://partnershiponai.org/) (Partnership on AI, 2016, ongoing)
   - *Why*: Multi-stakeholder organization developing AI best practices
   - *Members*: Google, Meta, Microsoft, Amazon, civil society groups
   - *Key work*: AI incident database, responsible practices library

2. 📄 [Model Cards for Model Reporting](https://arxiv.org/abs/1810.03993) (Mitchell et al., 2019)
   - *Why*: Transparency framework for documenting model characteristics
   - *Adoption*: Now widely used; required by some regulations
   - *Template*: [GitHub](https://github.com/huggingface/hub-docs/blob/main/modelcard.md)

3. 📄 [Datasheets for Datasets](https://arxiv.org/abs/1803.09010) (Gebru et al., 2018)
   - *Why*: Documentation framework for training datasets
   - *Purpose*: Increase transparency about data provenance, composition, biases
   - *Impact*: Influenced EU AI Act data documentation requirements

4. 📄 [AI Incident Database](https://incidentdatabase.ai/) (Partnership on AI, 2020, ongoing)
   - *Why*: Systematic collection of AI system failures and harms
   - *Learning*: Pattern identification across incidents
   - *Examples*: Hiring discrimination, safety failures, privacy breaches

5. 📄 [Microsoft Responsible AI Standard](https://www.microsoft.com/en-us/ai/responsible-ai) (Microsoft, 2022)
   - *Why*: Corporate AI governance framework from major AI provider
   - *Public version*: [Principles and approach](https://www.microsoft.com/en-us/ai/principles-and-approach)
   - *Structure*: Goals, requirements, tools, governance

6. 📄 [Google's AI Principles](https://ai.google/responsibility/principles/) (Google, 2018)
   - *Why*: Early corporate AI ethics framework
   - *Key commitments*: Social benefit, fairness, safety, accountability
   - *Controversies*: Application debates (Project Maven)

---

## Practical Compliance & Implementation
**Goal**: Apply policy frameworks in real-world scenarios

**Resources for Practitioners**:

### Assessment Tools
- **[NIST AI RMF Playbook](https://airc.nist.gov/AI_RMF_Knowledge_Base/Playbook)** - Step-by-step implementation
- **[EU AI Act Compliance Checker](https://artificialintelligenceact.eu/assessment/)** - Determine risk classification
- **[Microsoft HAX Toolkit](https://www.microsoft.com/en-us/haxtoolkit/)** - Human-AI experience design patterns

### Audit & Testing
- **[NIST SP 1270: Managing Bias in AI](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.1270.pdf)** - Standard for identifying and managing algorithmic bias
- **[Aequitas](http://aequitas.dssg.io/)** - Open-source bias audit toolkit
- **[AI Verify](https://aiverifyfoundation.sg/)** - Singapore's AI testing framework

### Documentation Templates
- **Model Cards** - [Hugging Face template](https://huggingface.co/docs/hub/model-cards)
- **Data Cards** - [Google template](https://sites.research.google/datacardsplaybook/)
- **AI Impact Assessments** - [Ada Lovelace Institute](https://www.adalovelaceinstitute.org/report/algorithmic-impact-assessment-case-study-healthcare/)

### Legal Resources
- **[Stanford HAI Policy Hub](https://hai.stanford.edu/policy)** - Tracking global AI policy
- **[OECD AI Policy Observatory](https://oecd.ai/)** - International policy database
- **[AlgorithmWatch](https://algorithmwatch.org/)** - Automated decision-making accountability

### US State Legislation Trackers
State AI law moves faster than any curated list can. Use these for current status rather than relying on the entries above:
- **[MultiState AI Legislation Tracker](https://www.multistate.ai/artificial-intelligence-ai-legislation)** - All 50 states, updated continuously
- **[NCSL AI Legislation Summary](https://www.ncsl.org/technology-and-communication/artificial-intelligence-2025-legislation)** - Enacted legislation by state and session

**2026 trend lines worth watching**: algorithmic pricing restrictions (California AB 325, New York S.7882, Connecticut HB 8002); second-generation employment-AI rules moving from disclosure to audit and anti-discrimination duties; laws barring AI from implying licensed-professional status in healthcare; and expanded non-consensual deepfake provisions.

---

## Key Takeaways

- **Multi-jurisdictional complexity**: AI systems often face overlapping regulations across geographies and sectors
- **Risk-based approach emerging**: Most frameworks categorize AI by risk level with proportional requirements — though Texas and India show that a light-touch or intent-based alternative is actively contested, not settled
- **The ground shifts under you**: between 2024 and 2026 the EU deferred its high-risk deadlines, the US federal posture reversed and then moved to preempt the states, Colorado repealed its own landmark law before it took effect, and two federal guidance documents were withdrawn outright. Treat every effective date as provisional and check the primary source
- **US regulation is currently state regulation**: with federal AI legislation stalled, binding US obligations come mostly from states — and are now the subject of an explicit federal preemption effort (EO 14365)
- **Documentation is critical**: Model cards, datasheets, impact assessments increasingly expected or required
- **Human oversight emphasized**: Most frameworks require meaningful human involvement in high-stakes decisions
- **Accountability clearly assigned**: Organizations can't hide behind "the algorithm did it"
- **Transparency vs. IP tension**: Balancing explainability requirements with proprietary interests
- **Continuous monitoring**: One-time validation insufficient; ongoing performance monitoring required
- **Interdisciplinary teams**: Compliance requires legal, technical, and domain expertise

---

## Further Reading

### Books & Reports
- **[Weapons of Math Destruction](https://weaponsofmathdestructionbook.com/)** (Cathy O'Neil, 2016) - Impact of algorithms on society
- **[Atlas of AI](https://www.katecrawford.net/)** (Kate Crawford, 2021) - Material and political dimensions of AI
- **[The Alignment Problem](https://brianchristian.org/the-alignment-problem/)** (Brian Christian, 2020) - AI safety and values

### Policy Tracking
- **[Future of Life Institute AI Policy](https://futureoflife.org/ai-policy/)** - Policy advocacy and tracking
- **[Center for AI and Digital Policy](https://www.caidp.org/)** - Global AI policy monitoring
- **[AI Now Institute](https://ainowinstitute.org/)** - Social implications research

### Academic Centers
- **[Stanford Institute for Human-Centered AI (HAI)](https://hai.stanford.edu/)**
- **[MIT Media Lab Ethics & Governance of AI](https://www.media.mit.edu/groups/ethics-and-governance-of-ai/overview/)**
- **[Oxford Internet Institute AI Ethics](https://www.oii.ox.ac.uk/research/ai-ethics/)**

---

**Related**: [Hardware](hardware.md) | [Safety](safety.md) | [Human-AI Interaction](human-ai-interaction.md)
