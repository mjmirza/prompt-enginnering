# Chain-of-Thought (CoT) Reasoning Pattern

A powerful technique for breaking down complex problems into step-by-step reasoning processes, improving accuracy and transparency in AI responses.

## Purpose

Enable the AI to think through problems systematically by explicitly showing its reasoning steps, leading to more accurate and explainable answers.

## When to Use

- Complex mathematical or logical problems
- Multi-step reasoning tasks
- When you need to understand the AI's thought process
- Problems requiring sequential decision-making
- When accuracy is more important than speed

## Template Structure

```
[CONTEXT/PROBLEM STATEMENT]

Let's approach this step-by-step:

1. First, [identify/analyze/break down the main components]
2. Next, [consider/evaluate/process each element]
3. Then, [apply logic/rules/calculations]
4. After that, [synthesize/combine the findings]
5. Finally, [reach conclusion/provide answer]

Therefore, [final answer with justification].
```

## Pattern Variations

### Basic CoT
```
Question: [Your question here]

Let's think through this step-by-step:
- Step 1: [First consideration]
- Step 2: [Second consideration]
- Step 3: [Third consideration]

Answer: [Conclusion based on above steps]
```

### Zero-Shot CoT
```
[Question or problem]

Let's think step by step.
```

### Few-Shot CoT (with examples)
```
Example 1:
Q: [Example question]
A: Let's break this down:
   1. [Step 1 of reasoning]
   2. [Step 2 of reasoning]
   Therefore: [Answer]

Example 2:
Q: [Another example question]
A: Let's break this down:
   1. [Step 1 of reasoning]
   2. [Step 2 of reasoning]
   Therefore: [Answer]

Now solve:
Q: [Your actual question]
A: Let's break this down:
```

## Real-World Examples

### Example 1: Mathematical Problem
```
Question: If a shirt costs $45 after a 25% discount, what was the original price?

Let's approach this step-by-step:

1. First, understand what we know:
   - Final price after discount: $45
   - Discount percentage: 25%
   - This means the customer paid 75% of the original price

2. Set up the equation:
   - 75% of original price = $45
   - 0.75 × original price = $45

3. Solve for the original price:
   - original price = $45 ÷ 0.75
   - original price = $60

4. Verify the answer:
   - 25% of $60 = $15
   - $60 - $15 = $45 ✓

Therefore, the original price was $60.
```

### Example 2: Logical Reasoning
```
Question: All roses are flowers. Some flowers fade quickly. Can we conclude that some roses fade quickly?

Let's think through this step-by-step:

1. Identify the given statements:
   - Statement A: All roses are flowers
   - Statement B: Some flowers fade quickly
   - Question: Do some roses fade quickly?

2. Analyze the logical relationship:
   - Roses are a subset of flowers
   - Some flowers (not all) fade quickly
   - We don't know if the "some flowers" that fade quickly include roses

3. Consider what we can and cannot conclude:
   - We CAN say: It's possible that some roses fade quickly
   - We CANNOT say: Some roses definitely fade quickly
   - We CANNOT say: No roses fade quickly

4. Evaluate the logical validity:
   - This is a case of underdetermined logic
   - The conclusion doesn't necessarily follow from the premises

Therefore, we cannot conclusively determine that some roses fade quickly based solely on these statements. The answer is: No, we cannot make that conclusion with certainty.
```

## Best Practices

1. **Be Explicit**: Show every reasoning step clearly
2. **Use Numbered Steps**: Makes the process easy to follow
3. **Verify When Possible**: Include verification of your answer
4. **State Assumptions**: Make any assumptions explicit
5. **Use Clear Language**: Avoid ambiguity in each step
6. **Show Intermediate Results**: Display calculations or intermediate conclusions
7. **Explain "Why"**: Don't just show what you're doing, explain why

## Common Pitfalls

- Skipping steps that seem obvious
- Not verifying the final answer
- Making unstated assumptions
- Jumping to conclusions too quickly
- Not showing the mathematical work
- Mixing steps together instead of separating them

## Tips for Optimization

- For simple problems, basic CoT is sufficient
- For complex problems, use detailed step-by-step breakdown
- Combine with few-shot examples for better results
- Request verification/double-checking in the prompt
- Ask the AI to identify potential errors in its reasoning
- Use phrases like "Let's think step by step" or "Let's approach this systematically"

## Combining with Other Techniques

- **CoT + Few-Shot**: Provide examples with reasoning steps
- **CoT + Self-Consistency**: Generate multiple reasoning paths and compare
- **CoT + Reflection**: Have the AI critique its own reasoning
- **CoT + Role-Playing**: "As an expert mathematician, let's solve this step by step"

## Related Patterns

- Self-Consistency Pattern
- Tree-of-Thoughts Pattern
- Reflection Pattern
- Few-Shot Learning Pattern
