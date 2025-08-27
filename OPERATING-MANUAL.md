# Claude.AI + GitHub MCP Integration: Complete Operating Manual

## For Humans: Simple Instructions

### When to Use This System
- **Complex projects** that exceed single conversation limits
- **Multi-session work** that needs to continue across different times  
- **Collaborative projects** where you want different Claude conversations to handle different aspects
- **Long-term projects** that build up knowledge over time

### Basic Workflow for Humans

#### Starting a New Project
1. **Create GitHub repository** (or use existing one)
2. **In Claude Desktop**, mention the repository name 
3. **Let Claude set up** the coordination structure
4. **Work normally** - Claude handles the GitHub integration

#### Continuing an Existing Project  
1. **Open Claude Desktop** (not web version!)
2. **Say:** "I need to continue working on [project name]. Please check the GitHub repository [repo-name] for current status."
3. **Let Claude read** the project state and continue
4. **Work normally** - Claude updates progress automatically

#### When to Start a New Conversation
- Current conversation getting slow/long (8000+ words)
- Switching focus areas (development → testing → documentation)  
- Need fresh context window for complex tasks
- Conversation becomes unfocused or cluttered

### What Happens Automatically
- ✅ Claude reads your project progress
- ✅ Claude understands what's been done
- ✅ Claude continues from where you left off
- ✅ Claude updates project status as work progresses
- ✅ All progress is saved to GitHub repository

### What You DON'T Need to Do
- ❌ Explain previous conversations to new Claude sessions
- ❌ Manually copy/paste information between conversations
- ❌ Re-explain project context or requirements
- ❌ Remember exactly where you left off

## For Claude Conversations: Technical Protocols

### Conversation Startup Protocol

#### 1. Project Recognition
When user mentions existing project or repository:
```
"I need to continue working on [project]. Please check repository [repo-name]."
```

**IMMEDIATE ACTIONS:**
1. Use `github:get_file_contents` to read `conversation-handoffs/project-state.json`
2. Use `github:get_file_contents` to read `conversation-handoffs/conversation-index.md`  
3. Use `github:list_issues` to check active issues

#### 2. Context Reconstruction
Based on project state file:
- **Identify current phase** from project-state.json
- **Configure appropriate expertise** based on project needs
- **Understand completed vs pending tasks**
- **Recognize any blockers or priorities**

#### 3. Conversation Registration
```json
// Add to conversation-index.md
### YYYY-MM-DD-HH-MM_focus-area_conv-XXX
- **Status:** ACTIVE
- **Focus:** [Brief description]
- **Previous conversation:** [reference if continuing]
- **Started:** [timestamp]
```

### During Conversation Protocol

#### State Updates
**After completing any task:**
1. Update `project-state.json` with completed tasks
2. Add new pending tasks if discovered
3. Update current phase if changed
4. Document key decisions in issues/comments

#### Progress Tracking
**For significant milestones:**
1. Create or update GitHub issues with progress
2. Tag issues with conversation ID for traceability
3. Document technical decisions in repository files
4. Update project timeline if needed

### Conversation Handoff Protocol  

#### Before Ending Conversation
**MANDATORY STEPS:**
1. **Update project-state.json:**
   ```json
   {
     "current_state": {
       "last_updated": "2025-08-27T19:XX:00Z",
       "active_conversation": "completed",
       "next_priority": "[what should happen next]",
       "handoff_notes": "[context for next conversation]"
     }
   }
   ```

2. **Create handoff summary:**
   - What was accomplished this session
   - What was learned/discovered  
   - What should happen next
   - Any blockers or important notes

3. **Update conversation index:**
   - Mark conversation as COMPLETE
   - Add key outcomes
   - Reference next recommended focus

#### Handoff Quality Checklist
- [ ] Project state updated with current status
- [ ] All completed tasks documented
- [ ] Next priorities clearly identified  
- [ ] Any blockers or issues noted
- [ ] Key decisions documented in appropriate files
- [ ] Repository files updated if code/content was created

### Error Recovery Protocol

#### If Project State is Missing/Corrupted
1. Check repository for README, issues, recent commits
2. Reconstruct basic project status from available evidence
3. Ask human to clarify current priorities
4. Rebuild project-state.json from available information
5. Document the recovery in project notes

#### If GitHub Access Fails
1. Verify this is Claude Desktop (not web)
2. Check if GitHub tools are enabled in Tools menu
3. Ask human to verify Docker Desktop is running
4. If persistent failure, document issue and suggest manual handoff

### File Structure Standards

```
repository-root/
├── README.md (project overview)
├── conversation-handoffs/
│   ├── README.md (protocol documentation)
│   ├── project-state.json (current status)
│   ├── conversation-index.md (conversation tracking)
│   └── conversation-history/ (archived summaries)
├── project-docs/ (main project documentation)
├── artifacts/ (code, documents, outputs)
└── issues/ (GitHub issues for tracking)
```

### Automation Guidelines

#### Smart Context Loading
- Always read project-state.json first
- Prioritize recent issues and commits for context
- Focus on pending tasks matching expertise
- Identify conversation handoff patterns

#### Efficient Updates  
- Batch GitHub operations when possible
- Use meaningful commit messages with conversation IDs
- Update project state incrementally, not wholesale rewrites
- Tag related issues and PRs for cross-referencing

## Emergency Protocols

### If Human Reports "Lost Context"
1. **Immediately read full project state** from GitHub
2. **Ask targeted questions** about current priorities
3. **Reconstruct context** from repository evidence
4. **Update project state** with recovered information

### If Conversations Become Inconsistent
1. **Review conversation-index.md** for overlap/conflicts
2. **Check project-state.json** for last known good state
3. **Ask human to clarify** current priorities
4. **Create reconciliation summary** documenting what happened

This system transforms GitHub repositories into persistent memory for Claude conversations, enabling complex projects to span multiple sessions without context loss.