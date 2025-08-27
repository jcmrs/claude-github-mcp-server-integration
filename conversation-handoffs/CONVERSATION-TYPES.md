# Conversation Types & Scope System

## Human-Friendly Format: `Type Scope Version`

### Primary Conversation Types
- **Setup** - Installation, configuration, initial setup
- **Planning** - Strategy, roadmaps, requirements, architecture  
- **Development** - Building, coding, implementation
- **Testing** - Validation, debugging, quality assurance
- **Documentation** - Writing guides, manuals, specifications
- **Integration** - Connecting systems, APIs, workflows
- **Review** - Evaluation, assessment, improvement
- **Maintenance** - Updates, fixes, ongoing support
- **Brainstorm** - Concept development, creative exploration, Claude.AI/Human synergy

### Specialized Conversation Types
- **Research** - Investigation, analysis, exploration
- **Security** - Security analysis, penetration testing, hardening
- **Performance** - Optimization, benchmarking, scaling
- **Training** - Learning, tutorials, knowledge transfer
- **Coffee** - Casual conversation, no formal constraints, relaxed interaction

### Common Scopes
#### Technical Scopes
- **Core** - Main functionality, essential features
- **Frontend** - UI, UX, client-side work
- **Backend** - Server, database, API work
- **Database** - Schema, queries, data modeling
- **API** - Interface design, endpoints, integration
- **Authentication** - Login, security, permissions
- **Infrastructure** - Deployment, hosting, DevOps

#### Project Scopes
- **Strategy** - Business planning, market analysis
- **Requirements** - Gathering, analysis, specification
- **User-Experience** - UX research, design, testing
- **Feature-[Name]** - Specific feature development
- **Module-[Name]** - Specific module/component
- **Integration-[System]** - Integration with specific system

#### General Scopes
- **General** - Broad or miscellaneous topics
- **All** - Project-wide discussions

### Version Indicators
- **v1, v2, v3** - Clear numerical progression
- **Continue** - Picking up where left off (same approach)
- **Fresh** - Starting completely new approach
- **Revision** - Revising/improving previous work

## Human Command Examples
```
"Continue the setup work" → Setup Core Continue
"Let's brainstorm API ideas" → Brainstorm API v1
"Start fresh documentation" → Documentation User-Guide Fresh
"Coffee chat about the project" → Coffee General Continue
"Debug the authentication system" → Testing Authentication v2
```

## System Translation
```
Human Input: "Continue database setup work"
→ System: Type=Setup, Scope=Database, Version=Continue
→ Searches: Recent Setup conversations with Database scope
→ Loads: Latest context and continues work
```