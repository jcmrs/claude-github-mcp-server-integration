# Human Commands for Claude.AI + GitHub Integration

## Transcript Management Commands

### Primary Commands
- **`SAVE`** - Triggers Claude to prepare current conversation transcript for immediate save to GitHub ✅ OPERATIONAL
- **`STATUS`** - Request current token usage, message length, and conversation health report ✅ OPERATIONAL  
- **`MILESTONE`** - Mark important conversation point (Claude will note in transcript and consider for save) ✅ OPERATIONAL

### Development Commands (Expanding Based on Need)
- **`UPDATE-INDEX`** - Triggers update to CONVERSATION-INDEX.json with current progress ✅ READY
- **`HANDOFF-PREP`** - Begin preparing conversation handoff documentation ✅ READY
- **`ARTIFACT-REPO`** - Move large artifacts from conversation to repository files ✅ READY
- **`ISSUE-UPDATE`** - Update specific GitHub issue with current progress ✅ READY
- **`PROJECT-STATE`** - Update project-state.json with current status ✅ READY
- **`REPO-CHECK`** - Run systematic repository maintenance checklist ✅ OPERATIONAL

### Advanced Commands (Future Expansion)
- **`CROSS-REF`** - Generate cross-references between conversations and issues ⚠️ PLANNED
- **`TEMPLATE-CREATE`** - Create new project template based on current work ⚠️ PLANNED  
- **`WORKFLOW-OPTIMIZE`** - Analyze and optimize conversation workflow ⚠️ PLANNED
- **`CONTEXT-SEARCH`** - Search across all conversation transcripts ⚠️ PLANNED

## When Claude Will Auto-Signal for Commands

### Automatic Triggers
- **Message approaching 8,000 characters** - Claude signals efficiency warning → Suggests `SAVE`
- **Token usage getting high** - Claude requests `STATUS` check
- **Major milestone completed** - Claude suggests `MILESTONE` command → **Auto-triggers `REPO-CHECK`**
- **Artifacts getting too large** - Claude recommends `ARTIFACT-REPO`
- **Natural handoff point reached** - Claude suggests `HANDOFF-PREP`
- **Issue progress significant** - Claude recommends `ISSUE-UPDATE`
- **Project state changed** - Claude suggests `PROJECT-STATE`
- **New concepts identified** - Claude auto-runs `REPO-CHECK` for documentation updates

### Claude Signal Format
When Claude needs action, it will use:
```
🚨 **HUMAN ACTION NEEDED:** [Command] - [Reason]
```

## Repository Maintenance Integration

### REPO-CHECK Command Details
**Purpose:** Systematic verification that repository files match conversation progress  
**Triggers:** Before MILESTONE, before SAVE, at handoff points, when significant changes occur  
**Process:** Claude runs through REPO-MAINTENANCE-CHECKLIST.md systematically  
**Output:** Reports what needs updating and executes necessary repository updates  

### Automatic Repository Maintenance
- **MILESTONE command** - Auto-triggers REPO-CHECK before marking milestone
- **SAVE command** - Verifies repository health before transcript save  
- **STATUS command** - Now includes repository maintenance health check
- **Concept identification** - Auto-documents new problems/ideas in FUTURE-CONCEPTS.md

### Repository Health Indicators in STATUS
✅ **Healthy:** All files current, issues match reality, documentation complete  
⚠️ **Attention Needed:** Some files outdated, minor gaps in documentation  
🚨 **Out of Sync:** Major disconnects between conversation and repository state  

## Current Session Commands Available
✅ `SAVE` - Transcript system fully operational  
✅ `STATUS` - Conversation health + repository maintenance monitoring  
✅ `MILESTONE` - Important point marking + automatic repo maintenance  
✅ `UPDATE-INDEX` - CONVERSATION-INDEX.json updates  
✅ `HANDOFF-PREP` - Conversation handoff preparation  
✅ `ARTIFACT-REPO` - Large file repository management  
✅ `ISSUE-UPDATE` - GitHub issue progress updates  
✅ `PROJECT-STATE` - Project state file maintenance  
✅ `REPO-CHECK` - Systematic repository maintenance verification  

## Command Usage Examples

### Basic Workflow
1. Work on tasks normally
2. When Claude signals or you want to save: `SAVE`
3. At completion points: `MILESTONE` (auto-runs REPO-CHECK)  
4. For status checks: `STATUS` (includes repo health)

### Development Workflow  
1. Complete significant work: `MILESTONE` (triggers repo maintenance)
2. Update project tracking: `UPDATE-INDEX` or `PROJECT-STATE`
3. Document progress: `ISSUE-UPDATE`
4. When ready to handoff: `HANDOFF-PREP`
5. Verify everything current: `REPO-CHECK`

### Repository Maintenance Workflow
1. Identify new concepts/problems: Auto-documented via REPO-CHECK
2. Complete major work: MILESTONE → REPO-CHECK → Updates
3. Before conversation end: REPO-CHECK → SAVE → Clean handoff

### File Management
1. Large artifacts getting unwieldy: `ARTIFACT-REPO`
2. Need clean conversation: `REPO-CHECK` → `SAVE` → start new conversation
3. Reference previous work: Claude auto-accesses transcripts

## Usage Notes
- Commands are case-insensitive
- Can be used mid-conversation at any point
- Claude maintains awareness of when commands are most useful
- **Repository maintenance now automatic** - Claude checks and updates systematically
- New commands added during development and documented here automatically
- Commands integrate with existing handoff protocols

## Implementation Status
- **Current Phase:** Repository maintenance system operational
- **Next Phase:** Advanced command testing and workflow optimization
- **Integration:** All commands work seamlessly with GitHub MCP and transcript system
- **Repository Health:** Systematic maintenance prevents documentation drift

## System Benefits
✅ **Complete project memory** - Full transcript access across conversations  
✅ **Human-friendly workflow** - Simple commands for complex operations  
✅ **Automated guidance** - Claude suggests optimal command usage  
✅ **Systematic maintenance** - Repository stays current automatically  
✅ **Flexible expansion** - New commands added based on development needs  
✅ **GitHub integration** - All operations sync with repository automatically  
✅ **Quality assurance** - Prevents missed documentation and file drift