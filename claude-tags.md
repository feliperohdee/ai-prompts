# Claude's Prompt Engineering Guide: Using Tags for Enhanced Interactions

## Introduction
Tags are powerful tools that help structure and guide Claude's responses. When properly used, they can enhance the clarity, reasoning, and effectiveness of our interactions.

## Basic Tag Structure
Tags follow XML-style syntax:


## Maximizing Claude's Performance

### General Principles for Effective Interaction

1. **Be Explicit and Specific**
   - State your goals clearly
   - Provide context upfront
   - Define expected outcomes
   - Specify any constraints or requirements

2. **Structure Complex Requests**
   ```xml
   <context>
   Primary task: Create a marketing strategy
   Available resources: $10,000 budget, 2-month timeline
   Target audience: Tech-savvy professionals, ages 25-40
   </context>

   <instructions>
   1. First, analyze market demographics
   2. Then, outline channel strategy
   3. Finally, create budget allocation plan
   </instructions>
   ```

3. **Use Iterative Refinement**
   - Start with broad concepts
   - Request specific improvements
   - Build upon previous responses
   - Ask for alternatives or variations

4. **Leverage Multi-Step Problem Solving**
   ```xml
   <chain_of_thoughts>
   Step 1: Define problem scope
   → List all requirements
   → Identify constraints
   → Set success criteria

   Step 2: Break down components
   → Map dependencies
   → Identify critical paths
   → Note potential blockers

   Step 3: Develop solution
   → Start with basic framework
   → Add detailed components
   → Validate against requirements
   </chain_of_thoughts>
   ```

### Common Pitfalls to Avoid

1. **Vague or Ambiguous Requests**
   - ❌ "Make it better"
   - ✅ "Improve the code's performance by optimizing database queries"

2. **Insufficient Context**
   - ❌ "Review this design"
   - ✅ "Review this UI design for a mobile banking app targeting elderly users"

3. **Overloaded Instructions**
   - ❌ Multiple unrelated requests in one prompt
   - ✅ Break down complex tasks into clear, sequential steps

### Best Practices for Complex Tasks

1. **Set Up the Framework**
   ```xml
   <context>
   Project scope and background information
   </context>

   <format>
   Desired output structure
   </format>

   <instructions>
   Step-by-step process
   </instructions>
   ```

2. **Request Interim Checkpoints**
   - Ask for validation at key steps
   - Review partial solutions
   - Confirm understanding before proceeding

3. **Handle Edge Cases**
   ```xml
   <thinking>
   1. Consider normal cases
   2. Identify potential edge cases
   3. Plan error handling
   4. Develop fallback strategies
   </thinking>
   ```

### Effective Question Strategies

1. **Clarifying Questions**
   - "Could you elaborate on [specific aspect]?"
   - "What are the key constraints for [feature]?"
   - "How should the system handle [edge case]?"

2. **Follow-up Refinement**
   - "Could we optimize the [specific part]?"
   - "What alternatives exist for [component]?"
   - "How would this change if we needed to [new requirement]?"

### Real-World Usage Examples

1. **Code Review Request**
   ```xml
   <context>
   Need code review for a Python data processing script
   Focus on performance and security
   </context>

   <instructions>
   1. Review algorithmic efficiency
   2. Check for security vulnerabilities
   3. Suggest optimizations
   4. Identify best practices violations
   </instructions>

   <output>
   Structured review with:
   - Critical issues
   - Performance improvements
   - Security recommendations
   - Code examples
   </output>
   ```

2. **System Architecture Design**
   ```xml
   <tree_of_thoughts>
   System Architecture
   ├── Frontend
   │   ├── User Interface
   │   └── Client Logic
   ├── Backend
   │   ├── API Layer
   │   ├── Business Logic
   │   └── Data Access
   └── Infrastructure
       ├── Deployment
       └── Monitoring
   </tree_of_thoughts>

   <chain_of_thoughts>
   Design Process
   → Requirements gathering
   → Component identification
   → Interface design
   → Implementation planning
   </chain_of_thoughts>
   ```

### Tips for Iterative Development

1. **Start Broad, Then Refine**
   - Begin with high-level concepts
   - Drill down into specific components
   - Iterate on individual elements
   - Validate against original requirements

2. **Use Feedback Loops**
   - Request intermediate reviews
   - Validate assumptions
   - Test edge cases
   - Refine based on findings

3. **Document Evolution**
   ```xml
   <context>
   Current version: 2.0
   Previous feedback: Performance issues in data processing
   Target: Improve processing speed by 50%
   </context>

   <thinking>
   1. Analyze current bottlenecks
   2. Identify optimization opportunities
   3. Implement improvements
   4. Measure results
   </thinking>

   <tagname>content</tagname>
   ```

## Detailed Tag Breakdown

### 1. Thinking Tag
**Purpose**: Enables explicit reasoning and step-by-step analysis  
**Usage**: `<thinking>...</thinking>`

```xml
<thinking>
1. First, I need to analyze the requirements
2. Then, I should consider the edge cases
3. Finally, I can formulate a comprehensive solution
</thinking>
```

**Best Practices**:
- Use numbered steps for complex reasoning
- Break down problems into manageable chunks
- Show your work, especially for mathematical or logical problems

### 2. Output Tag
**Purpose**: Specifies desired response format or structure  
**Usage**: `<output>...</output>`

**Supported Formats**:

1. **JSON**:
```xml
<output>
{
  "format": "json",
  "fields": ["name", "age", "occupation"],
  "style": "compact"
}
</output>
```

2. **Table**:
```xml
<output>
| Name    | Age | Score |
|---------|-----|-------|
| Alice   | 25  | 95    |
| Bob     | 30  | 88    |
</output>
```

3. **YAML**:
```xml
<output>
format: yaml
user:
  name: John Doe
  age: 30
  preferences:
    - coding
    - gaming
    - reading
</output>
```

4. **CSV**:
```xml
<output>
name,age,score
Alice,25,95
Bob,30,88
Charlie,28,92
</output>
```

5. **Structured List**:
```xml
<output>
1. Main Category
   1.1. Subcategory A
        - Item 1
        - Item 2
   1.2. Subcategory B
        - Item 3
        - Item 4
</output>
```

6. **Code Block**:
```xml
<output>
'''python
def calculate_score(points, multiplier):
    return points * multiplier
'''
</output>
```

7. **Document Template**:
```xml
<output>
Title: Project Report
Author: [Name]
Date: [Current Date]

Executive Summary:
[Summary Content]

1. Introduction
2. Methodology
3. Results
4. Conclusions
</output>
```

8. **XML**:
```xml
<output>
<user>
    <name>John Doe</name>
    <age>30</age>
    <skills>
        <skill>Python</skill>
        <skill>JavaScript</skill>
    </skills>
</user>
</output>
```

9. **Key-Value Pairs**:
```xml
<output>
Name: John Doe
Age: 30
Location: New York
Status: Active
Last Login: 2024-01-25
</output>
```

10. **Custom Format**:
```xml
<output format="custom">
[Start Report]
==============
Title: {title}
Date: {date}
Content: {content}
==============
[End Report]
</output>
```

**Best Practices**:
- Define clear data structures
- Specify formatting requirements
- Include validation rules if needed
- Use consistent formatting within each output type
- Include sample data for complex formats
- Specify any special characters or delimiters
- Consider readability and parsing needs

### 3. Context Tag
**Purpose**: Provides background information or sets the scene  
**Usage**: `<context>...</context>`

```xml
<context>
You are writing for a technical blog aimed at junior developers.
The audience has basic programming knowledge but needs clear explanations.
The topic is REST API design.
</context>
```

**Best Practices**:
- Be specific about audience
- Include relevant background information
- Define any constraints or assumptions

### 4. Format Tag
**Purpose**: Defines the structural layout of the response  
**Usage**: `<format>...</format>`

```xml
<format>
1. Title
2. Executive Summary (100 words)
3. Main Points (3-5 bullets)
4. Detailed Analysis
5. Recommendations
</format>
```

**Best Practices**:
- Provide clear structure
- Include length requirements if needed
- Specify any special formatting needs

### 5. Tone Tag
**Purpose**: Sets the writing style and voice  
**Usage**: `<tone>...</tone>`

```xml
<tone>
Professional but friendly, using accessible language while maintaining technical accuracy.
Avoid jargon unless necessary, and explain technical terms when used.
</tone>
```

**Best Practices**:
- Be specific about formality level
- Define any style constraints
- Specify language complexity

### 6. Example Tag
**Purpose**: Provides sample content or expected output  
**Usage**: `<example>...</example>`

```xml
<example>
Good response:
"The quick sort algorithm has an average time complexity of O(n log n)..."

Bad response:
"Quick sort is fast..."
</example>
```

**Best Practices**:
- Include both positive and negative examples
- Be specific and concrete
- Show context when relevant

### 7. Instructions Tag
**Purpose**: Provides specific guidance for task execution  
**Usage**: `<instructions>...</instructions>`

```xml
<instructions>
1. Review the code for security vulnerabilities
2. Focus on SQL injection and XSS attacks
3. Provide specific examples of vulnerable code
4. Suggest secure alternatives
5. Include testing recommendations
</instructions>
```

**Best Practices**:
- Use clear, actionable steps
- Be specific about requirements
- Include any constraints or limitations

## Combining Tags with Tree of Thoughts

Tree of Thoughts (ToT) is a systematic problem-solving approach that can be enhanced using these tags. Here's an example:

```xml
<thinking>
Let me break this down using Tree of Thoughts:

Branch 1: Security Analysis
├── SQL Injection risks
│   ├── Input validation
│   └── Prepared statements
└── XSS vulnerabilities
    ├── Output encoding
    └── Content Security Policy

Branch 2: Performance Optimization
├── Database queries
│   ├── Indexing
│   └── Query optimization
└── Frontend loading
    ├── Asset compression
    └── Caching strategies
</thinking>

<output>
Detailed analysis for each branch with specific recommendations...
</output>
```

## Combining Tags with Chain of Thought

Chain of Thought (CoT) reasoning can be structured using these tags:

```xml
<thinking>
Step 1: Analyze the problem domain
→ The system handles sensitive user data
→ Multiple entry points exist for data

Step 2: Identify potential vulnerabilities
→ User input validation is minimal
→ No rate limiting implemented

Step 3: Develop solutions
→ Implement input validation
→ Add rate limiting middleware
</thinking>

<instructions>
Based on this analysis:
1. Implement input validation
2. Add rate limiting
3. Test security measures
</instructions>
```

## Best Practices for Tag Usage

1. **Nesting**: Tags can be nested when logical:
```xml
<context>
  <format>
    Technical documentation
  </format>
  <tone>
    Professional and precise
  </tone>
</context>
```

2. **Order**: Use tags in a logical sequence:
- Context first
- Thinking/reasoning next
- Output/format last

3. **Clarity**: Keep tag content focused and specific
```xml
<thinking>
Clear, specific thought process:
1. Analyze requirements
2. Identify constraints
3. Develop solution
</thinking>
```

4. **Consistency**: Maintain consistent format within tags
```xml
<format>
All sections should use:
- Markdown headers
- Code blocks for examples
- Bulleted lists for features
</format>
```

Remember that tags are tools to enhance communication and understanding. Use them thoughtfully and purposefully to achieve the best results in your interactions with Claude.

## Additional Thinking Tags

You can also use specialized thinking tags to structure different types of reasoning:

### Tree of Thoughts Tag
**Usage**: `<tree_of_thoughts>...</tree_of_thoughts>`

### Chain of Thoughts Tag
**Usage**: `<chain_of_thoughts>...</chain_of_thoughts>`

## Complete Sample: Game Development Prompt

Here's a comprehensive example using multiple tags to guide the development of a game:

```xml
<context>
We need to develop a 2D platformer game with a space theme. The target audience is casual gamers aged 12-18. The game should be challenging but not frustrating, with a learning curve that gradually increases difficulty.
</context>

<format>
- Game Design Document Structure
- Core Mechanics
- Technical Requirements
- Implementation Plan
- Testing Strategy
</format>

<tree_of_thoughts>
Game Core Systems
├── Player Mechanics
│   ├── Movement
│   │   ├── Basic walking/running
│   │   ├── Jumping mechanics
│   │   └── Zero-gravity sections
│   └── Abilities
│       ├── Jetpack boost
│       └── Shield activation
├── Level Design
│   ├── Environment types
│   │   ├── Space stations
│   │   ├── Alien planets
│   │   └── Asteroid fields
│   └── Difficulty progression
│       ├── Tutorial section
│       ├── Early levels
│       └── Advanced challenges
└── Game Systems
    ├── Score tracking
    ├── Power-up collection
    └── Achievement system
</tree_of_thoughts>

<chain_of_thoughts>
Step 1: Core Gameplay Loop Analysis
→ Player explores space environments
→ Collects power-ups and resources
→ Overcomes platforming challenges
→ Reaches checkpoint or level end

Step 2: Technical Requirements
→ Physics system for variable gravity
→ Particle effects for space atmosphere
→ Smooth character controls
→ Efficient collision detection

Step 3: Development Priorities
→ Prototype basic movement
→ Implement core mechanics
→ Design initial levels
→ Add polish and effects
</chain_of_thoughts>

<instructions>
1. Create the basic player controller
   - Implement horizontal movement
   - Add jumping mechanics
   - Develop gravity switching system

2. Design level building blocks
   - Platform types
   - Hazards and obstacles
   - Power-up placement points

3. Implement game systems
   - Score tracking
   - Life/health system
   - Checkpoint system
   - Power-up effects

4. Create tutorial level
   - Introduce basic controls
   - Teach core mechanics
   - Provide clear guidance

5. Develop testing plan
   - Movement feel testing
   - Difficulty curve analysis
   - Bug tracking system
   - Player feedback sessions
</instructions>

<tone>
Technical and precise when discussing implementation details, but maintain accessibility for team members who might not be programmers.
</tone>

<example>
Good implementation description:
"The player controller should use physics-based movement with configurable parameters for acceleration, max speed, and jump force. Implement a ground check using raycasts to ensure precise jump detection."

Bad implementation description:
"Make the player move and jump smoothly."

Good level design guidance:
"Tutorial section should introduce mechanics sequentially: 1) basic movement, 2) jumping, 3) jetpack, with clear visual cues and optional text prompts."

Bad level design guidance:
"Start with easy levels and make them harder."
</example>

<output>
Expected deliverables:
1. Game Design Document (GDD)
2. Technical specification document
3. Sprint planning breakdown
4. Testing documentation template
5. Asset requirement list
</output>
```

This comprehensive example shows how to combine various tags to create a structured approach to game development. The tags help organize different aspects of the development process:

- `<context>` sets the project scope and target audience
- `<tree_of_thoughts>` breaks down the game systems hierarchically
- `<chain_of_thoughts>` outlines the logical development sequence
- `<instructions>` provides specific implementation steps
- `<tone>` ensures appropriate communication style
- `<example>` demonstrates good and bad practices
- `<output>` defines expected deliverables

The specialized thinking tags (`<tree_of_thoughts>` and `<chain_of_thoughts>`) help organize complex reasoning in different ways:
- Tree of thoughts is excellent for breaking down systems and features
- Chain of thoughts works well for sequential planning and development steps

Using these tags effectively can help ensure clear communication and systematic development approaches in complex projects.

## Requesting Thought Diagrams

### Requesting a Tree of Thoughts ASCII Diagram

#### Best Format:
```xml
<context>
I need to develop a Tree of Thoughts diagram for [your topic].
Key elements to consider:
- [List main components]
- [List key considerations]
- [List any constraints]
</context>

<format>
ASCII diagram with:
- Main branches using ├── and └── symbols
- Sub-branches indented with proper spacing
- Clear hierarchy of thoughts
- Maximum depth of [number] levels
</format>

<output>
Tree structure with:
- Clear node descriptions
- Proper indentation
- Logical grouping of related thoughts
</output>
```

#### Example Request:
```xml
<context>
I need to develop a Tree of Thoughts diagram for building a personal finance app.
Key elements:
- Core features
- User experience
- Technical requirements
- Security considerations
</context>

<format>
ASCII diagram with:
- Main branches for each key element
- Sub-branches for specific components
- Maximum depth of 3 levels
- Clear relationships between elements
</format>

<output>
Personal Finance App
├── Core Features
│   ├── Expense Tracking
│   │   ├── Manual Entry
│   │   └── Receipt Scanning
│   └── Budget Management
│       ├── Category Setting
│       └── Alerts System
└── User Experience
    ├── Interface Design
    │   ├── Mobile First
    │   └── Accessibility
    └── User Flow
        ├── Onboarding
        └── Daily Usage
</output>
```

### Requesting a Chain of Thoughts ASCII Diagram

#### Best Format:
```xml
<context>
I need to develop a Chain of Thoughts diagram for [your process].
Sequential steps should include:
- [List main steps]
- [List dependencies]
- [List decision points]
</context>

<format>
ASCII diagram with:
- Sequential steps using → or ⟶ arrows
- Clear step descriptions
- Decision points marked
- Optional branching paths
</format>

<output>
Sequential flow with:
- Numbered steps
- Logical progression
- Clear connections
</output>
```

#### Example Request:
```xml
<context>
I need to develop a Chain of Thoughts diagram for user authentication process.
Sequential steps including:
- Login attempt
- Validation
- Security checks
- Access granting
</context>

<format>
ASCII diagram showing step-by-step process with arrows and decision points
</format>

<output>
User Authentication Flow
Step 1: Login Attempt
→ User enters credentials
  → Validate input format
    → Check against database
      → [Decision Point]
        ├── Success → Grant access
        └── Failure → Error handling
          → Retry or Reset options
</output>
```

### Tips for Best Results:

1. **Be Specific**:
   - Clearly state the topic or process
   - Define the desired depth
   - Specify any particular formatting preferences

2. **Provide Context**:
   - Include relevant background information
   - Mention any specific requirements
   - Highlight important considerations

3. **Define Structure**:
   - Specify maximum levels of depth
   - Indicate if certain branches need more detail
   - Mention any required grouping or categorization

4. **Request Formatting**:
   - Ask for specific ASCII characters if preferred
   - Specify indentation preferences
   - Mention any special notation needs

5. **Consider Readability**:
   - Request appropriate spacing
   - Ask for clear labels
   - Specify if certain elements need emphasis

### Sample Combined Request:
```xml
<context>
I need both Tree and Chain of Thoughts diagrams for developing a new product feature.
The process should cover both the component breakdown and sequential implementation steps.
</context>

<format>
Provide both:
1. Tree diagram showing feature components
2. Chain diagram showing implementation sequence
Use clear ASCII formatting and proper indentation
</format>

<output>
[Tree of Thoughts will display here]

[Chain of Thoughts will display here]
</output>

<instructions>
Please ensure:
- Clear connection between tree components and chain steps
- Logical flow between elements
- Proper indentation and formatting
- Readable labels and descriptions
</instructions>
```
