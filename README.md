# Tailwind CSS @apply Directive Conflict within @layer

This repository demonstrates a bug related to the usage of Tailwind's `@apply` directive within `@layer` directives.  Specifically, it highlights situations where the order of style application doesn't always match the expected behavior, leading to style conflicts and unexpected results.

## Bug Description
When using `@apply` within different `@layer` directives, there's no consistent guarantee that the later layers will override the earlier ones. This means the `@apply` rules might not correctly overwrite or apply styles as expected, depending on the order and content of the layers. This inconsistency can result in styles not being applied or incorrect styles being applied.

## Reproduction
The `bug.css` file demonstrates the problem.  The `bugSolution.css` file shows a potential solution.

## Solution
This problem can be approached in several ways.  The most straightforward fix might involve either carefully re-ordering `@layer` or revising the way styles are applied to ensure clear precedence. In some cases,  rethinking the layer structure of your styles might be the best approach. The solution in `bugSolution.css` provides one approach, however, the best solution is contextual to your project needs.
