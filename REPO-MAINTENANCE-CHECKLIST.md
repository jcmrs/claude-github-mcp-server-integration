# Repository Maintenance Checklist

## Purpose
Systematic verification that all project updates are captured in repository files. Prevents missed documentation, ensures pattern consistency, and keeps repo current with conversation progress.

## When to Run This Checklist
- Before MILESTONE commands
- Before SAVE commands  
- At conversation handoff points
- When significant progress/changes occur
- When new concepts/problems are identified
- **Before creating new files or directories**

## Critical Pattern Verification (Added 2025-08-28 - Issue #8)

### Pattern Verification Requirements
- [ ] **Check existing patterns** - Use tools to verify directory contents and file formats before creating new content
- [ ] **Repository convention compliance** - Follow established naming and format conventions (e.g., handoffs are markdown, not JSON)
- [ ] **Evidence-based decisions** - Verify assumptions with actual repository data before making format choices
- [ ] **Document deviations** - If choosing different pattern, explicitly justify the change

### Pattern Consistency Checks
- [ ] **File naming consistency** - All files following established repository conventions?
- [ ] **Directory patterns** - New files placed in directories consistent with similar content?
- [ ] **Format consistency** - File formats match established patterns (handoffs = markdown, data = JSON, etc.)?
- [ ] **Convention compliance** - Repository patterns maintained across all conversations?

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
- [ ] **Pattern verification complete** - All new files follow repository conventions?
- [ ] **Cleanup needed** - Outdated or redundant files to remove/update?

## Repository Health Indicators

### ✅ Healthy Repository
- All project state files reflect current reality
- Issues match actual work status  
- Documentation covers existing functionality
- Future concepts captured systematically
- Clear handoff guidance for next conversations
- **All files follow established repository patterns**
- **Pattern consistency maintained across conversations**

### ⚠️ Repository Needs Attention
- Project state files outdated
- Completed work not reflected in issues
- New functionality undocumented
- Concepts/problems identified but not captured
- Unclear next steps for future conversations
- **Minor pattern deviations or inconsistencies**

### 🚨 Repository Out of Sync
- Major disconnects between conversation progress and repo state
- Critical concepts/problems not documented
- Issues don't reflect actual project status
- Missing essential documentation for handoffs
- Future conversations would be confused by repo state
- **Pattern violations requiring correction**
- **Repository conventions not followed**

## Implementation Integration

### Command System Integration
- **STATUS command** - Include repo maintenance health check
- **MILESTONE command** - Auto-trigger maintenance checklist  
- **SAVE command** - Verify repo updates before transcript save
- **REPO-CHECK command** - Run full maintenance checklist on demand

### Systematic Workflow
1. **Verify patterns** - Check existing repository patterns before creating new content
2. Work on development tasks
3. Identify significant progress/changes
4. Run maintenance checklist
5. Update necessary repository files
6. Continue with MILESTONE/SAVE as appropriate

## Pattern Verification Protocol

### Before Creating New Files
1. **Check directory contents** - Use `github:get_file_contents` to see existing files
2. **Identify patterns** - Note naming conventions, file formats, content structure
3. **Follow conventions** - Match established patterns unless explicitly changing them
4. **Document changes** - If deviating from pattern, explain reasoning

### Common Pattern Examples
- **Handoff documents:** `[Name]-FINAL-HANDOFF.md` (markdown format)
- **Transcripts:** `[Name]-TRANSCRIPT.md` (markdown format)  
- **Data files:** `[name].json` (JSON format for structured data)
- **Documentation:** `[NAME].md` (markdown for human-readable docs)

## Maintenance Examples

### Example: Pattern Verification Success
**Trigger:** Need to create handoff document
**Actions:**
- [ ] Check conversation-handoffs/conversation-history/ directory ✅
- [ ] Verify existing handoffs are markdown format ✅
- [ ] Create `Setup-Core-v2-FINAL-HANDOFF.md` following pattern ✅
- [ ] Maintain repository convention consistency ✅

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

### Pattern Consistency
- **Evidence-based pattern verification required**
- **Repository conventions take priority over individual preferences**
- **Pattern changes must be explicitly justified**
- **Systematic verification prevents assumption-based mistakes**

### Maintenance Frequency
- Major milestones: Full checklist including pattern verification
- Regular progress: Quick status checks
- Problem identification: Immediate concept documentation
- Handoff preparation: Complete repository sync verification
- **New file creation: Mandatory pattern verification**

---

**Meta Note:** This checklist demonstrates systematic maintenance including pattern verification requirements based on Issue #8 lesson learned. Pattern consistency prevents repository convention violations and maintains systematic organization.