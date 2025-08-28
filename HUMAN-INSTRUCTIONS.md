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

### Advanced Commands (Future Expansion)
- **`CROSS-REF`** - Generate cross-references between conversations and issues ⚠️ PLANNED
- **`TEMPLATE-CREATE`** - Create new project template based on current work ⚠️ PLANNED  
- **`WORKFLOW-OPTIMIZE`** - Analyze and optimize conversation workflow ⚠️ PLANNED
- **`CONTEXT-SEARCH`** - Search across all conversation transcripts ⚠️ PLANNED

## When Claude Will Auto-Signal for Commands

### Automatic Triggers
- **Message approaching 8,000 characters** - Claude signals efficiency warning → Suggests `SAVE`
- **Token usage getting high** - Claude requests `STATUS` check
- **Major milestone completed** - Claude suggests `MILESTONE` command
- **Artifacts getting too large** - Claude recommends `ARTIFACT-REPO`
- **Natural handoff point reached** - Claude suggests `HANDOFF-PREP`
- **Issue progress significant** - Claude recommends `ISSUE-UPDATE`
- **Project state changed** - Claude suggests `PROJECT-STATE`

### Claude Signal Format
When Claude needs action, it will use:
```
🚨 **HUMAN ACTION NEEDED:** [Command] - [Reason]
```

## Current Session Commands Available
✅ `SAVE` - Transcript system fully operational  
✅ `STATUS` - Conversation health monitoring  
✅ `MILESTONE` - Important point marking  
✅ `UPDATE-INDEX` - CONVERSATION-INDEX.json updates  
✅ `HANDOFF-PREP` - Conversation handoff preparation  
✅ `ARTIFACT-REPO` - Large file repository management  
✅ `ISSUE-UPDATE` - GitHub issue progress updates  
✅ `PROJECT-STATE` - Project state file maintenance  

## Command Usage Examples

### Basic Workflow
1. Work on tasks normally
2. When Claude signals or you want to save: `SAVE`
3. At completion points: `MILESTONE`  
4. For status checks: `STATUS`

### Development Workflow  
1. Complete significant work: `MILESTONE`
2. Update project tracking: `UPDATE-INDEX` or `PROJECT-STATE`
3. Document progress: `ISSUE-UPDATE`
4. When ready to handoff: `HANDOFF-PREP`

### File Management
1. Large artifacts getting unwieldy: `ARTIFACT-REPO`
2. Need clean conversation: `SAVE` then start new conversation
3. Reference previous work: Claude auto-accesses transcripts

## Usage Notes
- Commands are case-insensitive
- Can be used mid-conversation at any point
- Claude maintains awareness of when commands are most useful
- New commands added during development and documented here automatically
- Commands integrate with existing handoff protocols

## Implementation Status
- **Current Phase:** Core command system operational - Issue #5 complete
- **Next Phase:** Advanced command testing and workflow optimization
- **Integration:** All commands work seamlessly with GitHub MCP and transcript system

## System Benefits
✅ **Complete project memory** - Full transcript access across conversations  
✅ **Human-friendly workflow** - Simple commands for complex operations  
✅ **Automated guidance** - Claude suggests optimal command usage  
✅ **Flexible expansion** - New commands added based on development needs  
✅ **GitHub integration** - All operations sync with repository automatically