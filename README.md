# Claude.AI + GitHub MCP Server Integration Project

## What This Project Is
This project establishes a complete coordination system between Claude.AI conversations and GitHub repositories, enabling persistent project memory and seamless multi-conversation workflows that transcend individual conversation token limits.

## For New Conversations: START HERE 🎯

### Step 1: Read the Conversation Index
**IMMEDIATELY go to:** `conversation-handoffs/CONVERSATION-INDEX.json`
This file tells you:
- What work is currently active
- Which conversation you should be (Setup Core v2, Development API v1, etc.)
- What your immediate priority is
- Which files to read for context

### Step 2: Check Project State
**Read:** `conversation-handoffs/project-state.json`
- Current project status
- Completed vs pending tasks
- Any blockers or urgent priorities

### Step 3: Review Active Issues
**Check:** GitHub Issues #1-#5 for current priorities and discussions

### Step 4: Continue the Work
Based on the conversation index:
- Take on the role specified (e.g., "Setup Core v2")  
- Focus on the priority task listed
- Update the index when you complete work

## Core System Components
- **GitHub MCP Server** - Enables Claude ↔ GitHub integration
- **Project State Management** - Persistent project memory via JSON files
- **Conversation Coordination** - Cross-conversation referencing and versioning
- **Human-Friendly Interface** - Simple conversation types and workflows

## Current Status
**Foundation Complete** - All infrastructure established, now implementing full conversation transcript mirroring for complete context preservation.

## Repository Structure
```
├── CONVERSATION-INDEX.json          ← START HERE for new conversations
├── conversation-handoffs/
│   ├── project-state.json          ← Current project status  
│   ├── CONVERSATION-TYPES.md       ← Human-friendly conversation system
│   └── conversation-history/       ← Handoff summaries
├── conversation-transcripts/        ← Full conversation records
├── OPERATING-MANUAL.md             ← Complete system documentation
└── FUTURE-CONCEPTS.md              ← Strategic development concepts
```

## Success Metrics
✅ Persistent project memory across unlimited conversations
✅ No context loss between conversation sessions  
✅ Human-friendly project coordination
✅ Scalable to complex, long-term projects

---
**New conversations: Go read CONVERSATION-INDEX.json immediately to understand where to pick up!**