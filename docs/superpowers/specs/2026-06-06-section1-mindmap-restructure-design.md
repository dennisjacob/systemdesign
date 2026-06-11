# Section 1 — Mindmap Restructure Design

## Objective

Restructure three section-1 files (1.1 Scale Engineering Primitives, 1.2 OS Primitives, 1.3 Hardware Tier Boundaries) with a study-friendly mindmap flow that includes explicit Cause → Approach blocks for every characteristic and consideration.

## Per-File Template

Each file follows this exact template:

```
# Section Title: Topic Area
> Enhanced Edition tagline

## Master Mindmap (top of file)
[ASCII box diagram showing all topics in the file and their connections]

## Topic 1

### Mindmap Header
[ASCII box diagram showing the topic's hierarchy:
 central concept → its dimensions → characteristics beneath each dimension
 Arrows show cause→approach lines and cross-concept connections]

### What It Is
Brief definition (1-3 paragraphs). What problem does this concept solve?

### Core Dimensions
For each dimension of the topic:

#### Dimension Name
**Definition**: One-line what this is.

**Characteristics** (bulleted, each with child blocks):
- **Characteristic name**
  - **Cause**: Why this happens / what creates this behavior (include formulas if applicable)
  - **Approach**: How to handle it (bulleted strategies)
  - **Trade-off**: What you gain vs. what you lose

**Supporting Math** (if applicable):
- Formulas with worked examples

### Cross-Concept Connections
How this topic connects to other topics within the file and across files:
- Connection A → Topic X (reason)
- Connection B → Topic Y (reason)

### Failure Modes

Each failure mode is a structured block:

- **Failure name**
  - **Cause**: Root cause (1-2 lines)
  - **Approach**: Mitigation strategies (bullets)
  - **Trade-off**: What each mitigation costs

### Interview Questions
Preserved as `<details>` blocks, but prefixed with which core dimension they test.

### Quick Reference (cheat table)
Preserved at end of each file.

## Mindmap Header Format

ASCII box diagrams use this style:

```
┌─ Topic Name ──────────────────────────────────────────┐
│                                                        │
│  Dimension A               Dimension B                 │
│       │                        │                      │
│  ┌────┼────┐            ┌──────┼──────┐              │
│  │    │    │            │      │      │              │
│ Char1 Char2 Char3      CharA  CharB  CharC            │
│   │    │               Cause → Approach               │
│ Cause → Approach        Constraint → Mitigation        │
│                                                        │
│  Amdahl's Law ◄── governs both ──► Little's Law       │
│                          ▲                              │
│                    Cross-concept link                   │
└────────────────────────────────────────────────────────┘
```

Rules:
- Width: 60-80 chars per box
- `─│┌┐└┘├┤┬┴┼◄►▲▼` characters for lines and arrows
- `→` for cause→approach flow
- `◄──►` for cross-concept relationships
- `│` for parent-child hierarchy

## Cause → Approach Block Format

Every characteristic gets this explicit structure:

```
- **Characteristic name**
  - **Cause**: Why it happens. Include formulas, statistics, or mechanism description.
  - **Approach**: 
    - Strategy 1 — brief description
    - Strategy 2 — brief description
  - **Trade-off**: What you gain (latency, cost, reliability) vs. what you lose (complexity, overhead)
```

## Cross-File Connections Map

| Concept | File | Connects To | File |
|---------|------|-------------|------|
| Amdahl's Law / Parallelism | 1.1 | NUMA topology, core count | 1.3 |
| Latency waterfall | 1.1 | Latency numbers (L1→DRAM→SSD) | 1.3 |
| Event loop / coroutines | 1.2 | Context switch cost, cache misses | 1.3 |
| Memory mapped IPC | 1.2 | DRAM latency, NUMA | 1.3 |
| Cache hit ratio | 1.1 | Cache hierarchy (L1/L2/L3/DRAM) | 1.3 |
| Rate limiting (Little's Law) | 1.1 | Linux diagnostics (iostat, vmstat) | 1.2 |
| Process isolation | 1.2 | ECC memory, row hammer | 1.3 |

## Content Preservation Rules

- **Do NOT remove**: Any factual content, numbers, formulas, code examples, or interview questions
- **Do NOT change**: The overall informational depth or accuracy
- **Do change**: Structure, flow, organization, and how cause→approach relationships are presented
- **Preserve**: All `<details>` interview question blocks, tables, and ASCII diagrams
- **Remove**: Redundant prose that doesn't add information value

## Checklist

- [ ] Each topic starts with an ASCII mindmap header
- [ ] Each dimension has Characteristics with Cause → Approach → Trade-off
- [ ] Failure Modes have Cause / Approach / Trade-off
- [ ] Cross-concept connections are called out
- [ ] All original content preserved (just reorganized)
- [ ] Interview questions tagged with relevant dimension
- [ ] Quick Reference cheat sheet preserved at end