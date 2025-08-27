# Cross-Conversation State Management

## Purpose
This directory manages state, context, and handoffs between multiple Claude conversations working on the same project.

## Structure
- `active-conversations/` - Current conversation states and contexts
- `conversation-history/` - Archived conversation summaries and outcomes  
- `shared-knowledge/` - Project knowledge base accessible to all conversations
- `project-state.json` - Current project status, next steps, blockers
- `conversation-index.md` - Master index of all conversations and their focus areas

## Naming Convention
Conversations should use format: `YYYY-MM-DD-HH-MM_focus-area_conversation-id`

Example: `2025-08-27-19-15_integration-testing_conv-001`

## State Handoff Protocol
1. Before ending conversation: Update project-state.json
2. Document key decisions in shared-knowledge/
3. Create handoff entry in conversation-index.md
4. Tag relevant issues with conversation outcomes
