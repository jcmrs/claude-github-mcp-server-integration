# Repository Maintenance Checklist

## Purpose
Systematic verification that all project updates are captured in repository files. Prevents missed documentation and keeps repo current with conversation progress.

## When to Run This Checklist
- Before MILESTONE commands
- Before SAVE commands  
- At conversation handoff points
- When significant progress/changes occur
- When new concepts/problems are identified

## Core Maintenance Checks

### 1. Project State Updates
- [ ] **project-state.json** - Does current status match conversation progress?
- [ ] **CONVERSATION-INDEX.json** - Are priorities and next actions current?
- [ ] **Issue status** - Do GitHub issues reflect actual progress/completion?

### 2. Concept Documentation
- [ ] **FUTURE-CONCEPTS.md** - New concepts/problems/observations to document?
- [ ] **New issues needed** - Problems/features identified that need GitHub issues?
- [ ] **Lessons learned** - Technical discoveries to preserve for future conversations?

### 3. System Documentation  
- [ ] **HUMAN-INSTRUCTIONS.md** - New commands or workflow changes to document?
- [ ] **README updates** - Project description changes needed?
- [ ] **Documentation gaps** - Missing explanations for current functionality?

### 4. Conversation Continuity
- [ ] **Transcript current** - Latest save reflects important progress?
- [ ] **Handoff preparation** - Next conversation guidance clear and accurate?
- [ ] **Cross-references** - Links between issues/conversations properly maintained?

### 5. File Organization
- [ ] **New directories needed** - Project growth requiring new file structure?
- [ ] **File naming consistency** - All files following established conventions?
- [ ] **Cleanup needed** - Outdated or redundant files to remove/update?

## Repository Health Indicators

### ✅ Healthy Repository
- All project state files reflect current reality
- Issues match actual work status  
- Documentation covers existing functionality
- Future concepts captured systematically
- Clear handoff guidance for next conversations

### ⚠️ Repository Needs Attention
- Project state files outdated
- Completed work not reflected in issues
- New functionality undocumented
- Concepts/problems identified but not captured
- Unclear next steps for future conversations

### 🚨 Repository Out of Sync
- Major disconnects between conversation progress and repo state
- Critical concepts/problems not documented
- Issues don't reflect actual project status
- Missing essential documentation for handoffs
- Future conversations would be confused by repo state

## Implementation Integration

### Command System Integration
- **STATUS command** - Include repo maintenance health check
- **MILESTONE command** - Auto-trigger maintenance checklist  
- **SAVE command** - Verify repo updates before transcript save
- **New: REPO-CHECK command** - Run full maintenance checklist on demand

### Systematic Workflow
1. Work on development tasks
2. Identify significant progress/changes
3. Run maintenance checklist
4. Update necessary repository files
5. Continue with MILESTONE/SAVE as appropriate

## Maintenance Examples

### Example: New Concept Identified
**Trigger:** Conversation identifies LLM drift problem
**Actions:**
- [ ] Document in FUTURE-CONCEPTS.md ✅
- [ ] Consider if GitHub issue needed
- [ ] Update project priorities if critical
- [ ] Note in conversation transcript

### Example: Work Completion
**Trigger:** Issue #5 implementation complete  
**Actions:**
- [ ] Update issue with completion details ✅
- [ ] Update project-state.json with new status ✅
- [ ] Update CONVERSATION-INDEX.json priorities ✅
- [ ] Document achievements in transcript ✅

### Example: System Enhancement
**Trigger:** New command system functionality
**Actions:**
- [ ] Update HUMAN-INSTRUCTIONS.md with new commands ✅
- [ ] Update FUTURE-CONCEPTS.md if applicable
- [ ] Test and document new functionality
- [ ] Update conversation index with capability changes

## Quality Standards

### Documentation Quality
- Updates must be specific and actionable
- Avoid marketing language - use engineering terminology
- Include evidence/testing status for claims
- Maintain realistic scope assessment

### Maintenance Frequency
- Major milestones: Full checklist
- Regular progress: Quick status checks
- Problem identification: Immediate concept documentation
- Handoff preparation: Complete repository sync verification

---

**Meta Note:** This checklist itself demonstrates the concept - systematically identifying and documenting what needs repository maintenance rather than ad-hoc updates.