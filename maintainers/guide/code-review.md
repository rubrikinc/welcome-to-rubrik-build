# Code Reviews

All changes must be code reviewed. For non-maintainers this is obvious, since you can't commit anyway. But even for maintainers, all code changes should receive at least one review, preferably (for non-trivial changes obligatorily) from someone who knows the areas the change touches.

For non-trivial changes, multiple reviewers may be assigned. The primary reviewer will make this decision and nominate a second reviewer, if needed. If a maintainer intends to be the primary reviewer of a PR they should set themselves as the assignee on GitHub, then reply to the PR and specify so. However, only the primary reviewer of a change should conduct the merge, except in rare cases.

If a PR has gone 2 work days without an owner emerging, please poke the PR thread and ask for a reviewer to be assigned.

Except for rare cases, such as trivial changes (e.g. typos, comments) or emergencies (e.g. broken builds), maintainers should not merge their own changes.

Expect reviewers to request that you follow the PR template.

## Assigning Reviews

Maintainers can assign reviews to other maintainers, when appropriate. The assignee manages that PR and is responsible for merging or closing the PR once ready. The assignee may request reviews from non-maintainers.

## The Code Review Process

- The **author** submits a PR
- Phase 0: Select **reviewers** and **approvers** for the PR
  - Choose at least two suggested **reviewers** and request their reviews on the PR
  - Choose suggested **approvers**, based on project maintainers, and list them in a comment on the PR
- Phase 1: Humans review the PR
  - **Reviewers** look for general code quality, correctness, sane software engineering, style, etc.
  - Anyone in the organization can act as a **reviewer** with the _exception_ of the individual who opened the PR
  - If the code changes look good to them, a **reviewer** types :shipit:, `ship it` in a PR comment. If changes are needed, be precise and give detail as to what needs to be changed for approval. 
  - Once a **reviewer** has approved, apply an `status/4-merge` label to the PR
- Phase 2: Humans approve the PR
  - The PR **author** assigns all suggested **approvers** to the PR, and optionally notifies them
  - Only people listed as owners or maintainers can act as **approvers**, including the individual who opened the PR.
  - **Approvers** look for holistic acceptance criteria, including dependencies with other features, forwards/backwards compatibility, API and flag definitions, etc
  - If the code changes look good to them, an **approver** types `approved` in a PR comment or review. If changes are needed, be precise and give detail as to what needs to be changed for approval. 
- Phase 3: Merge the PR:
  - Then the PR can be merged by a project maintainer and any associated branches deleted
