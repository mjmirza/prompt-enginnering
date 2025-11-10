# Prompt Engineering Techniques

This directory contains specific prompting strategies and methods that have proven effective in practice.

## Core Techniques

### Zero-Shot Prompting
- Direct instructions without examples
- When to use zero-shot approaches
- Limitations and considerations

### Few-Shot Learning
- Providing examples in the prompt
- Example selection strategies
- Balancing example quantity and quality
- Format consistency in examples

### Chain-of-Thought (CoT)
- Step-by-step reasoning prompts
- "Let's think step by step"
- Benefits for complex problem-solving
- CoT variations and improvements

### Role-Based Prompting
- Assigning personas and expertise
- Setting context through roles
- Professional vs. creative roles
- Combining roles with other techniques

### Instruction Engineering
- Crafting clear, actionable instructions
- Command structure and syntax
- Positive vs. negative instructions
- Layering multiple instructions

### Prompt Chaining
- Breaking complex tasks into steps
- Sequential prompt execution
- Managing context between prompts
- Error handling in chains

### Self-Consistency
- Generating multiple outputs
- Selecting the most consistent answer
- Voting mechanisms
- Use cases for self-consistency

### Reflection and Self-Critique
- Asking models to review their outputs
- Iterative improvement prompts
- Identifying and correcting errors
- Meta-reasoning techniques

### Constrained Generation
- Limiting output format and style
- Structured output requirements
- Length and content constraints
- JSON and formatted responses

### Context Stuffing
- Providing relevant background information
- Document inclusion strategies
- Context prioritization
- Managing large context windows

## Technique Selection

Choose techniques based on:
- Task complexity
- Required accuracy
- Available context
- Response time constraints
- Token budget

## Combining Techniques

Many techniques work well together:
- Few-shot + Chain-of-Thought
- Role-based + Instruction Engineering
- Prompt Chaining + Self-Consistency
- Context Stuffing + Constrained Generation
