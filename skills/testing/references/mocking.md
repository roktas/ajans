# Mocking

Use substitutes only at boundaries where the real dependency is external, nondeterministic, slow, destructive, or
otherwise unsuitable for the test being written. Prefer real project components inside the system under test.

## Boundaries

Good candidates for substitution include:

- external network services and third-party APIs;
- time, randomness, environment, and other nondeterministic inputs;
- filesystems, subprocesses, devices, or operating-system services when a real integration is not appropriate;
- databases when the project does not provide a practical test database or integration fixture.

When the repository already has a reliable test database, local service, fake server, fixture, or integration harness,
prefer it over a mock that reproduces the dependency's behavior by hand.

## Internal collaborators

Do not mock your own classes, modules, functions, or internal collaborators merely to isolate every unit. Such mocks bind
tests to the current implementation graph and often fail during behavior-preserving refactors.

Prefer testing through the stable public seam with real internal collaborators. If a component is difficult to test
without extensive internal mocking, first ask whether the public boundary or dependency direction is poorly designed.
Do not introduce abstraction only to satisfy a mocking technique.

## Boundary design

At a real external boundary, expose the smallest interface that represents the operation the application needs. Prefer
specific domain operations over a generic transport wrapper whose mocks require conditional logic to imitate many
unrelated calls.

Inject boundary dependencies when that makes the contract explicit and testable, but follow the project's existing
architecture. Do not add dependency injection, wrapper layers, or interfaces solely because a test framework makes them
convenient.

## Assertions

Assert the behavior visible through the tested seam. At a mocked external boundary, verify the minimum interaction that
is itself part of the contract. Avoid incidental call counts, ordering, or argument structure that callers do not depend
on.
