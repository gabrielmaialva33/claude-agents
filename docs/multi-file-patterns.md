# Multi-File Operation Patterns

Advanced patterns for working with multiple files efficiently using the new specialized agents and MCP integration.

## Overview

The new multi-file agents bring powerful capabilities for large-scale codebase operations:

- **MultiEdit Tool**: Atomic changes across multiple files
- **MCP Integration**: Intelligent search with Exa and Ref servers
- **Parallel Processing**: Execute independent operations concurrently
- **Batch Operations**: Process hundreds of files efficiently

## Agent Capabilities

### 🔄 Multi-File Refactor
Specializes in complex refactoring operations with atomic guarantees:
- Global renames with dependency tracking
- Extract/inline patterns across files
- Framework migrations with zero downtime
- Maintains semantic consistency

### 🔍 Intelligent Search Agent
Combines local and semantic search for deep code understanding:
- Conceptual pattern matching beyond keywords
- Cross-language equivalent discovery
- Hidden dependency mapping
- API usage pattern analysis

### 📦 Batch File Processor
High-volume file operations with progress tracking:
- Template application across files
- Bulk formatting and linting
- Mass configuration updates
- Parallel execution with checkpoints

### 🚀 Code Migration Specialist
Framework and version migrations with safety guarantees:
- Incremental migration strategies
- Backward compatibility maintenance
- Feature flag integration
- Performance improvement tracking

## Core Patterns

### Pattern 1: Global Refactoring with MultiEdit

```python
# Example: Rename a class across entire codebase
def global_rename():
    # Step 1: Find all occurrences
    files = intelligent_search_agent.find_all("UserManager")
    
    # Step 2: Build atomic change set
    changes = []
    for file in files:
        changes.append({
            "file": file,
            "edits": [
                {"old": "class UserManager", "new": "class UserService"},
                {"old": "UserManager(", "new": "UserService("},
                {"old": "import UserManager", "new": "import UserService"}
            ]
        })
    
    # Step 3: Apply atomically
    multi_file_refactor.apply_atomic(changes)
```

### Pattern 2: Intelligent Migration

```yaml
Migration Strategy:
  1. Discovery Phase:
     - Use intelligent-search to map current patterns
     - Identify all affected components
     - Build dependency graph
  
  2. Planning Phase:
     - code-migration-specialist creates strategy
     - Define rollback points
     - Set feature flags
  
  3. Execution Phase:
     - Apply changes in dependency order
     - Validate after each batch
     - Monitor performance metrics
```

### Pattern 3: Batch Processing Pipeline

```bash
# Process 1000+ files efficiently
batch_pipeline() {
    # Phase 1: Collection
    files=$(find . -name "*.js" -type f)
    
    # Phase 2: Parallel Processing
    echo "$files" | parallel -j 4 --progress \
        'process_file {}'
    
    # Phase 3: Validation
    npm test && npm run lint
}
```

## MCP Server Integration

### Using Exa for Semantic Search

```python
# Find conceptually similar code
results = mcp_exa_search(
    query="authentication validation patterns",
    similarity_threshold=0.8,
    include_context=True
)

# Discover equivalent implementations
similar_code = mcp_exa_search(
    code_sample=example_function,
    find_similar=True,
    cross_language=True
)
```

### Using Ref for Documentation

```python
# Verify API compatibility during refactoring
api_docs = mcp_ref(
    library="react",
    version="18.0",
    method="useState"
)

# Check migration guides
migration_guide = mcp_ref(
    from_version="17.0",
    to_version="18.0",
    breaking_changes=True
)
```

## Advanced Workflows

### Workflow 1: Complete Framework Migration

```markdown
1. **Analysis** (intelligent-search-agent)
   - Map all framework-specific code
   - Identify third-party dependencies
   - Assess migration complexity

2. **Planning** (code-migration-specialist)
   - Create incremental migration plan
   - Set up parallel environments
   - Define success metrics

3. **Execution** (multi-file-refactor + batch-file-processor)
   - Transform code in atomic batches
   - Update configurations
   - Migrate tests

4. **Validation** (code-reviewer + performance-optimizer)
   - Verify functionality preserved
   - Check performance improvements
   - Security audit
```

### Workflow 2: Large-Scale Refactoring

```markdown
1. **Discovery** (intelligent-search-agent)
   - Find all instances of pattern
   - Map relationships
   - Identify edge cases

2. **Transformation** (multi-file-refactor)
   - Apply changes atomically
   - Update imports/exports
   - Maintain backward compatibility

3. **Cleanup** (batch-file-processor)
   - Format all changed files
   - Update documentation
   - Remove deprecated code
```

### Workflow 3: Codebase Modernization

```markdown
1. **Assessment** (code-archaeologist + intelligent-search)
   - Analyze legacy patterns
   - Find modernization opportunities
   - Prioritize changes

2. **Modernization** (code-migration-specialist)
   - Update to latest syntax
   - Replace deprecated APIs
   - Improve type safety

3. **Optimization** (performance-optimizer + batch-file-processor)
   - Apply performance improvements
   - Optimize bundle size
   - Update build configuration
```

## Best Practices

### 1. Atomic Operations
- Always use MultiEdit for related changes
- Group changes by semantic meaning
- Validate after each atomic operation
- Keep rollback points

### 2. Search Strategy
- Start with quick local search
- Use semantic search for concepts
- Combine multiple search modalities
- Cache search results

### 3. Batch Processing
- Determine optimal batch size (10-20 files)
- Use parallel processing when possible
- Implement checkpoint recovery
- Monitor resource usage

### 4. Migration Safety
- Always maintain backward compatibility
- Use feature flags for gradual rollout
- Keep parallel environments
- Document all decisions

## Performance Guidelines

### MultiEdit Operations
- **Batch Size**: 5-10 files per operation
- **Validation**: After each batch
- **Memory**: Monitor for >100 files
- **Rollback**: Keep git checkpoints

### Search Operations
- **Cache Duration**: 5-15 minutes
- **Parallel Searches**: Max 3
- **Result Limit**: 1000 matches
- **Timeout**: 30s per search

### Batch Processing
- **Parallel Workers**: CPU cores - 1
- **Chunk Size**: 10-20 files
- **Checkpoint Frequency**: Every 50 files
- **Memory Limit**: 80% available RAM

## Example Commands

### Refactor Class Name
```bash
claude "Use @multi-file-refactor to rename UserManager to UserService everywhere"
```

### Migrate to New Framework
```bash
claude "Use @code-migration-specialist to migrate from React 17 to React 18"
```

### Find Security Patterns
```bash
claude "Use @intelligent-search-agent to find all authentication and authorization patterns"
```

### Update All Configs
```bash
claude "Use @batch-file-processor to update all package.json files to use Node 18"
```

## Troubleshooting

### Common Issues

1. **Memory Issues with Large Operations**
   - Reduce batch size
   - Process in smaller chunks
   - Use streaming for large files

2. **Failed Atomic Operations**
   - Check git status
   - Review rollback procedure
   - Verify file permissions

3. **Slow Search Performance**
   - Use more specific queries
   - Leverage search cache
   - Parallelize independent searches

4. **Migration Conflicts**
   - Use incremental approach
   - Maintain compatibility layer
   - Test with feature flags

## Integration with Existing Agents

The new multi-file agents work seamlessly with existing specialists:

```markdown
Tech-Lead Orchestrator
├── Intelligent-Search (discovery)
├── Multi-File-Refactor (transformation)
├── Framework Specialists (implementation)
├── Batch-Processor (cleanup)
└── Code-Reviewer (validation)
```

## Summary

The new multi-file operation patterns enable:
- **Atomic changes** across entire codebases
- **Intelligent search** beyond keyword matching
- **Efficient processing** of hundreds of files
- **Safe migrations** with zero downtime

These patterns transform how we handle large-scale codebase operations, making complex refactoring and migrations manageable and safe.