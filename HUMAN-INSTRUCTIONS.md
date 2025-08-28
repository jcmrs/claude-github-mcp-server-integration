# Human Commands for Claude.AI + GitHub Integration

## Transcript Management Commands

### Primary Commands
- **`SAVE`** - Triggers Claude to prepare current conversation transcript for immediate save to GitHub
- **`STATUS`** - Request current token usage, message length, and conversation health report
- **`MILESTONE`** - Mark important conversation point (Claude will note in transcript and consider for save)

### Development Commands (Expected to expand)
- **`UPDATE-INDEX`** - Triggers update to CONVERSATION-INDEX.json with current progress
- **`HANDOFF-PREP`** - Begin preparing conversation handoff documentation
- **`ARTIFACT-REPO`** - Move large artifacts from conversation to repository files

## When Claude Will Auto-Signal for Commands

### Automatic Triggers
- **Message approaching 8,000 characters** - Claude signals efficiency warning
- **Token usage getting high** - Claude requests STATUS check
- **Major milestone completed** - Claude suggests MILESTONE command
- **Artifacts getting too large** - Claude recommends ARTIFACT-REPO
- **Natural handoff point reached** - Claude suggests HANDOFF-PREP

### Claude Signal Format
When Claude needs action, it will use:
```
🚨 **HUMAN ACTION NEEDED:** [Command] - [Reason]
```

## Current Session Commands Available
✅ `SAVE` - Test transcript system  
✅ `STATUS` - Monitor conversation health  
✅ `MILESTONE` - Mark important points  
⚠️ `UPDATE-INDEX` - Not yet implemented  
⚠️ `HANDOFF-PREP` - Not yet implemented  
⚠️ `ARTIFACT-REPO` - Not yet implemented  

## Usage Notes
- Commands are case-insensitive
- Can be used mid-conversation at any point
- Claude maintains awareness of when commands are most useful
- New commands will be added during development and documented here

## Implementation Status
- **Current Phase:** Testing basic transcript system
- **Next Phase:** Expand command set based on development needs
- **Integration:** Commands work with existing handoff protocols