# Research Agent File Handling Workflow

**Issue**: Research agents using the Task tool generate file creation responses but don't actually save files to the filesystem.

**Root Cause**: Task tool agents operate in simulation environment - artifact syntax in responses doesn't execute actual file operations.

## Corrected Workflow

### When Using Research Agents for File Generation:

1. **Use Task tool** to generate comprehensive research and file content
2. **Review agent response** for file creation artifacts and content  
3. **Manually extract content** from agent response
4. **Use Write tool** to actually save files to filesystem
5. **Verify file creation** with filesystem checks

### Example Implementation:

```bash
# Step 1: Use research agent
Task with Documentation Research Specialist -> generates response with file content

# Step 2: Extract content and manually create file  
Write tool -> create actual file with agent-generated content

# Step 3: Verify
ls or find -> confirm file exists on filesystem
```

## Prevention Strategy

- Always verify file creation after research agent tasks
- Don't assume agent "file creation" responses represent actual filesystem operations
- Use systematic verification workflow for all research agent outputs

## Long-term Solution Options

1. **Accept Current Behavior**: Research agents provide content, manual file creation required
2. **Create Wrapper Workflow**: Automate extraction and file creation from agent responses  
3. **Documentation Update**: Clarify in project docs that research agents require manual file creation

**Recommended**: Option 1 (Accept) - maintains security isolation while providing research value.