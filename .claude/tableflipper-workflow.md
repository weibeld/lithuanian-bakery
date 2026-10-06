Tableflipper (agentic development workflow) concept

This document contains the current (2026-09-24) conceptualisation for Tableflipper including the earlier attempts at creating an agentic development workflow that Tableflipper is based on.

> Note: this is an excerpt from the original Owl note 1790167562.md taken on 2026-10-06.

## Idea

- Reuse proven software development lifecycle (requirements engineering, architecture, development) with each phase assisted by agents
- TBD: Implemented as an agent skill ⚠️  TODO: investigate suitability of a skill for this (e.g. Claude Code Skill)
- Different roles naturally have different levels of agent human vs. responsibilities:
  - Requirements: mostly human (human provides content, agent may support with formalities)
  - Architecture: 50/50 (agent proposes architecture, human reviews and decides)
  - Development: mostly agent (agent implements, human supervises)
- Value proposition: not a novelty or technical invention, pieces together existing parts, provides value through curation and vetting by providing convenience and consistency
- Benefits:
  - Scaffold directory structure
  - Scaffold artefacts (e.g. requirements documents, architecture documentation)
  - Vetted set of technologies, solutions, and methodologies for requirements engineering, architecture, and development
  - TBD: Bundled authoritative reference material (guaranteeing accurate and up-to-date agent knowledge e.g. for requirements or architecture approaches) ⚠️  TODO: investigate viabiilty and how to implement. Use MCP?
  - Explicit approval points in control flow (e.g. for architecture decisions)
  - TBD: internal consistency enforcement (e.g. ADRs against code, quality attributes in requirements vs. arc42, etc.) ⚠️  TODO: investigate how to implement (see e.g. Decision Guardian, Mneme)
  - TBD: development approach? ⚠️  TODO: research whether specific agentic development approaches that fit into this framework exist
  - TBD: Utility commands (e.g. generating documentation artefacts) ⚠️  TODO: evaluate if needed, and if so, what (e.g. arc42 Canvases as generated output)
  - TBD: prototyping support? ⚠️  TODO: evaluate whether prototyping as a means for requirements discovery and risk-reduction in architecture should be supported by the workflow, and if so, how
  - TBD: quality assurance? ⚠️  TODO: evaluate whether quality assurance can and should be supported somehow by the workflow
  - TBD: holistic documentation (guidebook)? ⚠️  TODO: evaluate whether to include support for creating a Simon Brown type guidebook (broader than arc42 docs), how to handle duplication of information and syncing, location (directory, README, etc.)
- Core design choices:
  - TBD: req42 for the requirements document ⚠️  TODO: do more research for alternatives
  - Q42 as the quality model for requirements
  - arc42 for the architecture documentation
  - TBD: Nygard format for ADRs ⚠️  TODO: evaluate alternatives, preference for just sticking with a standard format over inventing a custom sophisticated format
  - TBD: LikeC4 for diagramming ⚠️  TODO: evaluate alternatives
  - TBD: architecture methodology? ⚠️  TODO: do research on architecture methodologies
- Directory structure (directories with brackets are optional and created on demand):
  ```
  /
  ├─ requirements/       # Requirement docs
  ├─ architecture/       # Architecture docs
  ├─ TBD: tools/         # Tools for utility commands ⚠️  TODO: evaluate whether this is necessary
  ├─ [generated/]        # Disposable generated output
  ├─ <implementation>    # Code
  ├─ TBD: [prototypes/]  # Prototype code ⚠️  TODO: evaluate whether to explicitly support prototyping, and if so, how
  ├─ TBD: [guidebook/]   # Software guidebook by Simon Brown ⚠️  TODO: evaluate whether to include, and location (e.g. directory, README, single file)
  └─ TBD: [concept.md]   # Concept doc (corresponding to Conceptualisation phase of SDLC) ⚠️  TODO: evaluate whether to include, i.e. should the agent help even with this?
  ```

> TODO: for resolving the arc42 vs. software guidebook question: would it be an option to have different workflow levels, a full one and a light one, and the full one uses arc42, etc (full directory structure) and the light one uses only the software guidebook instead (single file)? The rationale is that the software guidebook is designed to be standalone (arguably, unless arc42 which depends on requirement docs, etc.) and it can probably be made rather compact.
