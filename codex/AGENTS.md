# Engineering Rules

## General

- Prefer the simplest implementation that fully solves the requested problem.
- Avoid speculative abstractions, unnecessary wrappers, factories, generic layers, and premature extensibility.
- Reuse existing platform/framework capabilities before adding dependencies.
- Keep diffs small and focused.
- Do not modify unrelated code.
- Do not add dependencies without a concrete need.

## Project creation

When starting a new project:

1. Clarify the actual requirements from the task.
2. Choose the smallest suitable stack.
3. Establish a working vertical slice before adding architecture.
4. Add structure only when real code needs it.
5. Avoid creating placeholder abstractions for hypothetical future features.

## Implementation

- Prefer readable, boring code.
- Prefer explicit code over clever abstractions.
- Prefer composition over unnecessary inheritance/framework layers.
- Keep modules cohesive and reasonably small.
- Do not create helpers used only once unless they materially improve clarity.

## Testing

- Test observable behavior, not implementation details.
- For bugs, reproduce the bug before fixing when practical.
- Run relevant tests after changes.
- Run build/typecheck/lint when applicable.
- Never claim something works unless it was actually verified.

## Debugging

When behavior is broken:

1. Reproduce.
2. Gather evidence.
3. Identify root cause.
4. Form a hypothesis.
5. Make the smallest appropriate fix.
6. Verify the fix.
7. Stop when the requested behavior works.

Do not shotgun-edit code based on guesses.

## Refactoring

- Preserve existing behavior unless explicitly asked to change it.
- Refactor in small verified steps.
- Avoid refactoring unrelated code.
- Prefer deletion and simplification over adding architecture.

## UI

When building UI:

- Establish a coherent visual direction before polishing individual components.
- Use semantic HTML and accessible controls.
- Support keyboard interaction where appropriate.
- Handle loading, empty, error, disabled, hover, focus, and responsive states.
- Avoid generic AI-dashboard aesthetics unless explicitly requested.
- Prefer a small consistent design system over one-off styling.

## Completion

Before declaring a task complete:

- run relevant tests
- run type checking if available
- run build if applicable
- inspect resulting behavior
- review the diff for unrelated changes

If acceptance criteria are satisfied, stop.
