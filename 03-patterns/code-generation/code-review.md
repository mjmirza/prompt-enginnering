# Code Review Pattern

A structured approach for conducting thorough, constructive code reviews that improve code quality and foster learning.

## Purpose

Systematically review code for quality, correctness, maintainability, security, and best practices while providing actionable feedback.

## When to Use

- Pull request reviews
- Security audits
- Performance optimization
- Refactoring assessment
- Mentoring developers
- Pre-production code validation
- Learning from existing codebases

## Template Structure

```
Review this code for [SPECIFIC FOCUS or "comprehensive review"]:

[CODE TO REVIEW]

Context:
- Language: [programming language]
- Purpose: [what the code does]
- Framework/Libraries: [if relevant]
- Target environment: [production/test/dev]

Review criteria:
1. **Functionality**: Does it work correctly?
2. **Code Quality**: Is it clean, readable, maintainable?
3. **Performance**: Any efficiency concerns?
4. **Security**: Vulnerabilities or risks?
5. **Best Practices**: Following language/framework conventions?
6. **Testing**: Adequate test coverage?
7. **Documentation**: Clear comments and docs?
8. **Error Handling**: Proper exception management?

For each issue found, provide:
- Severity: [Critical/Major/Minor/Suggestion]
- Location: [specific line or function]
- Issue: [what's wrong]
- Why: [why it's a problem]
- Fix: [how to improve it]
- Example: [code example of improvement]

Summary:
- Overall assessment
- Must-fix items
- Nice-to-have improvements
- Positive aspects
```

## Pattern Variations

### Quick Code Review
```
Perform a quick code review of:

[CODE]

Focus on:
- Critical bugs or errors
- Security vulnerabilities
- Obvious performance issues
- Major code smell

Provide top 3 most important issues with fixes.
```

### Security-Focused Review
```
Security audit this code:

[CODE]

Check for:
- SQL injection vulnerabilities
- XSS (Cross-Site Scripting) risks
- Authentication/authorization flaws
- Sensitive data exposure
- Insecure dependencies
- CSRF vulnerabilities
- Input validation issues
- Cryptography problems
- Access control bugs

For each security issue:
- Risk level: [Critical/High/Medium/Low]
- Vulnerability type
- Attack scenario
- Mitigation strategy
- Secure code example
```

### Performance Review
```
Review this code for performance:

[CODE]

Analyze:
- Time complexity
- Space complexity
- Database query efficiency
- Network calls optimization
- Caching opportunities
- Memory leaks
- Unnecessary computations
- Algorithm choice

Suggest optimizations with:
- Expected performance gain
- Implementation difficulty
- Trade-offs to consider
```

### Refactoring Assessment
```
Evaluate this code for refactoring:

[CODE]

Assess:
- Code smells (duplicated code, long methods, god objects, etc.)
- SOLID principles violations
- Coupling and cohesion
- Naming clarity
- Function/class size
- Complexity (cyclomatic complexity)
- Testability

Provide refactoring suggestions:
- What to refactor
- Proposed structure
- Benefits
- Refactoring steps
- Risks/considerations
```

## Real-World Examples

### Example 1: JavaScript Function Review
```
Review this JavaScript function comprehensively:

```javascript
function processUserData(users) {
    var result = [];
    for (var i = 0; i < users.length; i++) {
        if (users[i].age >= 18) {
            result.push({
                name: users[i].firstName + ' ' + users[i].lastName,
                email: users[i].email,
                age: users[i].age
            });
        }
    }
    return result;
}
```

Context:
- Language: JavaScript (ES6+ available)
- Purpose: Filter and transform user data
- Used in: Customer management system
- Performance: May handle 1000+ users

Review for:
- Modern JavaScript practices
- Code quality and readability
- Performance
- Error handling
- Type safety considerations
```

### Example 2: Python API Endpoint
```
Security and functionality review:

```python
@app.route('/api/user/<user_id>', methods=['GET'])
def get_user(user_id):
    query = f"SELECT * FROM users WHERE id = {user_id}"
    result = db.execute(query)
    user = result.fetchone()
    return jsonify(user)
```

Context:
- Framework: Flask
- Database: PostgreSQL
- Environment: Production API
- Authentication: JWT (handled elsewhere)

Focus on:
- Security vulnerabilities (priority)
- Error handling
- Best practices
- Performance considerations
```

### Example 3: React Component Review
```
Review this React component:

```typescript
import React, { useState, useEffect } from 'react';

const UserProfile = ({ userId }) => {
    const [user, setUser] = useState(null);
    const [loading, setLoading] = useState(false);

    useEffect(() => {
        setLoading(true);
        fetch(`/api/users/${userId}`)
            .then(res => res.json())
            .then(data => {
                setUser(data);
                setLoading(false);
            });
    }, [userId]);

    if (loading) return <div>Loading...</div>;
    if (!user) return <div>No user found</div>;

    return (
        <div>
            <h1>{user.name}</h1>
            <p>{user.email}</p>
            <p>{user.bio}</p>
        </div>
    );
};

export default UserProfile;
```

Context:
- Framework: React 18 with TypeScript
- Purpose: Display user profile
- State management: Local state (no Redux)

Review for:
- React best practices
- Error handling
- Loading states
- TypeScript usage
- Performance optimization
- Accessibility
```

## Best Practices

1. **Be Constructive**: Focus on improvement, not criticism
2. **Be Specific**: Point to exact lines and provide examples
3. **Explain Why**: Don't just say what's wrong, explain the impact
4. **Prioritize**: Distinguish critical issues from suggestions
5. **Acknowledge Good**: Highlight well-written code
6. **Provide Context**: Explain the reasoning behind feedback
7. **Offer Solutions**: Suggest how to fix, not just what's wrong
8. **Consider Trade-offs**: Recognize that perfect code isn't always practical

## Common Pitfalls

- Being overly critical or negative
- Nitpicking minor style issues
- Not explaining the "why" behind feedback
- Suggesting changes without considering context
- Missing security vulnerabilities
- Focusing only on what's wrong
- Being vague ("this could be better")
- Not prioritizing feedback by importance

## Review Checklist

### Functionality
- [ ] Code does what it's supposed to do
- [ ] Edge cases are handled
- [ ] Input validation is present
- [ ] Output is correct format

### Code Quality
- [ ] Readable and self-documenting
- [ ] Following naming conventions
- [ ] Appropriate comments where needed
- [ ] No code duplication
- [ ] Functions are single-purpose
- [ ] Reasonable complexity

### Performance
- [ ] No obvious performance issues
- [ ] Efficient algorithms
- [ ] Appropriate data structures
- [ ] No memory leaks
- [ ] Database queries optimized

### Security
- [ ] Input sanitization
- [ ] No SQL injection risks
- [ ] No XSS vulnerabilities
- [ ] Proper authentication/authorization
- [ ] Sensitive data protected
- [ ] Dependencies are secure

### Error Handling
- [ ] Exceptions are caught appropriately
- [ ] Error messages are helpful
- [ ] Graceful degradation
- [ ] Logging for debugging

### Testing
- [ ] Unit tests present
- [ ] Tests cover edge cases
- [ ] Tests are meaningful
- [ ] Test names are descriptive

### Documentation
- [ ] Function/class documentation
- [ ] Complex logic is explained
- [ ] API documentation if relevant
- [ ] README updated if needed

## Tips for Optimization

- Specify what aspects are most important
- Provide context about the codebase standards
- Mention if this is for learning or production
- Indicate team's proficiency level
- Share any specific concerns you have
- Request code examples in feedback
- Ask for prioritized issues
- Specify coding standards to check against

## Severity Levels Guide

**Critical**:
- Security vulnerabilities
- Data loss risks
- System crashes
- Broken functionality

**Major**:
- Significant performance issues
- Poor error handling
- Major code smells
- Scalability concerns

**Minor**:
- Style inconsistencies
- Missing documentation
- Suboptimal but working code
- Minor code smells

**Suggestion**:
- Nice-to-have improvements
- Alternative approaches
- Educational points
- Future enhancements

## Combining with Other Techniques

- **Code Review + Testing**: Review tests alongside code
- **Code Review + Refactoring**: Suggest refactoring opportunities
- **Code Review + Documentation**: Review docs for accuracy
- **Code Review + Pair Programming**: Collaborative review
- **Code Review + Benchmarking**: Measure performance claims

## Advanced Variation: Comparative Review

```
Compare these two implementations and recommend the better approach:

Implementation A:
[CODE A]

Implementation B:
[CODE B]

Context: [purpose and requirements]

Compare based on:
1. Correctness
2. Readability
3. Performance
4. Maintainability
5. Security
6. Scalability
7. Test coverage

For each criterion:
- Which is better and why
- Specific advantages/disadvantages
- Could either be improved?

Final recommendation:
- Which to use
- Why
- Any modifications needed
```

## Language-Specific Considerations

When requesting reviews, mention language-specific aspects:

**JavaScript/TypeScript**:
- Modern syntax usage
- Type safety
- Async/await patterns
- Promise handling

**Python**:
- PEP 8 compliance
- Pythonic idioms
- Type hints
- Generator usage

**Java**:
- SOLID principles
- Design patterns
- Exception handling
- Resource management

**Go**:
- Idiomatic Go
- Error handling patterns
- Goroutine safety
- Interface usage

## Related Patterns

- Refactoring Pattern
- Testing Pattern
- Security Audit Pattern
- Performance Optimization Pattern
- Code Documentation Pattern
