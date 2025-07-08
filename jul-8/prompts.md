# Prompt Collection

## 1. Implementation Planning & Code Review Prompt

```
generate a todo list of how we could apply the above items. for each gather the relevant context that we need to understand how the code is used, how information flows and architectural decisions. ultrathink and execute subtasks in parallel if possible.

once you're done with the implementation, run a code review on the changes and check for breaking bugs or crucial breaking points. find root causes, no superficial patches that cover the actual probem. suggest 1-2 solutions depending on the complexity. make sure to not touch irrelevant parts of the code or break things that you might lack context for. do not write any code, just respond back with fixes to crucial bugs. then pick the more reliable straightforward solutions.
```

## 2. Lean PRD Creation Prompt

```
You are tasked with creating a lean Product Requirements Document (PRD) based on the provided information. Your goal is to organize the given data into a structured PRD format that is concise, actionable, and optimized for fast shipping.

You will be provided with the following input variables:

<USER_PERSONAS>
{{USER_PERSONAS}}
</USER_PERSONAS>

<CORE_HYPOTHESIS>
{{CORE_HYPOTHESIS}}
</CORE_HYPOTHESIS>

<KEY_METRICS>
{{KEY_METRICS}}
</KEY_METRICS>

<USER_STORIES>
{{USER_STORIES}}
</USER_STORIES>

<RELEASE_STRATEGY>
{{RELEASE_STRATEGY}}
</RELEASE_STRATEGY>

Use only the information provided in these input variables to create the PRD.

The PRD should follow this structure:

1. Problem Statement
2. Target User
3. Core Features
4. Ship Criteria
5. Success Metrics
6. Tech Debt Accepted

For each section:

1. Problem Statement: Extract the main problem being solved from the CORE_HYPOTHESIS or other variables. 1-2 sentences max.

2. Target User: Summarize the primary persona from USER_PERSONAS in one sentence.

3. Core Features: List features from USER_STORIES as bullets:
   " [Feature name]: [1-line description] (Priority: P0/P1/P2)

4. Ship Criteria: Define concrete conditions for shipping based on RELEASE_STRATEGY. Focus on MVP criteria.

5. Success Metrics: List key metrics from KEY_METRICS as bullets:
   " [Metric]: [Target change] - Triggered by [event]

6. Tech Debt Accepted: Note any shortcuts, limitations, or future work explicitly deferred for speed.

Output only the PRD content with clear section headings.
```

## 3. Code Improvement Suggestions Prompt

```
give me two suggested solutions how we can improve this and simplify and follow clean code conventions. startup prototype 90/10 impact to effort. don't write code, just respond
```

## 4. Clarifying Questions Prompt

```
Ask any clarifying questions before proceeding. Do not write any code, just respond back.
```

## 5. Code Review for Breaking Changes Prompt

```
can you code review this and check for breaking bugs or crucial breaking points? find root causes and suggest 1-2 solutions depending on the complexity. make sure to not touch irrelevant parts of the code or break things that you might lack context for. Do not write any code, just respond back.
```

## 6. Continue Execution Prompt

```
continue, execute subtasks in parallel if possible
```
