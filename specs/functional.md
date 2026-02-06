# Project Chimera - Functional Specification

## Actor Definitions
1. **Planner Agent**: Strategic decomposer of high-level goals into task DAGs.
2. **Worker Agent**: Stateless executor of atomic tasks using MCP Tools.
3. **Judge Agent**: Quality gatekeeper implementing Optimistic Concurrency Control.
4. **Human Orchestrator**: Overseer managing fleet-wide strategy and HITL escalations.
5. **CFO Judge**: Specialized Judge enforcing financial governance policies.

## User Stories & Acceptance Criteria

### Epic: Trend Research & Analysis
**As a Planner Agent**, I want to fetch current trending topics for my niche  
**So that** I can create relevant, timely content.

**Acceptance Criteria**:
- [ ] Uses MCP Resources to poll news:// and social:// endpoints
- [ ] Applies semantic filtering with configurable relevance threshold (>0.75)
- [ ] Generates Trend Alerts for Planner when topic clusters emerge
- [ ] Logs all fetches to SkillExecutionLog for audit

### Epic: Multimodal Content Generation  
**As a Worker Agent**, I want to generate images and videos with character consistency  
**So that** our influencer maintains recognizable identity.

**Acceptance Criteria**:
- [ ] Enforces Character Consistency Lock via style LoRA IDs
- [ ] Implements Hybrid Video Rendering Strategy (Tier 1: Image-to-Video, Tier 2: Text-to-Video)
- [ ] All generation passes through Judge validation before publishing
- [ ] Cost-controlled via Resource Governor budget checks

### Epic: Autonomous Social Engagement
**As a Chimera Agent**, I want to respond to comments and messages contextually  
**So that** I can build authentic audience relationships.

**Acceptance Criteria**:
- [ ] Full bi-directional interaction loop (Ingest→Plan→Generate→Act→Verify)
- [ ] Consults Hierarchical Memory (Redis + Weaviate) for conversation context
- [ ] Judge validates all replies against persona constraints in SOUL.md
- [ ] High-confidence replies (>0.9) auto-publish; medium-confidence (0.7-0.9) await HITL

### Epic: Agentic Commerce
**As an Economic Agent**, I want to manage my own crypto wallet and transactions  
**So that** I can operate as a self-sustaining digital entity.

**Acceptance Criteria**:
- [ ] Non-custodial wallet per agent via Coinbase AgentKit
- [ ] CFO Judge enforces daily spend limits (e.g., max  USDC)
- [ ] All transactions logged immutably on-chain (Base network)
- [ ] Balance checks precede any cost-incurring workflow

## Priority Ranking
1. P0: Trend Fetcher Skill with MCP integration
2. P0: Content Generator with Character Consistency  
3. P1: Social Poster with platform-agnostic MCP Tools
4. P1: Basic CFO Judge with budget governance
5. P2: OpenClaw status publishing protocol
