# Building and running

Before submitting any changes, it is crucial to validate them by running the
full preflight check. This command will build the repository, run all tests,
and lint the code.

To run the full suite of checks, execute the following command:

```bash
npm run preflight
```

This single command ensures that your changes meet all the quality gates of the
project. While you can run the individual steps (`build`, `test`, `lint`)
separately, it is highly recommended to use `npm run preflight` to ensure a
comprehensive validation.

# Writing Tests

When writing tests, aim to follow existing patterns. Key conventions include:

## Test Structure and Framework

* **Framework**: All tests are written using pytest.
* **File Location**: Test files are co-located with the source files they test.
* **Setup/Teardown**: Use `setup_class`, `teardown_class`, `setup_method`, and
    `teardown_method`.

## Asynchronous Testing

* Use `async/await`.

## General Guidance

* When adding tests, first examine existing tests to understand and conform to
  established conventions.
* Pay close attention to the mocks at the top of existing test files; they
  reveal critical dependencies and how they are managed in a test environment.

# Process

1. Analyze the user's code for optimization opportunities:
   * Check for React anti-patterns that prevent compiler optimization
   * Look for component structure issues that limit compiler effectiveness
   * Think about each suggestion you are making and consult React docs for best
     practices

2. Provide actionable guidance:
   * Explain specific code changes with clear reasoning
   * Show before/after examples when suggesting changes
   * Only suggest changes that meaningfully improve optimization potential

# Optimization Guidelines

* State updates should be structured to enable granular updates
* Side effects should be isolated and dependencies clearly defined

# Comments policy

Only write high-value comments if at all. Avoid talking to the user through
comments.

# General Guidelines

* This project is written in Python.

# General style requirements

Use hyphens instead of underscores in flag names (e.g. `my-flag` instead of
`my_flag`).

# Git Repo

The main branch for this project is called "main"