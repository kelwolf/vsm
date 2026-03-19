# Complete Conversational Context — EA Project

*All sessions, February 24–27, 2026. Sequential, factorial accounting.*

---

## Session 1: Business Plan (Feb 24)

### Starting Point
Operator asked: what is the most practical mental model for employment when the goal is to get a job?

### Key Developments

**Employment as transaction.** Employment is a transaction where you solve a specific problem someone is willing to pay to have solved. An employer has work that needs doing and is looking for someone to match with.

**EA role identified.** Executive administration / executive assistant / administrative officer / secretarial service — different names for the same core function. The problem solved: an executive has finite attention and too many operational demands. The EA multiplies the executive's capacity.

**Automation insight.** The role is heavily automatable — not by the executives, but by the EAs themselves. The EAs who automate become more valuable because they expand what they can handle. The EAs who don't automate are the ones threatened.

**Scaling intent.** Operator's goal is not a single employment relationship but scaling the ability to transact across multiple clients/jobs, including job stacking (holding multiple positions simultaneously where automation handles the throughput).

**PRD created.** Synthesized as a product requirements document: transactional employment model, automation as leverage, multiplexed engagements.

**Pivot to SBA business plan.** Operator wanted a conventional SBA-approvable business plan format — not to apply for SBA funding but to use a rigorous, externally validated structure. Full nine-part plan produced.

### Decisions Made
- EA is the target role
- Automation is the core differentiator
- Multi-client / job-stacking model is the aspiration
- SBA business plan format is the planning structure

### Files Created
- Business plan (SBA format)
- PRD

---

## Session 2: Employment Pivot + System Integration (Feb 25)

### Starting Point
Continued from Session 1 with the SBA business plan.

### Key Developments

**Interview protocol.** 71-question comprehensive interview generated, sorted by business plan section, to stress-test every assumption.

**NotebookLM research integration.** Operator pasted extensive research from NotebookLM covering EA tools, workflows, SOPs, automation methodologies. Sorted for relevance. Deep integration into business plan with full traceability via integration log.

**Executive summary derived.** Standalone executive summary created from the developed business plan.

**Pivot from business to employment.** Operator decided: no longer building this as a business at this stage. Instead pursuing two tracks: (1) get employed as an EA, (2) help others gain EA employment by expanding access to employment opportunities within a small inner circle (2–5 people).

**Inner circle defined.** Not a formal structure — personal network of people operator can help gain employment. Initial conditions: Kellen (not employed, looking at UCSF), Maylee (not employed, looking for work), Mike (employed at UCSF as administrative officer for department head/CSO, training partner). Scope is an open placeholder for iterative development.

**kelwolf-core system discovered.** Operator had an existing operating system built with Claude Code: kelwolf-core (~/core). Contains CORE.md (operating principles: The Book as source of truth, Layer Model, Write-Orchestrate-Execute, self-annealing, session management, documentation as infrastructure, operator judgment at decision points), CLAUDE.md (session init directive), COMMANDS.md, PROJECT-TRACKER-TEMPLATE.md. Medicine Basket Goods is another project using the same system.

**Terminal literacy established.** Operator needed context for terminal commands (cd, ~, git concepts). Established format: every instruction comes with context explaining what the command does and why.

**Repository naming corrected.** Repos renamed: kelwolf-core → core, kelwolf-ea → ea. Convention: kelwolf/{project-name} on GitHub, ~/{project-name} locally. Medicine Basket Goods local folder renamed to ~/medicine-basket-goods.

**EA project initialized.** ~/ea created, connected to GitHub, CLAUDE.md created pointing to ~/core then ~/ea. THE-BOOK.md created per kelwolf-core protocol. Claude Code session booted and read all project files.

**Operating principle added.** "The Book is for decisions, not data." Added to CORE.md. Operator corrected initial draft for being too specific/not aging well — refined to the essential principle.

**Notion integration established.** API key created, stored in ~/.zshrc as environment variable. NOTION-INTEGRATION.md created in ~/core as reusable infrastructure reference. Integration connected and tested.

**Notion workspace V1 built.** Claude Code built full workspace via API: dashboard, SOPs, job tracker with 12 UCSF positions, 14-tool automation stack, 6 SOPs, 6 agent workflows, inner circle structure. Build script saved as build-notion.py. NOTION-WORKSPACE.md saved as reference.

**V1 feedback.** Operator said it should feel like Jarvis from Iron Man — not a filing cabinet but a system that knows the situation before you ask, surfaces what matters, offers options with context, and gets smarter over time.

### Decisions Made
- Pivot from business plan to employment strategy
- Inner circle model: 2–5 people, personal network, iterative scope
- Three people identified: Kellen, Maylee, Mike
- kelwolf-core is the governing operating system
- Terminal instruction format: always provide context
- Repo naming convention: kelwolf/{project-name}
- Notion is the operational layer, connected via API
- "The Book is for decisions, not data" — core principle

### Files Created/Modified
- ~/ea/ project initialized with CLAUDE.md, THE-BOOK.md, PROJECT-TRACKER.md
- ~/core/CORE.md updated with new principle
- ~/core/NOTION-INTEGRATION.md created
- ~/ea/NOTION-WORKSPACE.md created
- ~/ea/build-notion.py created
- Notion workspace V1 built

---

## Session 3: Notion V2 Rebuild (Feb 27a)

### Starting Point
V1 Notion workspace felt overwhelming. Needed redesign.

### Key Developments

**Design critique of V1.** Operator: "it feels overwhelming; I would rather have it nested and intuitive to navigate, with an emphasis on functional flow." V1 was a system map, not a work surface. Didn't answer the daily question: "What do I need to do right now?"

**Critical correction on instances vs. system.** Operator: "you keep conflating the instances with the system: job search vs. employed is purely instance — these are operational contexts not system requirements." The system doesn't change based on context. What changes is what's processed through it.

**V2 designed.** Command Center as daily work-processing surface: Briefing (status summary), Inbox (capture/triage), Actions (active work), Waiting (pending others). Full system (tools, SOPs, agents) nested one level down in Toolbox. Pipeline for job tracking. Operator Dashboard for aggregate view.

**Version control for Notion builds.** Operator wanted build scripts version-controlled rather than deleted and recreated. V2 build script saved as build-notion-v2.py alongside V1's build-notion.py.

**Claude Code OAuth debugging.** Notion API appeared to expire. Investigation revealed it wasn't the Notion key — Claude Code's own OAuth session had expired. Fixed by re-authenticating Claude Code itself. Key learning: the error message was misleading; the actual problem was upstream.

**V2 built and deployed.** Clean hub with briefing callout, three databases (Inbox with 4 pre-populated items, Actions empty, Waiting empty), nested Toolbox/Pipeline/Operator Dashboard pages.

### Decisions Made
- Notion is a work-processing surface, not a system map
- System is context-independent; contexts are instances
- Version control all build scripts
- V2 structure: Briefing + Inbox/Actions/Waiting + nested Toolbox/Pipeline/Dashboard

### Files Created/Modified
- ~/ea/COMMAND-CENTER-V2.md created
- ~/ea/build-notion-v2.py created
- Notion workspace V2 built

---

## Session 4: Demo + Intelligence Brief (Feb 27b)

### Starting Point
V2 built. Mike and Maylee on Zoom for live demo.

### Key Developments

**V2 feedback.** Operator: "I don't feel like my load is lightened by logging in. I have no sense that automation is enabled or that Jarvis is there to assist. The design itself should indicate function."

**Critical realization about Notion's role.** Notion is not the system — it's the front end for a system that lives elsewhere. Intelligence lives in the pipeline (the orchestration layer that processes data, makes assessments, pushes updates into Notion). Notion is the display and interaction layer. Users see pre-processed, pre-assessed data with action options. Their selections flow back as data.

**Simplest intelligent version scoped.** Manual script → pre-assessed data → Notion with action options → operator sees responses. The pipeline is what makes it feel like Jarvis. Without it, Notion is just a database.

**Demo pipeline built.** demo-pipeline.py created live on Zoom: read 12 UCSF positions from Notion, assess each against operator criteria (grade floor, compensation floor, role types), write fit analysis back to Notion with tier assignments.

**Intelligence brief created.** Strategic intelligence brief in IC format (modeled on DNI/CIA congressional briefing conventions) describing why EA role is suited for the three individuals. Navy section banners, classification markings, individual subject assessments.

### Decisions Made
- Notion is UI layer to backend pipeline, not the system itself
- Pipeline is what makes the system intelligent
- Demo validated the concept for inner circle

### Files Created/Modified
- ~/ea/demo-pipeline.py created
- Intelligence brief created (in conversation, not committed)

---

## Session 5: Mobile OS Architecture + Gap Analysis (Feb 27c — pre-compaction)

### Starting Point
EA training exercise with Mike, then pivot to mobile OS design.

### Key Developments

**EA training: email processing.** Mike presented training exercise: email from Sarah Hopkins (ASCO) to Eric (Mike's principal) about two Science Matters video items. Mike was CC'd. Full analysis of EA response protocol: monitor inbox → prompt principal → hold the line → coordinate scheduling → draft response. Automation analysis: detection/tracking fully automatable, drafting semi-automatable, judgment/timing/relationship management not automatable. System designed around this split.

**Mobile OS: three failed attempts.**

*Attempt 1:* Three phone modes (morning briefing, training reps, capture). Operator correction: "This isn't about training reps or time blocking. The system is for running my EA office from my phone."

*Attempt 2:* Four apps as office components with knowledge architecture. Operator correction: "This design equates levels where there is instead hierarchy: education and job search are activities, not system components."

*Attempt 3:* Pure system infrastructure. Operator correction: "This doesn't integrate the system I already have via kelwolf-core."

**NotebookLM research integration.** Operator provided compiled research. Key findings sorted by relevance:

- Claude Code Remote Control: generates URL/QR code syncing desktop terminal to phone. Collapses gap between strategic layer and phone. Requires Pro/Max plan.
- Obsidian as complement/alternative to Notion: local-first, markdown-based, works offline. Strategic layer already lives in markdown. Could serve as mobile-accessible interface via iCloud sync.
- claude.md as living documentation: updated frequently, kept concise, documents what Claude should NOT do.
- /context, /today, /close command patterns: custom commands for loading context, generating daily plans, closing sessions.
- Skills architecture with progressive disclosure: descriptions trigger specific skill files dynamically.
- Parallel AI delegation: spawn separate Claude instances for specialized tasks.
- Git as audit trail: auto-commit hooks track every AI-generated change.

**Obsidian integration decided.** Architecture boundary: Obsidian = brain (strategic layer, private, decisions, durable reference). Notion = office (operational layer, shared, transient data, databases). Boundary rule: if you decided it or wrote it → Obsidian. If operational data, shared, or database-managed → Notion.

**Six-component architecture defined.** Obsidian (strategic), Notion (operational), Claude Code (orchestration), Claude Mobile (intelligence), Google Drive (documents), GitHub (version control).

**File topology designed.** Vault in iCloud Drive with symlinks to git repos. Obsidian on Mac follows symlinks; iCloud syncs content to phone; .git directories stay outside iCloud.

**Pipeline included in spec.** Operator agreed: architecture without pipeline is static containers (same mistake a third time). Spec must include pipeline design and implementation.

**Critical evaluation of spec plan.** Weaknesses identified: spec assumes Obsidian familiarity (operator never used it), pipeline underspecified, iCloud/git coexistence is technical risk, Claude Code remote control is conditional, existing Notion build not addressed, Claude Mobile context problem, spec too large.

**Gap analysis.** Ten gaps identified:
1. Automation runtime — completely missing. No component runs pipelines on schedule.
2. Calendar — completely absent. No scheduling integration.
3. Email — completely absent. Core EA function unaddressed.
4. Communication — absent but manageable with existing channels.
5. Obsidian knowledge management — undefined linking/property conventions.
6. Inner circle access model — architecturally unresolved.
7. Credentials management — fragile.
8. Cost — unaddressed. Operator unemployed.
9. Backup/recovery — partial.
10. Mobile input — UX gap.

**Full spec written.** EA-OFFICE.md v3: ten components (six primary, four supporting), file topology, Obsidian configuration, Notion restructuring, three concrete pipelines, remote control, Claude Mobile context protocol, operational concerns, CPM project management methodology, four-phase implementation with dependency tables.

### Decisions Made
- Obsidian for strategic layer, Notion for operational layer
- Six primary + four supporting components
- Symlink-based file topology
- Three pipelines: Job Assessment, Briefing Generator, Circle Status Sync
- CPM methodology for phased implementation
- No paid tools until employment
- Remote control is capability enhancer, not foundation

### Files Created/Modified
- ~/ea/EA-OFFICE.md created (commit 53c3e3e)
- ~/ea/THE-BOOK.md updated with adoption decision (commit 5da925a)
- ~/ea/PROJECT-TRACKER.md updated with Phase 1 tasks (commit 5da925a)
- ~/ea/EA-OFFICE-EDITS.md created (commit 0344a3f)
- EA-OFFICE.md Edit 1: CLAUDE.md added to core/ listing (commit 6b6fd72)

---

## Session 6: Current Session (Feb 27 — post-compaction)

### Starting Point
EA-OFFICE.md committed. Beginning Phase 1 execution.

### Key Developments

**Version control for EA-OFFICE.md.** Operator wanted to track edits. Decision: git provides version history — version number removed from document header. EA-OFFICE-EDITS.md created for logging edit rationale.

**Edit 1 applied.** CLAUDE.md was missing from core/ listing in Section 4 Knowledge Base Structure. Fixed and committed.

**Structured task execution process drafted.** Pattern for working through phased implementation: task identifier, dependencies, spec context, operational context, instruction, instruction target. Operator identified this should be saved to kelwolf-core as reusable infrastructure.

**Upstream architecture identified.** EA-OFFICE.md contains both project-specific and general infrastructure content. General content should live upstream in ~/core. This prompted the question: what is the right upstream document?

**CORE.md → OFFICE.md proposed.** An office is an operating system. OFFICE.md would become the top-level document, absorbing CORE.md and the general infrastructure from EA-OFFICE.md.

**OFFICE.md → ORGANIZATION.md.** Operator recognized: core is logically embedded in office, office is logically embedded in organization. "Organization" already exists in Apple Notes as top-level folder for organizational documents.

**Three senses of organization identified.** Organization means:
1. The act of organizing — structuring, deciding what goes where
2. The system of organization — documents, tools, processes, architecture
3. The organization itself — the evolving entity (currently single operator + inner circle)

All three are real and active. The top-level governing concept must account for all three.

**Modular documentation, not monolithic.** One document covering all three senses would be monolithic. Documentation is infrastructure. Infrastructure is modular. Each sense should be its own document, independently versioned, independently evolved.

**Three documents named.**
1. **ORGANIZATION.md** — the entity. What the organization is, who's in it, how it's constituted.
2. **OPERATIONS.md** — the system. How the organization operates. Components, topology, access, information flow, tools, environment. Absorbs general infrastructure from EA-OFFICE.md.
3. **METHODOLOGY.md** — the practice. How work is structured and executed. Layer model, project management, phased implementation, structured task execution, operating principles. Absorbs CORE.md content.

### Decisions Made
- Git is the version control system for all docs (no version numbers in files)
- EA-OFFICE-EDITS.md tracks edit rationale per edit
- Structured task execution is a reusable process (not yet codified)
- CORE.md is retired, content distributed to three new documents
- Three upstream documents: ORGANIZATION.md, OPERATIONS.md, METHODOLOGY.md
- Each organizational sense gets its own document for independent evolution
- Naming convention must reflect contained concepts

### Pending Work (In Order)
1. Draft ORGANIZATION.md, OPERATIONS.md, METHODOLOGY.md — present for revision
2. Create in ~/core, delete CORE.md, commit and push
3. Refactor EA-OFFICE.md to inherit from upstream documents
4. Grep all repos for "CORE.md" references, update
5. Check Notion pages and build scripts for stale references
6. Codify structured task execution process in METHODOLOGY.md
7. Resume Phase 1 execution starting at Task 1.1 (Install Obsidian)

### Downstream Migration Requirements
- Every project's CLAUDE.md reads "all markdown in ~/core" — new files auto-discovered, no change needed
- EA-OFFICE.md references CORE.md by filename in Sections 1 and 4 — must update
- PROJECT-TRACKER.md — check for CORE.md references
- Medicine Basket Goods — check for filename references
- Notion pages may contain "CORE.md" text — update during planned restructuring or via API
- Build scripts — grep for references
- Git history preserves CORE.md forever

---

## Distribution of CORE.md Content

Everything currently in CORE.md goes to METHODOLOGY.md:
- The Book as source of truth per project
- The Layer Model (structured build sequence)
- Write-Orchestrate-Execute protocol
- Self-annealing principle
- Session management
- Documentation as infrastructure
- Operator judgment at decision points
- Undefined elements stay open
- The Book is for decisions, not data

## Distribution of EA-OFFICE.md General Content

To OPERATIONS.md:
- Section 2: System architecture component model
- Section 3: File topology (vault/symlink/iCloud)
- Section 4: Obsidian configuration
- Section 7: Claude Code remote control
- Section 8: Claude Mobile context protocol
- Section 9: Operational concerns patterns

To METHODOLOGY.md:
- Section 10: Project management methodology (CPM, dependency types)
- Section 11: Phased implementation structure (not specific tasks)
- Structured task execution process (not yet written)

Stays in EA-OFFICE.md:
- Specific Notion databases, inner circle access, three pipelines, Notion restructuring, Phase 1/2/3/4 task tables, UCSF targeting, cost specifics, knowledge base structure

---

## Key Design Principles (Accumulated)

1. Employment is a transaction
2. Automation is the EA's core differentiator
3. The Book is for decisions, not data
4. System is context-independent; contexts are instances
5. Documentation is infrastructure — modular, not monolithic
6. Undefined elements stay open
7. The system must function fully without conditional capabilities (e.g., remote control)
8. Pipeline is what makes the system intelligent; architecture without pipeline is static containers
9. Notion is UI layer to backend pipeline, not the system itself
10. Naming conventions must reflect the concepts they contain
11. Each organizational sense (entity, system, practice) evolves independently
12. Always provide context with instructions
13. No paid tools until employment provides income
14. The job search is the critical path activity

---

## People

- **Kellen (operator):** Building the system. Not employed. Job searching at UCSF. Mobile-first. Has never used Obsidian. Terminal-literate but learning.
- **Maylee:** Inner circle. Not employed. Looking for work. First recipient of system access.
- **Mike:** Inner circle. Employed at UCSF as administrative officer for department head/CSO. EA training partner. Seasoned professional.

---

## Active Files and Their Locations

### ~/core/ (kelwolf-core repo)
- CORE.md — *to be retired, content → METHODOLOGY.md*
- CLAUDE.md — session init directive
- COMMANDS.md — operator command reference
- PROJECT-TRACKER-TEMPLATE.md — per-project template
- NOTION-INTEGRATION.md — API connection reference

### ~/ea/ (ea repo)
- THE-BOOK.md — project source of truth
- PROJECT-TRACKER.md — session continuity
- CLAUDE.md — session init (reads ~/core then ~/ea)
- EA-OFFICE.md — system specification (v3, current)
- EA-OFFICE-EDITS.md — edit tracking
- COMMAND-CENTER-V2.md — Notion V2 spec
- NOTION-WORKSPACE.md — workspace reference
- build-notion.py — V1 build script
- build-notion-v2.py — V2 build script
- demo-pipeline.py — demo script

### Notion
- Command Center (V2): Briefing, Inbox (4 items), Actions (empty), Waiting (empty)
- Nested: Toolbox, Pipeline, Operator Dashboard

### Credentials
- NOTION_API_KEY in ~/.zshrc
- NOTION_EA_PAGE_ID in ~/.zshrc

---

## Session 6 Addendum: VSM Mandate (Feb 27 — continued)

### Key Developments

**Evaluation criteria derived from first principles.** Three domains examined (organizational design, enterprise architecture, systems theory) not for frameworks but for imperatives — what must be true for any organization to function:

1. **Division and reintegration** — work must be split and reconnected
2. **Function, structure, purpose must all be visible** — nothing can be invisible to the system
3. **Internal variety must match environmental variety** — the system must be as complex as what it faces

These three imperatives synthesize into a unit specification: every unit must be **self-describing** (purpose, structure, function visible), **self-connecting** (interfaces defined at every boundary), and **self-varying** (able to produce responses proportional to demands).

**Five-document architecture evaluated and found insufficient.** Against the three imperatives: division was sound but reintegration was insufficient (no downstream propagation, no lateral coordination). Structure was visible but function was partial and purpose was invisible at org level. Variety was moderate but had critical single-operator bottleneck.

**Retrofit and overfit patterns identified.** Operator repeatedly corrected approach of evaluating existing design against criteria rather than deriving design from criteria. Also corrected pattern of treating scale as future state rather than unit-level property.

**Unit-level economics principle established.** Scale is a property of the unit, not a future state. If the unit doesn't scale at the unit level, adding more units doesn't create scale. The question is always: does this unit, as designed, function correctly if instantiated a hundred times with no additional design work?

**VSM identified as mandated structural foundation.** Stafford Beer's Viable System Model is the only model found that satisfies all three imperatives completely — not as recommendations but as structural requirements for viability:
- Self-describing: S1-S3 (function), five-subsystem structure (structure), S5 (purpose) — all required
- Self-connecting: S2 (coordination), six information channels — every boundary has a defined interface
- Self-varying: Built on Ashby's Law, S4 (environmental scanning), five variety balances — diagnostic at every level

The recursive property means the unit at any level has the same five-subsystem structure as every other level. Scale is a structural property of the unit itself.

**Mandate issued.** The organizational architecture will be redesigned from the VSM. The previous five-document structure (ENTITY.md, OPERATIONS.md, OFFICE.md, METHOD.md, README.md) is retired as a starting point. The new starting point is Beer's five subsystems and their required interrelationships, applied recursively.

### Decisions Made
- Three foundational imperatives established as evaluation criteria
- Self-describing, self-connecting, self-varying as unit specification
- VSM mandated as structural foundation
- Previous document architecture retired
- Scale is a unit-level property, not a future state

### Pending Work (Updated)
1. Design organizational architecture from VSM first principles
2. Map existing content (CORE.md, EA-OFFICE.md, etc.) onto VSM structure
3. Determine document set that satisfies VSM requirements
4. Draft documents, present for revision
5. Execute migration (rename ~/core → ~/org, update references)
6. Resume Phase 1 task execution

### Files Created
- /mnt/user-data/outputs/VSM-REFERENCE.md — primary reference for VSM application
- /mnt/user-data/outputs/COMPLETE-CONTEXT-2026-02-27.md — updated with VSM mandate
