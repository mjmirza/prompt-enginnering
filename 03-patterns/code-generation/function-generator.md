# Function Generator Pattern

A structured approach for generating well-documented, tested, and production-ready code functions.

## Purpose

Generate clean, efficient, and maintainable functions with proper documentation, error handling, and test cases.

## When to Use

- Creating new utility functions
- Implementing specific algorithms
- Building reusable code components
- Need for well-documented code
- Requiring both implementation and tests

## Template Structure

```
Create a [LANGUAGE] function that [SPECIFIC TASK].

Requirements:
- Function name: [functionName]
- Input parameters: [parameter1: type, parameter2: type, ...]
- Return type: [type]
- Edge cases to handle: [list edge cases]
- Performance constraints: [if any]

Include:
1. Clear function documentation
2. Type hints/annotations
3. Input validation
4. Error handling
5. Usage examples
6. Unit tests

Code style: [style guide if applicable]
```

## Pattern Variations

### Simple Function Generation
```
Write a [LANGUAGE] function called [functionName] that:
- Takes [inputs] as parameters
- Returns [output]
- Handles [edge cases]

Include docstring and example usage.
```

### Advanced Function with Tests
```
Generate a production-ready [LANGUAGE] function:

Purpose: [Clear description of what it does]
Signature: [functionName(param1: type1, param2: type2) -> returnType]

Requirements:
- Input validation for [specific constraints]
- Error handling for [specific scenarios]
- Time complexity: [target, e.g., O(n)]
- Space complexity: [target, e.g., O(1)]

Provide:
1. Fully documented function
2. Comprehensive unit tests
3. Usage examples
4. Performance notes
```

### Refactoring Pattern
```
Refactor this function to improve [readability/performance/maintainability]:

[PASTE EXISTING CODE]

Goals:
- [Specific improvement 1]
- [Specific improvement 2]
- Maintain backward compatibility: [Yes/No]

Provide before/after comparison and explanation of changes.
```

## Real-World Examples

### Example 1: Python String Validator
```
Create a Python function that validates email addresses.

Requirements:
- Function name: is_valid_email
- Input parameter: email (str)
- Return type: bool
- Edge cases: empty strings, missing @, invalid domains, special characters

Include:
1. Clear function documentation
2. Type hints
3. Comprehensive validation logic
4. Usage examples
5. Unit tests covering edge cases

Code style: PEP 8
```

**Expected Output Structure:**
```python
def is_valid_email(email: str) -> bool:
    """
    Validates an email address format.

    Args:
        email (str): The email address to validate

    Returns:
        bool: True if email is valid, False otherwise

    Examples:
        >>> is_valid_email("user@example.com")
        True
        >>> is_valid_email("invalid.email")
        False
    """
    # Implementation with validation logic
```

### Example 2: JavaScript Array Utility
```
Write a JavaScript function called chunk that splits an array into smaller arrays of a specified size.

Requirements:
- Input: array (any[]), chunkSize (number)
- Return: array of arrays
- Handle: empty arrays, chunkSize larger than array, invalid inputs
- Use TypeScript for type safety

Include JSDoc comments and Jest test cases.
```

### Example 3: Data Processing Function
```
Generate a Python function for data transformation:

Purpose: Convert a flat list of records into a nested dictionary grouped by category
Signature: group_by_category(records: List[Dict], key: str) -> Dict[str, List[Dict]]

Requirements:
- Handle missing keys gracefully
- Preserve original record order within groups
- Validate input types
- O(n) time complexity

Provide:
1. Function with type hints and docstring
2. Input validation
3. Error handling with custom exceptions
4. 5+ unit tests including edge cases
5. Usage example with sample data
```

## Best Practices

1. **Clear Specifications**: Be explicit about inputs, outputs, and behavior
2. **Edge Cases**: Always specify edge cases to handle
3. **Documentation**: Request proper docstrings/comments
4. **Testing**: Ask for comprehensive test coverage
5. **Error Handling**: Specify what errors should be caught and how
6. **Performance**: Mention any performance requirements
7. **Code Style**: Reference specific style guides if needed
8. **Examples**: Request usage examples for clarity

## Common Pitfalls

- Vague function descriptions
- Not specifying edge cases
- Forgetting to request tests
- Missing type annotations
- Unclear error handling requirements
- Not mentioning performance constraints
- Skipping validation logic

## Tips for Optimization

- Provide example inputs/outputs for clarity
- Specify the exact naming convention
- Mention any dependencies or libraries to use/avoid
- Request explanation of algorithm choices
- Ask for time/space complexity analysis
- Include requirements for backwards compatibility
- Specify logging or debugging requirements

## Combining with Other Techniques

- **Function Generation + Code Review**: Generate then review
- **Function Generation + Refactoring**: Create initial version, then optimize
- **Function Generation + Documentation**: Generate comprehensive docs separately
- **Function Generation + Testing**: Generate tests first (TDD approach)

## Template for Multiple Related Functions

```
Create a [LANGUAGE] module for [PURPOSE] with the following functions:

1. [functionName1]: [description]
   - Inputs: [parameters]
   - Output: [return type]
   - Purpose: [specific goal]

2. [functionName2]: [description]
   - Inputs: [parameters]
   - Output: [return type]
   - Purpose: [specific goal]

3. [functionName3]: [description]
   - Inputs: [parameters]
   - Output: [return type]
   - Purpose: [specific goal]

Requirements:
- Shared type definitions
- Consistent error handling
- Comprehensive module documentation
- Integration tests showing functions working together
- Export all public functions

Code organization: [structure preferences]
```

## Related Patterns

- Code Review Pattern
- Refactoring Pattern
- Test Generation Pattern
- Documentation Pattern
- Algorithm Implementation Pattern
