# Conversation Cross-Referencing & Versioning System

## Purpose
Enable conversations to reference specific insights, decisions, and work from other conversations, including proper version management for conversation continuations.

## Naming Convention

### Standard Format
```
[PROJECT-ABBREV]-[YYYY-MM-DD-HHMM]-[FOCUS-AREA]-v[N]
```

### Examples
```
CGI-2025-08-27-1900-setup-v1        # This conversation
CGI-2025-08-27-1930-setup-v2        # Continuation after limits
CGI-2025-08-28-1400-api-design-v1   # New focus area
CGI-2025-08-28-1500-api-design-v2   # Revised approach
```

## Cross-Reference Syntax

### Reference Examples
```markdown
See analysis from [Conv: CGI-setup]                    # Latest version
Build on [Conv: CGI-api-design-v1]                    # Specific version  
Reference [Conv: CGI-setup-latest]                     # Explicit latest
Summary of [Conv: CGI-setup-all]                       # All versions
```

### Resolution Rules
- **Default:** `[Conv: CGI-setup]` resolves to latest version
- **Explicit:** `[Conv: CGI-setup-v1]` targets specific version
- **Latest:** `[Conv: CGI-setup-latest]` explicitly requests latest
- **Summary:** `[Conv: CGI-setup-all]` aggregates across versions

## Version Relationships

### Relationship Types
- **continuation:** v2 continues where v1 left off (limits reached)
- **revision:** v2 revises/replaces v1's approach  
- **branch:** v2 explores alternative approach to v1
- **merge:** v3 combines insights from v1 and v2

### Conversation Lifecycle
1. **Start conversation** with appropriate naming
2. **Register in conversation-registry.json**
3. **Work until limits/natural break**
4. **Create handoff summary**
5. **Start new version** if continuing same focus
6. **Update registry** with version relationship

## Registry Structure

### conversation-registry.json
```json
{
  "conversation_chains": {
    "CGI-setup": {
      "latest_version": "CGI-2025-08-27-1930-setup-v2",
      "versions": [...],
      "focus_area": "integration-setup"
    }
  },
  "conversations": {
    "CGI-2025-08-27-1900-setup-v1": {
      "conversation_id": "...",
      "chain": "CGI-setup", 
      "version": 1,
      "key_outputs": [...],
      "major_decisions": [...],
      "relationships": {...}
    }
  }
}
```

## Implementation Protocol

### For New Conversations
1. **Determine focus area** and check for existing chains
2. **Assign conversation ID** following naming convention
3. **Register conversation** in registry
4. **Reference relevant previous conversations** using cross-reference syntax

### For Conversation Continuations  
1. **Update registry** with end_time for current conversation
2. **Create handoff summary**
3. **Start new version** with incremented version number
4. **Set relationship** (continuation/revision/branch/merge)
5. **Update chain's latest_version**

### For Cross-References
1. **Use standard syntax** `[Conv: chain-name]` or `[Conv: specific-id]`
2. **Validate references** exist in registry
3. **Provide context** about what specific insight/decision is being referenced
4. **Update relationships** in registry (referenced_by tracking)

## Benefits

### Enabled Capabilities
✅ **"Reference the API design from [Conv: CGI-api-design-v2]"**
✅ **"Build on security analysis from [Conv: CGI-security]"** 
✅ **"See database schema in [Conv: CGI-database-v1]"**
✅ **Conversation networks instead of linear chains**
✅ **Knowledge building across specialized focus areas**
✅ **Version history tracking and reference integrity**

### Project Coordination Unlocked
- **Specialized conversations** for different aspects
- **Parallel workstreams** with cross-referencing
- **Iterative improvement** with version tracking
- **Knowledge networks** spanning multiple focus areas
- **Advanced project orchestration** across conversation ecosystem

---

**This system transforms conversation coordination from linear handoffs to networked knowledge building.**