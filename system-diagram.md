Here's a detailed prompt for creating code-to-diagram visualizations:

# Code Flow Diagram Creation Prompt

## Context
I need to create a comprehensive flow diagram from source code that accurately represents:
- System execution flow
- State transitions
- Concurrency points
- Error handling
- Decision points
- Input/output paths

## Source Code Input Requirements
Please provide:
1. The complete source code or relevant sections
2. File type/programming language
3. Any specific focus areas you want to highlight (e.g., error handling, concurrency)

## Expected Output Style
The diagram should:
1. Use Mermaid flowchart syntax
2. Include clear node categorization:
   - Process nodes (execution steps)
   - Decision nodes (conditionals)
   - State nodes (system states)
   - Error nodes (error handling)
   - Concurrent operation nodes
3. Use consistent styling with:
   - Clear color coding for different node types
   - High contrast for readability
   - Appropriate spacing and layout
4. Show all terminal points (Start/End)

## Analysis Requirements
Please analyze the code for:
1. Entry points and triggers
2. Main execution paths
3. Concurrency mechanisms:
   - Parallel execution points
   - Locks and synchronization
   - Resource sharing
4. Error handling flows
5. State transitions
6. Business logic decision points
7. Subprocess and function calls
8. Data flow between components

## Diagram Organization
Structure the diagram to show:
1. Logical grouping of related operations
2. Clear progression of execution flow
3. All possible paths between states
4. Proper error and exception flows
5. Concurrent operation boundaries
6. Input/output relationships

## Visual Style Guidelines
Use these style conventions:
1. Process nodes: Light blue fill, dark blue border
2. Decision nodes: Light green fill, dark green border
3. State nodes: Light purple fill, dark purple border
4. Error nodes: Light red fill, dark red border
5. Concurrent nodes: Light orange fill, dark orange border
6. High contrast colors for text
7. Clear connection lines
8. Descriptive labels

## Technical Details Required
For each major component, identify:
1. Function signatures and parameters
2. State mutations
3. External dependencies
4. Resource requirements
5. Error conditions
6. Success criteria
7. Concurrent operation requirements
8. Performance considerations

## Expected Diagram Elements
Please include:
1. Start and End nodes
2. Main process flow
3. All decision points with conditions
4. Error handling paths
5. State transitions
6. Concurrent operation indicators
7. Critical resource access points
8. System boundaries

## Special Considerations
1. Highlight performance-critical paths
2. Mark points of potential resource contention
3. Identify retry mechanisms
4. Show timeout handling
5. Indicate validation steps
6. Mark transaction boundaries
7. Show external system interactions
8. Indicate asynchronous operations

## Output Format
Provide the diagram as:
1. Mermaid-compatible syntax
2. Clear node and edge definitions
3. Proper styling declarations
4. Comments explaining complex flows
5. Legend for node types
6. Clear section organization

## Additional Notes
Please explain:
1. Any assumptions made
2. Simplifications applied
3. Areas needing clarification
4. Critical path identification
5. Resource bottlenecks
6. Scaling considerations
7. Performance implications
8. Security boundaries

This prompt should help reproduce detailed system flow diagrams from source code, similar to how we analyzed the task processing system. When following this prompt, focus on understanding the core system behavior first, then build out the visual representation systematically.

Would you like me to demonstrate how to use this prompt with a different piece of code?
