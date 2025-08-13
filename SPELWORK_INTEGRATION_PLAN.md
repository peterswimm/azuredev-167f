# SPELWork-Infused Azure AI Template Integration Plan

## Overview
This document outlines the transformation of the Azure AI Foundry agent template into a Toilville-aligned, SPELWork-governed system.

## Current State Analysis
This workspace implements a comprehensive Azure AI agent solution with:
- FastAPI backend with streaming responses
- React/TypeScript frontend with Fluent UI
- Azure AI Agents with knowledge retrieval
- Complete infrastructure as code (Bicep)
- Monitoring and evaluation capabilities

## Core Architecture Enhancements

### 1. Replace Chat Interface with Wish-Based Workflow
- Transform `src/api/routes.py:37` chat endpoint into wish submission/processing
- Add Seven Questions validation before agent interactions:
  - Intent
  - Motivation
  - Stakeholders
  - Effort
  - Risks
  - Success criteria
  - Next steps
- Implement progressive consent checkpoints

### 2. Add Governance Manifests
- Create `manifests/actor_manifest.yaml` for role definitions
- Add `manifests/workspace_manifest.yaml` for boundaries and contracts
- Implement `trustlog.jsonl` for all agent interactions
- Define contract-bound workspace enforcement

### 3. Rockford Trust Integration
- Wrap Azure AI responses with trust scoring at `src/api/routes.py:78`
- Add lens certification for different deliberation contexts
- Implement citation trust verification
- Create Rockford Federation scoring endpoints

## Specific Implementation Points

### 4. Ritual Pipeline (Replace Simple Chat)
- Transform frontend from chat to ritual authoring (Kurt-style PWA)
- Add wish → ruse → ritual → rubric flow
- Store rituals in vector DB (Chroma) alongside Azure Search
- Implement stateless authoring patterns

### 5. Steward Tone Management
- Add tone-aware filtering between user and Azure agents
- Implement "Mayor's Promise" humility checks
- Create egoless rigor validation
- Add draft assistant capabilities

### 6. Memory Auditing
- Extend `src/api/main.py:18` lifecycle with memory pipeline
- Add prompt history tracking
- Implement collapse detection for ruse offloading
- Create memory agent "Paladin" integration

## Ethical AI Enhancements

### 7. SPELWork's 18 Dimensions Evaluation
Extend `evals/evaluate.py` with SPELWork dimensions:
- Consent
- Plurality
- Traceability
- Transparency
- Accountability
- Fairness
- Privacy
- Security
- Reliability
- Safety
- Interpretability
- Sustainability
- Accessibility
- Inclusivity
- Dignity
- Agency
- Beneficence
- Non-maleficence

Add dimension-based agent selection and scoring.

### 8. ToilMail Integration
- Add secure messaging layer for sensitive interactions
- Implement ruse-based value generation
- Create audit trails for all communications
- Add trauma-aware research bundles

### 9. OMAC Core (Ops and Memory Arbitration)
- Add operations and memory arbitration core
- Implement contract-bound workspace enforcement
- Create arbitration endpoints
- Add dispute resolution mechanisms

## Monitoring & Compliance

### 10. Trust Analytics
- Extend Application Insights with trust metrics
- Add Rockford Federation scoring
- Implement civic readiness assessments
- Create deliberation scoring dashboards

## Implementation Priority

### Phase 1: Foundation
1. Create manifest structure
2. Implement wish-based workflow
3. Add basic trust scoring

### Phase 2: Governance
4. Add Toilville governance layer
5. Implement Steward tone management
6. Create memory auditing

### Phase 3: Advanced Features
7. Implement full Ritual pipeline
8. Add 18 Dimensions evaluation
9. Integrate ToilMail
10. Deploy OMAC core

## Technical Integration Points

### Backend Modifications
- `src/api/main.py`: Add lifecycle hooks for SPELWork
- `src/api/routes.py`: Transform endpoints to wish-based
- `src/api/search_index_manager.py`: Add Chroma vector DB
- New: `src/spelwork/` directory for governance modules

### Frontend Modifications
- Replace chat UI with Kurt-style authoring
- Add wish submission forms
- Create ritual visualization
- Implement trust score displays

### Infrastructure Additions
- Add Chroma vector database
- Configure Datasette for structured data
- Set up trustlog storage
- Implement backup strategies

## Toilville Philosophy Integration

### Core Principles
- "Mayor's Promise" - humility and respect for engineers
- Egoless rigor in all interactions
- Ruses create value
- Trust-based governance
- Progressive consent
- Ethical AI alignment

### Business Alignment
- Toilville LLC mission: Ethical AI consultancy
- Focus on automation with human dignity
- Structured workflows with accountability
- Trust-based governance systems

## Next Steps
1. Review and approve this integration plan
2. Set up development environment with SPELWork dependencies
3. Begin Phase 1 implementation
4. Create test scenarios for wish-based workflows
5. Develop evaluation metrics for trust scoring

## Notes
- Maintain compatibility with existing Azure AI Foundry features
- Ensure all changes are reversible/configurable
- Document all SPELWork additions thoroughly
- Create migration path for existing chat-based interactions