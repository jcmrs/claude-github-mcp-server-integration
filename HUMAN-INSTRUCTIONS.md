# Human Commands for Claude.AI + GitHub Integration

## Essential Commands

### Core Information Commands
- **`LIST`** - Display all available commands with current status and brief descriptions ✅ OPERATIONAL
- **`STATUS`** - Request current token usage, message length, conversation health, and development command recommendations ✅ OPERATIONAL  
- **`HELP [command]`** - Get detailed help for specific command (e.g., HELP STATUS) ✅ OPERATIONAL

### Primary Commands
- **`SAVE`** - Triggers Claude to create complete conversation transcript AND update JSON coordination files ✅ ENHANCED
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

## Enhanced SAVE Command

### SAVE Command Now Performs:
1. **Complete Conversation Transcript Creation** - Full markdown transcript with all exchanges
2. **JSON Coordination File Updates** - Updates CONVERSATION-INDEX.json and project-state.json  
3. **Repository Health Verification** - Runs REPO-CHECK before saving
4. **Contextual Preservation** - Captures decision rationale and conversational nuance

### Why This Enhancement Matters:
**Problem Solved:** JSON summaries lose contextual details and decision-making rationale that future conversations need for continuity.

**Solution:** SAVE now creates both detailed transcripts AND coordinating JSON files, ensuring complete contextual preservation.

### SAVE Command Process:
```
🚨 SAVE Command Initiated
├── 1. Repository health check (REPO-CHECK)
├── 2. Create complete markdown transcript
├── 3. Update JSON coordination files
├── 4. Verify all saves successful
└── ✅ Complete contextual preservation achieved
```

## LIST Command Output

### When you type `LIST`, Claude provides:

```
📋 **AVAILABLE COMMANDS**

**Essential:**
• LIST - Show all commands (you just used this!)
• STATUS - Health check + development command recommendations  
• HELP [command] - Detailed help for specific command

**Primary Workflow:**
• SAVE - Complete transcript + JSON updates to repository
• MILESTONE - Mark important progress + auto repository maintenance

**Development Commands:**
• UPDATE-INDEX - Update conversation coordination
• PROJECT-STATE - Update project status files  
• ISSUE-UPDATE - Update GitHub issues with progress
• HANDOFF-PREP - Prepare conversation handoff
• ARTIFACT-REPO - Move large content to repository
• REPO-CHECK - Systematic repository maintenance

**Context Access:**
• READ [target] - Access transcripts/files (e.g., READ Setup-Core-v1)

**Status:** ✅ Ready  ⚠️ Planned  🔧 In Development

Type HELP [command] for detailed usage (e.g., HELP STATUS)
```

## Specialized Conversation Setup

### Dev Commands Conversation - Simple Setup

**Recommended Name:** "Dev Commands v1" (simple, clear, versioned)

**When to Create:**
1. **Project Start Checklist** - Recommended as part of initial setup
2. **MILESTONE Prompts** - When development commands accumulate
3. **STATUS Recommendations** - When main conversation gets command-heavy

### Creating Dev Commands Conversation

**Step 1:** Create new conversation named "Dev Commands v1"

**Step 2:** Use this conversation starter text:
```
You are the Dev Commands specialist for the Claude.AI + GitHub project jcmrs/claude-github-mcp-server-integration.

ROLE: Execute development commands (UPDATE-INDEX, PROJECT-STATE, ISSUE-UPDATE, REPO-CHECK, HANDOFF-PREP) efficiently without consuming tokens from main development conversations.

SETUP INSTRUCTIONS:
1. Read CONVERSATION-INDEX.json immediately
2. Read conversation-handoffs/project-state.json  
3. Review HUMAN-INSTRUCTIONS.md for command details
4. Execute commands as requested by human
5. Report completion status back

SCOPE: Development command execution, repository maintenance, project coordination updates.

CONVERSATION TYPE: Dev Commands v1
PURPOSE: Token-efficient specialized maintenance operations

Ready to execute development commands for the project.
```

**Step 3:** Confirm Claude understands its specialized role

### Integration with Main Conversations

**MILESTONE Auto-Prompt:**
```
🔧 **DEVELOPMENT COMMANDS RECOMMENDATION**
Consider using "Dev Commands v1" conversation for:
• UPDATE-INDEX (project priorities changed)  
• PROJECT-STATE (major achievements to document)
• ISSUE-UPDATE (progress on GitHub issues)

This keeps main conversation focused on development work.
```

**STATUS Command Enhancement:**
Now includes "Dev Commands conversation recommended" when appropriate.

## When Claude Will Auto-Signal for Commands

### Automatic Triggers
- **Message approaching 8,000 characters** - Claude signals efficiency warning → Suggests `SAVE`
- **Token usage getting high** - Claude requests `STATUS` check
- **Major milestone completed** - Claude suggests `MILESTONE` command → **Auto-triggers `REPO-CHECK`** → **Recommends Dev Commands conversation**
- **Artifacts getting too large** - Claude recommends `ARTIFACT-REPO`
- **Natural handoff point reached** - Claude suggests `HANDOFF-PREP`
- **Issue progress significant** - Claude recommends `ISSUE-UPDATE` (via Dev Commands conversation)
- **Project state changed** - Claude suggests `PROJECT-STATE` (via Dev Commands conversation)
- **New concepts identified** - Claude auto-runs `REPO-CHECK` for documentation updates
- **Development commands accumulating** - Claude recommends "Dev Commands v1" conversation

### Claude Signal Format
When Claude needs action, it will use:
```
🚨 **HUMAN ACTION NEEDED:** [Command] - [Reason]
🔧 **DEV COMMANDS RECOMMENDED:** Use "Dev Commands v1" conversation for: [specific commands]
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

**Specialized Conversation Recommendations:**
- **"Dev Commands v1" recommended** when multiple development commands needed
- **Token efficiency suggestion** when main conversation getting command-heavy
- **Setup guidance** if Dev Commands conversation doesn't exist

**Next Action Suggestions:**
- Immediate priorities based on conversation progress
- Optimal next commands based on current status
- Warning about approaching conversation limits
- Dev Commands conversation usage recommendations

## HELP Command Implementation

### HELP Command Usage
- **`HELP`** - General command system overview
- **`HELP LIST`** - How to use LIST command
- **`HELP STATUS`** - Detailed STATUS command capabilities
- **`HELP READ`** - READ command syntax and examples
- **`HELP MILESTONE`** - MILESTONE command workflow and auto-triggers
- **`HELP SAVE`** - Enhanced SAVE command with transcript creation details

### HELP Command Benefits
- **Quick reference** without reading full documentation
- **Context-specific guidance** for each command
- **Usage examples** for complex commands
- **Integration information** showing how commands work together

## READ Command Implementation

### READ Command Usage
- **`READ Setup-Core-v1`** - Access complete transcript from Setup Core v1 conversation
- **`READ Setup-Core-v2`** - Access Setup Core v2 full transcript
- **`READ Setup-Core-v3`** - Access Setup Core v3 complete context (when available)
- **`READ project-state`** - Current project status summary from project-state.json
- **`READ conversation-index`** - Master coordination file (CONVERSATION-INDEX.json)
- **`READ issue-5`** - Specific GitHub issue details and comments
- **`READ future-concepts`** - Development concepts and planning notes

### READ Command Benefits
- **Complete contextual access** to all conversation details and decision rationale
- **Context retrieval** for cross-conversation references with full conversational nuance
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
- **SAVE command** - Verifies repository health AND creates complete transcripts AND updates JSON files
- **STATUS command** - Now includes repository maintenance health check AND development command guidance AND specialized conversation recommendations
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

### Specialized Dev Commands Conversation

**When STATUS Recommends Dev Commands Conversation:**
- Multiple development commands needed simultaneously
- Main conversation token usage approaching efficiency limits
- Regular maintenance operations accumulating
- Repository maintenance tasks piling up

**Benefits:**
- Token efficiency for maintenance operations
- Specialized context for development command execution
- Separation of concerns between development work and project maintenance
- Focused execution environment for repository operations

**Usage Pattern:**
1. Main conversation focuses on development work
2. STATUS command recommends development commands + Dev Commands conversation
3. Human creates or switches to "Dev Commands v1" conversation
4. Execute development commands in specialized conversation
5. Return to main conversation for continued development

## Current Session Commands Available
✅ `LIST` - Complete command reference with status indicators  
✅ `HELP [command]` - Detailed command help and usage examples  
✅ `SAVE` - Enhanced: Complete transcript creation + JSON coordination file updates  
✅ `STATUS` - Conversation health + repository maintenance + development command guidance + specialized conversation recommendations  
✅ `MILESTONE` - Important point marking + automatic repo maintenance + Dev Commands conversation prompts  
✅ `UPDATE-INDEX` - CONVERSATION-INDEX.json updates (recommend via Dev Commands conversation)  
✅ `HANDOFF-PREP` - Conversation handoff preparation  
✅ `ARTIFACT-REPO` - Large file repository management  
✅ `ISSUE-UPDATE` - GitHub issue progress updates (recommend via Dev Commands conversation)  
✅ `PROJECT-STATE` - Project state file maintenance (recommend via Dev Commands conversation)  
✅ `REPO-CHECK` - Systematic repository maintenance verification  
✅ `READ` - Access specific transcripts and project files  

## Command Usage Examples

### Getting Started
1. New to the system: `LIST` to see all available commands
2. Need help with specific command: `HELP STATUS` for detailed guidance
3. Check system health: `STATUS` for comprehensive assessment
4. Access historical context: `READ Setup-Core-v1` for complete previous conversation

### Basic Workflow
1. Work on tasks normally
2. Use `STATUS` to check health and get development command recommendations
3. When Claude signals or STATUS recommends: Execute suggested commands
4. At completion points: `MILESTONE` (triggers repo maintenance + Dev Commands recommendations)
5. For complete preservation: `SAVE` (creates full transcript + updates coordination)

### Enhanced Development Workflow  
1. Complete significant work: `STATUS` to check recommendations
2. If multiple dev commands needed: Create/use "Dev Commands v1" conversation
3. Execute recommended development commands in specialized conversation
4. Mark achievements in main conversation: `MILESTONE` 
5. Access complete historical context as needed: `READ [target]`
6. When ready to handoff: `HANDOFF-PREP` → `SAVE` (preserves complete context)

### Specialized Conversation Pattern
1. Main conversation: Focus on development work
2. `STATUS` recommends development commands + specialized conversation
3. Create "Dev Commands v1" conversation with provided starter text
4. Execute: `UPDATE-INDEX`, `PROJECT-STATE`, `ISSUE-UPDATE`, `REPO-CHECK`
5. Return to main conversation with clean repository state

### Repository Maintenance Workflow
1. `STATUS` shows repository health and command recommendations
2. Execute recommended commands (main conversation or Dev Commands conversation)
3. `REPO-CHECK` verifies all updates complete
4. `MILESTONE` to mark maintenance completion
5. `SAVE` to preserve complete maintenance work with full context

### Cross-Conversation Reference Workflow
1. `READ Setup-Core-v1` to access complete previous conversation details
2. `READ project-state` to understand current status summary
3. `READ issue-5` to review specific issue context
4. Continue work with complete historical context including decision rationale
5. `UPDATE-INDEX` to reflect cross-conversation insights

## Usage Notes
- Commands are case-insensitive
- Can be used mid-conversation at any point
- **LIST and HELP commands provide immediate guidance without documentation lookup**
- **STATUS command now provides specialized conversation recommendations**
- **READ command enables systematic access to complete historical context**
- **SAVE command now preserves complete conversational context, not just summaries**
- Repository maintenance now automatic with development command recommendations
- Dev Commands specialized conversation available for token-efficient maintenance operations
- Commands integrate with existing handoff protocols

## Implementation Status
- **Current Phase:** Enhanced SAVE command with complete transcript preservation
- **Next Phase:** Testing enhanced system and cross-conversation handoff validation
- **Integration:** All commands work seamlessly with GitHub MCP and enhanced transcript system
- **Repository Health:** Systematic maintenance with complete contextual preservation

## System Benefits
✅ **Complete command discoverability** - LIST and HELP commands for immediate guidance  
✅ **Complete project memory** - Full transcript access with READ command including decision context  
✅ **Intelligent workflow guidance** - STATUS provides specific command and conversation recommendations  
✅ **Token efficiency options** - Specialized Dev Commands conversation for maintenance operations  
✅ **Human-friendly operations** - Simple commands for complex project management  
✅ **Systematic maintenance** - Repository stays current automatically  
✅ **Cross-conversation continuity** - READ command enables complete historical context access  
✅ **Flexible workflow patterns** - Multiple approaches for different project needs  
✅ **GitHub integration** - All operations sync with repository automatically  
✅ **Contextual preservation** - SAVE command maintains complete conversational context and decision rationale

## Human Protocol Recommendations

### Current Protocols Working Well:
✅ **Command Discovery:** LIST command provides immediate orientation  
✅ **Command Help:** HELP [command] gives detailed guidance  
✅ **Status Monitoring:** STATUS provides health checks and recommendations  
✅ **Milestone Marking:** MILESTONE captures important progress points  

### Recommended Protocol Enhancements:

#### For New Conversations:
1. **Always start with `LIST`** to see available commands
2. **Use `READ [previous-conversation]`** for context continuity
3. **Check `STATUS`** for current system health and recommendations

#### For Mid-Conversation:
1. **Use `STATUS`** when unsure about next steps
2. **Use `MILESTONE`** when significant progress achieved
3. **Use `SAVE`** when approaching handoff or conversation limits

#### For Conversation Endings:
1. **Use `HANDOFF-PREP`** to prepare transition
2. **Use `SAVE`** to preserve complete context
3. **Update Project Description** as prompted

#### For Command-Heavy Situations:
1. **Create "Dev Commands v1"** conversation for maintenance commands
2. **Use specialized conversation** for repository operations
3. **Return to main conversation** for continued development work

### Protocol Optimization Opportunities:
- **Enhanced human signaling** for when to use specialized conversations
- **Better guidance** on choosing between command options
- **Clearer indicators** for conversation transition points
- **Systematic approach** for cross-project protocol adaptation