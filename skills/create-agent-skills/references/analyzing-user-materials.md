# Reference: Analyzing User-Provided Materials

<overview>
When building skills, user-provided reference materials provide invaluable context that web searches cannot: specific API signatures, internal conventions, project-specific patterns, and domain terminology. This reference explains how to gather, analyze, and synthesize user materials into effective skill content.
</overview>

<material_types>
## Types of Reference Materials

<type name="Documentation Files">
**Examples:** README.md, API docs, library documentation, internal wikis
**Value:** Authoritative source for terminology, concepts, constraints
**What to extract:**
- Key terminology and definitions
- API signatures and parameters
- Constraints and limitations
- Recommended patterns from the docs
</type>

<type name="Code Examples">
**Examples:** Sample implementations, existing scripts, reference projects
**Value:** Concrete patterns showing how things actually work
**What to extract:**
- Coding conventions (naming, structure)
- Common patterns and idioms
- Error handling approaches
- Integration patterns
</type>

<type name="Existing Skills">
**Examples:** Other SKILL.md files, workflows, references
**Value:** Proven structures and patterns to adopt
**What to extract:**
- Effective intake/routing patterns
- Workflow organization
- Reference file structures
- Success criteria patterns
</type>

<type name="API Specifications">
**Examples:** OpenAPI/Swagger specs, GraphQL schemas, SDK docs
**Value:** Precise interface definitions
**What to extract:**
- Endpoint signatures
- Request/response structures
- Authentication requirements
- Rate limits and constraints
</type>

<type name="Screenshots/Diagrams">
**Examples:** UI mockups, architecture diagrams, flowcharts
**Value:** Visual context for workflows
**What to extract:**
- User flow understanding
- Component relationships
- State transitions
- Expected outputs
</type>
</material_types>

<gathering_process>
## How to Gather Materials

**Step 1: Ask what materials are available**
```
Do you have any reference materials I should review before building this skill?

Examples:
- Documentation files (README, API docs, guides)
- Code examples or existing implementations
- Other skills to use as patterns
- API specs or schemas
- Screenshots or diagrams

You can provide file paths, paste content, or say "none" to proceed without.
```

**Step 2: For each material provided**
- If file path: Read the file
- If pasted content: Analyze inline
- If URL: Use WebFetch to retrieve (if accessible)

**Step 3: Acknowledge what was received**
```
I've reviewed:
- [filename] - [brief description of what it contains]
- [filename] - [brief description]

Key insights I'll incorporate:
- [insight 1]
- [insight 2]
```
</gathering_process>

<analysis_methodology>
## Analysis Methodology

<analysis_for type="Documentation">
**Read for:**
1. **Terminology** - Domain-specific terms to use in the skill
2. **Concepts** - Core ideas the skill must understand
3. **Constraints** - Limitations, requirements, boundaries
4. **Workflows** - Recommended sequences of operations
5. **Edge cases** - Special handling documented

**Output:** List of terms, concepts, and constraints to incorporate
</analysis_for>

<analysis_for type="Code Examples">
**Read for:**
1. **Patterns** - Repeated structures across examples
2. **Conventions** - Naming, formatting, organization
3. **Error handling** - How errors are managed
4. **Integration** - How components connect
5. **Testing** - How correctness is verified

**Output:** Pattern summary with code snippets to reference
</analysis_for>

<analysis_for type="Existing Skills">
**Read for:**
1. **Structure** - How intake/routing is organized
2. **Workflow design** - Step granularity and flow
3. **Reference organization** - How knowledge is split
4. **Voice/tone** - How instructions are phrased
5. **Success criteria** - How completion is defined

**Output:** Structural patterns to adopt or adapt
</analysis_for>

<analysis_for type="API Specifications">
**Read for:**
1. **Endpoints** - Available operations
2. **Parameters** - Required and optional inputs
3. **Responses** - Expected outputs and errors
4. **Auth** - Authentication requirements
5. **Limits** - Rate limits, quotas, constraints

**Output:** API summary for skill reference sections
</analysis_for>
</analysis_methodology>

<synthesis>
## Synthesizing into Skill Content

**For SKILL.md essential principles:**
- Extract fundamental concepts that always apply
- Use terminology from user's documentation
- Reference constraints discovered in materials

**For workflows:**
- Mirror patterns seen in code examples
- Include steps that match documented workflows
- Add verification steps based on how examples test

**For references:**
- Organize by concepts found in documentation
- Include code patterns extracted from examples
- Document constraints and edge cases discovered

**For success criteria:**
- Base on verification patterns from examples
- Include checks mentioned in documentation
- Match quality standards implied by materials
</synthesis>

<verification>
## Verifying Material Quality

Before incorporating materials, check:

<check name="Currency">
- When was this documentation last updated?
- Does the API version match current?
- Are code examples using current syntax?
</check>

<check name="Authority">
- Is this official documentation?
- Is the code from a maintained source?
- Are these patterns recommended or just one approach?
</check>

<check name="Completeness">
- Does this cover the full scope needed?
- Are there gaps requiring additional research?
- What's missing that we'll need to find elsewhere?
</check>

<check name="Consistency">
- Do multiple materials agree?
- Are there contradictions to resolve?
- Which source should take precedence?
</check>
</verification>

<anti_patterns>
## What NOT to Do

- **Don't blindly copy** - Adapt patterns, don't just paste
- **Don't assume currency** - Verify documentation is up-to-date
- **Don't skip synthesis** - Raw extraction isn't useful; synthesize insights
- **Don't ignore conflicts** - If materials disagree, ask user which is authoritative
- **Don't over-extract** - Focus on what's relevant to the skill being built
- **Don't forget attribution** - Note which insights came from user materials
</anti_patterns>

<integration_with_research>
## Combining with Web Research

User materials complement (not replace) web research:

1. **User materials first** - Establish baseline from provided context
2. **Web research to fill gaps** - Search for what materials don't cover
3. **Web research to verify** - Confirm user materials are current
4. **User materials to filter** - Use provided context to evaluate search results

**Priority order:**
1. Official documentation provided by user
2. Code examples from user's actual project
3. Web research from authoritative sources
4. General patterns from Claude's knowledge
</integration_with_research>
