# Root Cause Analysis Pattern

A systematic approach to identifying the fundamental cause of a problem rather than just addressing symptoms.

## Purpose

Dig deep beneath surface-level issues to identify and address the true root cause, preventing recurrence and enabling effective solutions.

## When to Use

- Recurring problems that keep coming back
- Complex issues with unclear origins
- System failures or breakdowns
- Quality issues in products or processes
- Performance problems
- When quick fixes haven't worked

## Template Structure

```
Perform a root cause analysis for: [PROBLEM STATEMENT]

Analysis Framework:

1. Problem Definition
   - Clear description of the issue
   - When it occurs
   - Impact and severity
   - Who/what is affected

2. Symptom vs. Root Cause
   - Observable symptoms
   - Underlying factors

3. 5 Whys Analysis
   - Problem: [Initial problem]
   - Why 1: [First answer]
   - Why 2: [Dig deeper]
   - Why 3: [Continue]
   - Why 4: [Keep going]
   - Why 5: [Root cause]

4. Contributing Factors
   - People factors
   - Process factors
   - Technology factors
   - Environmental factors

5. Root Cause Identification
   - Primary root cause
   - Secondary causes
   - Supporting evidence

6. Recommended Solutions
   - Address root cause
   - Prevent recurrence
   - Fix immediate symptoms

7. Validation
   - How to verify the root cause
   - Success metrics

Approach: Systematic, thorough, evidence-based
```

## Pattern Variations

### Quick 5 Whys
```
Problem: [PROBLEM DESCRIPTION]

Apply the 5 Whys technique:
1. Why did this happen? [Answer]
2. Why did that happen? [Answer]
3. Why did that happen? [Answer]
4. Why did that happen? [Answer]
5. Why did that happen? [Root cause]

Root cause: [Final answer]
Recommended fix: [Solution addressing root cause]
```

### Fishbone Diagram (Ishikawa)
```
Analyze this problem using a fishbone/Ishikawa approach:

Problem: [PROBLEM STATEMENT]

Examine potential causes in each category:

1. People (Manpower)
   - Skills/training issues
   - Human error factors
   - Communication breakdowns

2. Methods (Process)
   - Procedural problems
   - Workflow issues
   - Missing steps

3. Machines (Technology)
   - Equipment failures
   - Tool limitations
   - Technical issues

4. Materials
   - Input quality
   - Resource availability
   - Dependency issues

5. Measurement
   - Metrics problems
   - Data accuracy
   - Monitoring gaps

6. Environment
   - External factors
   - Conditions
   - Constraints

For each category, identify specific potential root causes.
Then determine the most likely actual root cause.
```

### Comparative Analysis
```
We have a problem that occurs in some cases but not others:

Problem: [DESCRIPTION]

Occurs when:
- [Condition 1]
- [Condition 2]
- [Condition 3]

Does NOT occur when:
- [Condition A]
- [Condition B]
- [Condition C]

Analyze:
1. What's different between the two scenarios?
2. What do problem cases have in common?
3. What variable is the likely root cause?
4. How can we test this hypothesis?
5. What solution would address this root cause?
```

### Failure Mode Analysis
```
Analyze potential failure modes for: [SYSTEM/PROCESS]

For this [failure/problem]:

1. What failed?
   - Component/step that failed
   - Expected vs. actual behavior

2. How did it fail?
   - Failure mode
   - Failure mechanism

3. Why did it fail?
   - Immediate cause
   - Underlying cause
   - Root cause

4. Could it have been prevented?
   - Warning signs
   - Preventive measures
   - Detection opportunities

5. How to prevent recurrence?
   - Design changes
   - Process improvements
   - Monitoring systems
```

## Real-World Examples

### Example 1: Software Bug
```
Perform root cause analysis on this recurring production bug:

Problem: User checkout process fails intermittently (5% of attempts)

Observable symptoms:
- Payment screen shows "Transaction Failed" error
- Happens randomly, not reproducible in testing
- Affects both new and returning customers
- Started 2 weeks ago after deployment

Impact:
- ~$50,000 in lost revenue per week
- Customer complaints increasing
- Support ticket volume up 40%

Context:
- Recent deployment included payment gateway update
- No changes to checkout code itself
- Database load has increased 30%
- Error logs show timeout messages

Analyze using:
1. 5 Whys to dig into timeout cause
2. Fishbone to examine all possible factors
3. Timeline analysis (what changed when)
4. Root cause identification
5. Recommended fixes (immediate and long-term)
```

### Example 2: Team Performance Issue
```
Root cause analysis for team productivity decline:

Problem: Team velocity decreased from 50 to 30 story points per sprint

Observable data:
- Declined over last 3 sprints
- More bugs in production (up 60%)
- Team member satisfaction scores down
- Longer code review times
- More meetings added to calendar

Team composition:
- 2 senior devs left, replaced by junior devs (2 months ago)
- New project manager started (1 month ago)
- Team size unchanged (6 people)

Context:
- Company growth and new priorities
- Multiple projects running in parallel
- Pressure to deliver faster

Analyze:
1. People factors (skills, morale, communication)
2. Process factors (workflows, meetings, priorities)
3. Technical factors (technical debt, complexity)
4. Environmental factors (pressure, resources)
5. Identify primary root cause
6. Distinguish between symptoms and cause
7. Recommend solutions that address the root, not just symptoms
```

### Example 3: Customer Churn
```
Analyze why customer churn increased from 5% to 12% this quarter:

Data available:
- Churn survey responses (50% completion rate)
- Usage analytics
- Customer support tickets
- Competitor analysis
- Product change log

Top reasons given in exit surveys:
1. "Too expensive" (40%)
2. "Found better alternative" (30%)
3. "Too complicated" (20%)
4. "Not using it enough" (10%)

Additional observations:
- Churn highest among customers 6-12 months old
- Recent price increase (15%) implemented
- Competitor launched similar product at lower price
- New features released but adoption is low
- Support response time increased to 24 hours

Perform deep root cause analysis:
1. Are exit survey reasons symptoms or actual causes?
2. Apply 5 Whys to each stated reason
3. Examine what competitor is doing differently
4. Analyze correlation between new features and churn timing
5. Identify true root cause(s)
6. Distinguish between market factors vs. internal factors
7. Recommend retention strategies addressing root causes
```

## Best Practices

1. **Define Problem Clearly**: Be specific about what's wrong
2. **Gather Data**: Use evidence, not assumptions
3. **Ask "Why" Multiple Times**: Don't stop at surface answers
4. **Look for Patterns**: Recurring themes point to root causes
5. **Verify the Root Cause**: Test your hypothesis
6. **Address Cause, Not Symptoms**: Fix what actually breaks
7. **Prevent Recurrence**: Implement systemic solutions
8. **Document Findings**: Learn for future issues

## Common Pitfalls

- Stopping too early in the "why" chain
- Confusing symptoms with causes
- Blaming people instead of examining processes
- Accepting first plausible explanation
- Not gathering enough data before analyzing
- Overlooking multiple contributing causes
- Proposing solutions that only treat symptoms
- Not validating the identified root cause

## Tips for Optimization

- Provide specific details about the problem
- Include timeline of when problem started
- Mention what changed around that time
- Share relevant data and metrics
- Specify known symptoms vs. unknowns
- Include failed solution attempts
- Request specific analysis framework
- Ask for both immediate and long-term solutions
- Request validation methods

## Combining with Other Techniques

- **RCA + Data Analysis**: Use data to support cause identification
- **RCA + Stakeholder Input**: Interview affected parties
- **RCA + Experimentation**: Test hypotheses about causes
- **RCA + Process Mapping**: Visualize where breakdown occurs
- **RCA + Timeline Analysis**: Map events leading to problem

## Advanced Variation: Multi-Layer Analysis

```
Perform comprehensive root cause analysis with multiple methodologies:

Problem: [COMPLEX PROBLEM STATEMENT]

Apply these complementary techniques:

1. Timeline Analysis
   - Map chronology of events
   - Identify what changed and when
   - Correlate changes with problem onset

2. 5 Whys (multiple paths)
   - Path A: [From one angle]
   - Path B: [From another angle]
   - Path C: [From third perspective]
   - Compare where paths converge

3. Fishbone Diagram
   - Examine all categories
   - Identify potential causes in each
   - Rate likelihood of each

4. Comparative Analysis
   - When does problem occur vs. not occur
   - Difference analysis

5. Fault Tree Analysis
   - Work backwards from failure
   - Map logical gates (AND/OR)
   - Identify critical path

6. Synthesis
   - Integrate findings from all methods
   - Determine primary root cause
   - Identify contributing factors
   - Rank by impact

7. Solution Design
   - Address root cause directly
   - Mitigate contributing factors
   - Prevent similar issues
   - Implement early warning systems

Evidence required for each finding.
Confidence level for root cause identification.
```

## Root Cause Validation Questions

Before finalizing root cause, ask:
- "If we fix this, will the problem definitely go away?"
- "Would this problem have occurred without this cause?"
- "Is this really a cause or just another symptom?"
- "Have we dug deep enough, or should we ask 'why' again?"
- "What evidence confirms this is the root cause?"
- "Are there multiple root causes we need to address?"

## Related Patterns

- Problem Decomposition Pattern
- Systems Thinking Pattern
- Data Analysis Pattern
- Decision Tree Pattern
- Failure Mode Analysis Pattern
