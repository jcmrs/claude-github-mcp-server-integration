# Human Commands for Claude.AI + GitHub Integration

## Transcript Management Commands

### Primary Commands
- **`SAVE`** - Triggers Claude to prepare current conversation transcript for immediate save to GitHub ✅ OPERATIONAL
- **`STATUS`** - Request current token usage, message length, conversation health, and development command recommendations ✅ OPERATIONAL  
- **`MILESTONE`** - Mark important conversation point (Claude will note in transcript and consider for save) ✅ OPERATIONAL

### Development Commands (Expanding Based on Need)
- **`UPDATE-INDEX`** - Triggers update to CONVERSATION-INDEX.json with current progress ✅ READY
- **`HANDOFF-PREP`** - Begin preparing conversation handoff documentation ✅ READY
- **`ARTIFACT-REPO`** - Move large artifacts from conversation to repository files ✅ READY
- **`ISSUE-UPDATE`** - Update specific GitHub issue with current progress ✅ READY
- **`PROJECT-STATE`** - Update project-state.json with current status ✅ READY
- **`REPO-CHECK`** - Run systematic repository maintenance checklist ✅ OPERATIONAL
- **`READ`** - Access specific conversation transcripts or project files ✅ READY

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

## Enhanced STATUS Command Output

### STATUS Command Now Provides
**Conversation Health:**
- Current message length and token usage
- Conversation efficiency assessment
- Context window utilization

**Repository Maintenance Status:**
- ✅ **Healthy** - All files current, documentation complete
- ⚠️ **Attention** - Minor updates needed
- 🚨 **Out of Sync** - Major repository maintenance required

**Development Command Recommendations:**
- **UPDATE-INDEX recommended** when conversation priorities have shifted significantly
- **PROJECT-STATE recommended** when major progress achieved but not yet documented
- **ISSUE-UPDATE recommended** when substantial work completed on tracked issues
- **HANDOFF-PREP recommended** when conversation approaching natural ending point
- **ARTIFACT-REPO recommended** when large content created that should be in repository
- **REPO-CHECK recommended** when significant changes made since last maintenance

**Next Action Suggestions:**
- Immediate priorities based on conversation progress
- Optimal next commands based on current status
- Warning about approaching conversation limits

## READ Command Implementation

### READ Command Usage
- **`READ Setup-Core-v1`** - Access complete transcript from Setup Core v1 conversation
- **`READ Setup-Core-v2`** - Access current conversation full context
- **`READ project-state`** - Current project status summary from project-state.json
- **`READ conversation-index`** - Master coordination file (CONVERSATION-INDEX.json)
- **`READ issue-5`** - Specific GitHub issue details and comments
- **`READ future-concepts`** - Development concepts and planning notes

### READ Command Benefits
- **Systematic access** to historical conversation details
- **Context retrieval** for cross-conversation references
- **Distinction** between summary data and complete transcripts
- **Human-friendly naming** instead of complex file paths

## Repository Maintenance Integration

### REPO-CHECK Command Details
**Purpose:** Systematic verification that repository files match conversation progress  
**Triggers:** Before MILESTONE, before SAVE, at handoff points, when significant changes occur  
**Process:** Claude runs through REPO-MAINTENANCE-CHECKLIST.md systematically  
**Output:** Reports what needs updating and executes necessary repository updates  

### Automatic Repository Maintenance
- **MILESTONE command** - Auto-triggers REPO-CHECK before marking milestone
- **SAVE command** - Verifies repository health before transcript save  
- **STATUS command** - Now includes repository maintenance health check AND development command guidance
- **Concept identification** - Auto-documents new problems/ideas in FUTURE-CONCEPTS.md

### Development Command Guidance from STATUS

**When STATUS recommends specific development commands:**

**UPDATE-INDEX Recommended When:**
- Conversation priorities have changed significantly
- New issues created or existing issues resolved
- Phase transitions (Setup → Development → Planning)
- Major milestones achieved that affect project coordination

**PROJECT-STATE Recommended When:**
- Major achievements completed but not documented in project-state.json
- System capabilities enhanced (new commands, features)
- Infrastructure milestones reached
- Technology stack or approach changes

**ISSUE-UPDATE Recommended When:**
- Substantial progress made on tracked GitHub issues
- Issues resolved or status changed significantly
- New technical findings that affect issue scope
- Implementation approaches validated or changed

**HANDOFF-PREP Recommended When:**
- Conversation approaching 70-80% of typical limit
- Natural completion point reached for current phase
- Major phase transition imminent
- Significant achievements that warrant clean handoff

**ARTIFACT-REPO Recommended When:**
- Large documents or code created in conversation
- Content that should be preserved in repository structure
- Templates or reusable materials developed
- Documentation that exceeds conversation artifact limits

### Specialized Development Conversations

**Simple Implementation Available:**
Create dedicated "Development Maintenance" conversation for executing development commands without consuming tokens in working conversations.

**Benefits:**
- Token efficiency for maintenance operations
- Specialized context for development command execution
- Separation of concerns between development work and project maintenance

**Usage Pattern:**
1. Main conversation focuses on development work
2. STATUS command recommends development commands
3. Human creates "Development Maintenance" conversation
4. Execute development commands in specialized conversation
5. Return to main conversation for continued development

## Current Session Commands Available
✅ `SAVE` - Transcript system fully operational  
✅ `STATUS` - Conversation health + repository maintenance + development command guidance  
✅ `MILESTONE` - Important point marking + automatic repo maintenance  
✅ `UPDATE-INDEX` - CONVERSATION-INDEX.json updates  
✅ `HANDOFF-PREP` - Conversation handoff preparation  
✅ `ARTIFACT-REPO` - Large file repository management  
✅ `ISSUE-UPDATE` - GitHub issue progress updates  
✅ `PROJECT-STATE` - Project state file maintenance  
✅ `REPO-CHECK` - Systematic repository maintenance verification  
✅ `READ` - Access specific transcripts and project files  

## Command Usage Examples

### Basic Workflow
1. Work on tasks normally
2. Use `STATUS` to check health and get development command recommendations
3. When Claude signals or STATUS recommends: Execute suggested commands
4. At completion points: `MILESTONE` (triggers repo maintenance)
5. For important preservation: `SAVE`

### Enhanced Development Workflow  
1. Complete significant work: `STATUS` to check recommendations
2. Execute recommended development commands: `UPDATE-INDEX`, `PROJECT-STATE`, `ISSUE-UPDATE`
3. Mark achievements: `MILESTONE` (triggers automatic repo maintenance)
4. Access historical context: `READ Setup-Core-v1` for previous conversation details
5. When ready to handoff: `HANDOFF-PREP` → `SAVE`

### Specialized Conversation Pattern
1. Main conversation: Focus on development work
2. `STATUS` recommends development commands
3. Create "Development Maintenance" conversation
4. Execute: `UPDATE-INDEX`, `PROJECT-STATE`, `ISSUE-UPDATE`, `REPO-CHECK`
5. Return to main conversation with clean repository state

### Repository Maintenance Workflow
1. `STATUS` shows repository health and command recommendations
2. Execute recommended commands based on STATUS guidance
3. `REPO-CHECK` verifies all updates complete
4. `MILESTONE` to mark maintenance completion
5. `SAVE` to preserve maintenance work

### Cross-Conversation Reference Workflow
1. `READ Setup-Core-v1` to access previous conversation details
2. `READ project-state` to understand current status
3. `READ issue-5` to review specific issue context
4. Continue work with complete historical context
5. `UPDATE-INDEX` to reflect cross-conversation insights

## Usage Notes
- Commands are case-insensitive
- Can be used mid-conversation at any point
- **STATUS command now provides specific development command guidance**
- **READ command enables systematic access to historical context**
- Repository maintenance now automatic with development command recommendations
- Specialized conversations available for token-efficient maintenance operations
- Commands integrate with existing handoff protocols

## Implementation Status
- **Current Phase:** Enhanced command system with development guidance and READ capability
- **Next Phase:** Command chaining implementation and specialized conversation testing
- **Integration:** All commands work seamlessly with GitHub MCP and transcript system
- **Repository Health:** Systematic maintenance with intelligent command recommendations

## System Benefits
✅ **Complete project memory** - Full transcript access with READ command  
✅ **Intelligent workflow guidance** - STATUS provides specific command recommendations  
✅ **Human-friendly operations** - Simple commands for complex project management  
✅ **Token efficiency options** - Specialized conversations for development commands  
✅ **Systematic maintenance** - Repository stays current automatically  
✅ **Cross-conversation continuity** - READ command enables historical context access  
✅ **Flexible workflow patterns** - Multiple approaches for different project needs  
✅ **GitHub integration** - All operations sync with repository automatically