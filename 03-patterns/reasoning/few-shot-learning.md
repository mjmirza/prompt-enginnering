# Few-Shot Learning Pattern

A technique for improving AI responses by providing a small number of examples that demonstrate the desired output format, style, and approach.

## Purpose

Guide the AI to understand your exact requirements by showing examples of correct inputs and outputs, dramatically improving response quality and consistency.

## When to Use

- Need specific output format
- Complex or unusual tasks
- Consistency across multiple prompts
- Custom classification or categorization
- Specific tone or style required
- Pattern recognition tasks
- When zero-shot attempts fail

## Template Structure

```
Task: [CLEAR DESCRIPTION OF WHAT YOU WANT]

Here are examples of correct inputs and outputs:

Example 1:
Input: [Example input 1]
Output: [Desired output 1]

Example 2:
Input: [Example input 2]
Output: [Desired output 2]

Example 3:
Input: [Example input 3]
Output: [Desired output 3]

Now apply the same pattern to:
Input: [YOUR ACTUAL INPUT]
Output:
```

## Pattern Variations

### Basic Few-Shot
```
I need you to [TASK].

Examples:

[Example 1]
[Example 2]
[Example 3]

Now do the same for: [YOUR INPUT]
```

### Few-Shot with Explanation
```
Task: [TASK DESCRIPTION]

Format: [DESIRED FORMAT]

Examples with explanation:

Example 1:
Input: [Input]
Output: [Output]
Why this works: [Brief explanation]

Example 2:
Input: [Input]
Output: [Output]
Why this works: [Brief explanation]

Now process: [YOUR INPUT]
```

### Few-Shot Classification
```
Classify the following into categories: [CATEGORY 1], [CATEGORY 2], [CATEGORY 3]

Training examples:

"[Text 1]" → Category: [CATEGORY]
"[Text 2]" → Category: [CATEGORY]
"[Text 3]" → Category: [CATEGORY]
"[Text 4]" → Category: [CATEGORY]

Classify:
"[YOUR TEXT]" → Category:
```

### Few-Shot with Edge Cases
```
[TASK DESCRIPTION]

Examples including edge cases:

Normal case:
Input: [Normal example]
Output: [Expected output]

Edge case 1 (empty input):
Input: ""
Output: [How to handle]

Edge case 2 (invalid format):
Input: [Invalid example]
Output: [Error handling or correction]

Normal case 2:
Input: [Another normal example]
Output: [Expected output]

Process:
Input: [YOUR INPUT]
Output:
```

## Real-World Examples

### Example 1: Sentiment Analysis with Nuance
```
Classify customer feedback into: Positive, Negative, Mixed, or Neutral.
Include confidence level and key reason.

Examples:

"The product works great but shipping took forever."
Classification: Mixed
Confidence: High
Reason: Positive about product, negative about shipping

"It's okay, nothing special."
Classification: Neutral
Confidence: High
Reason: Lacks strong positive or negative indicators

"Absolutely love it! Game changer!"
Classification: Positive
Confidence: Very High
Reason: Strong positive language and enthusiasm

"Stopped working after a week. Waste of money."
Classification: Negative
Confidence: Very High
Reason: Product failure and explicit dissatisfaction

Now classify:
"Does the job but I expected more for the price."
Classification:
Confidence:
Reason:
```

### Example 2: Code Comment Generation
```
Generate concise, helpful code comments.

Examples:

Code: `const users = data.filter(u => u.age >= 18)`
Comment: // Filter to only include adult users (18+)

Code: `await Promise.all(requests.map(r => fetch(r)))`
Comment: // Execute all API requests in parallel

Code: `if (!user?.permissions?.includes('admin')) throw new Error('Unauthorized')`
Comment: // Verify user has admin permissions before proceeding

Code: `const cached = localStorage.getItem(key) || fetchFresh()`
Comment: // Use cached data if available, otherwise fetch new data

Now generate comment for:
Code: `const throttled = debounce(handleSearch, 300)`
Comment:
```

### Example 3: Email Subject Line Generation
```
Generate engaging, specific subject lines (under 50 characters).

Email content → Subject line:

"Hi! Just wanted to follow up on our conversation about the Q4 marketing budget..."
→ "Following up: Q4 marketing budget discussion"

"I'm excited to share that we've just released a major update to our platform..."
→ "We've launched new platform features!"

"Unfortunately, we need to reschedule tomorrow's meeting due to a conflict..."
→ "Meeting reschedule request - tomorrow"

"Thank you for taking the time to speak with me yesterday about the partnership opportunity..."
→ "Thank you - partnership conversation follow-up"

Generate subject for:
"I wanted to reach out because I noticed you're using our competitor's product and thought you might be interested in..."
→
```

### Example 4: Data Extraction
```
Extract structured data from unstructured text.

Text: "John Smith, age 34, lives in Seattle and works as a Software Engineer at Microsoft."
Output:
{
  "name": "John Smith",
  "age": 34,
  "location": "Seattle",
  "occupation": "Software Engineer",
  "company": "Microsoft"
}

Text: "Sarah Chen is a 28-year-old designer from Portland."
Output:
{
  "name": "Sarah Chen",
  "age": 28,
  "location": "Portland",
  "occupation": "designer",
  "company": null
}

Text: "Dr. Ahmed Hassan works at Johns Hopkins Hospital in Baltimore as a cardiologist."
Output:
{
  "name": "Dr. Ahmed Hassan",
  "age": null,
  "location": "Baltimore",
  "occupation": "cardiologist",
  "company": "Johns Hopkins Hospital"
}

Extract from:
Text: "Meet Lisa Rodriguez, a 31-year-old data scientist based in Austin, currently at Google."
Output:
```

### Example 5: Text Transformation
```
Transform formal business language to friendly, casual tone while keeping the message.

Formal → Casual:

"We regret to inform you that your application has not been successful at this time."
→ "Thanks for applying! Unfortunately, we decided to go with other candidates this time."

"Please find attached the quarterly report as requested."
→ "Here's the quarterly report you asked for!"

"We would appreciate it if you could provide feedback at your earliest convenience."
→ "We'd love to hear your feedback when you get a chance!"

"I am writing to confirm receipt of your email dated..."
→ "Got your email! Just confirming I received it."

Transform:
"We kindly request that you complete the survey to help us improve our services."
→
```

## Best Practices

1. **Choose Good Examples**: Representative of the task
2. **Diverse Examples**: Cover different scenarios
3. **Consistent Format**: Examples follow same structure
4. **Sufficient Quantity**: Usually 2-5 examples (more isn't always better)
5. **Include Edge Cases**: Show how to handle unusual inputs
6. **Clear Pattern**: Examples should make pattern obvious
7. **Balanced Examples**: Don't bias toward one type
8. **Quality Over Quantity**: Good examples beat many mediocre ones

## Common Pitfalls

- Examples don't actually show the pattern you want
- Too few examples (pattern unclear)
- Too many examples (dilutes focus)
- Examples too similar to each other
- Inconsistent format across examples
- Examples that contradict each other
- Not including edge case handling
- Examples that are too complex

## Tips for Optimization

- Start with 3 examples as baseline
- Add more if AI doesn't get it
- Ensure examples span the range of expected inputs
- Include at least one edge case example
- Make format extremely consistent
- Use clear delimiters between examples
- Label what's input vs. output clearly
- Consider adding brief explanations for complex cases

## Number of Examples Guide

**1-2 Examples**: Very simple, obvious patterns
**3-4 Examples**: Most tasks (sweet spot)
**5-7 Examples**: Complex patterns, multiple variations
**8+ Examples**: Usually unnecessary, may confuse

## Combining with Other Techniques

- **Few-Shot + Chain-of-Thought**: Show reasoning in examples
- **Few-Shot + Role**: "As a [role], here are examples..."
- **Few-Shot + Instructions**: Combine examples with explicit rules
- **Few-Shot + Constraints**: Examples demonstrate constraints
- **Few-Shot + Iterative**: Start few-shot, refine based on results

## Advanced Variations

### Contrastive Examples
```
Task: [DESCRIPTION]

Good examples:
Input: [Input] → Output: [Correct output] ✓

Bad examples (don't do this):
Input: [Input] → Output: [Incorrect output] ✗ (Wrong because: [reason])

Good example:
Input: [Input] → Output: [Correct output] ✓

Bad example (don't do this):
Input: [Input] → Output: [Incorrect output] ✗ (Wrong because: [reason])

Now process:
Input: [YOUR INPUT] → Output:
```

### Few-Shot with Reasoning
```
Task: [TASK]

Examples with reasoning:

Example 1:
Input: [Input]
Reasoning: [Step-by-step thought process]
Output: [Output]

Example 2:
Input: [Input]
Reasoning: [Step-by-step thought process]
Output: [Output]

Example 3:
Input: [Input]
Reasoning: [Step-by-step thought process]
Output: [Output]

Apply the same reasoning to:
Input: [YOUR INPUT]
Reasoning:
Output:
```

### Few-Shot with Categories
```
I have multiple types of [ITEMS] that need different handling:

Type A (characteristics: [X, Y]):
Example 1: [Input] → [Output]
Example 2: [Input] → [Output]

Type B (characteristics: [M, N]):
Example 1: [Input] → [Output]
Example 2: [Input] → [Output]

Type C (characteristics: [P, Q]):
Example 1: [Input] → [Output]
Example 2: [Input] → [Output]

Classify and process:
[YOUR INPUT]
Type:
Output:
```

## Example Selection Strategy

**Good Examples Are**:
- Typical of the task
- Clear and unambiguous
- Diverse but not contradictory
- Simple enough to understand
- Complex enough to be useful

**Include**:
- Most common case
- Important edge case
- Different variations
- Range of difficulty
- Clear positive examples

**Avoid**:
- Overly complex examples
- Ambiguous cases
- Controversial examples
- Examples that contradict
- Extremely rare edge cases

## Testing Your Examples

Before using, verify:
1. Do examples clearly show the pattern?
2. Could someone unfamiliar replicate the pattern?
3. Are any examples confusing or ambiguous?
4. Do examples cover the range of actual use?
5. Is the format perfectly consistent?
6. Are there contradictions between examples?

## Related Patterns

- Zero-Shot Prompting Pattern
- Chain-of-Thought Pattern
- Classification Pattern
- Template Generation Pattern
- Data Transformation Pattern
