## Code Review using OWNERS files

This is a simplified description of our [full PR testing and merge
workflow](/contributors/guide/pull-requests.md#the-testing-and-merge-workflow)
that conveniently forgets about the existence of tests, to focus solely on the roles driven by
OWNERS files.  Please see [below](#automation-using-owners-files) for details on how specific
aspects of this process may be configured on a per-repo basis.

### The Code Review Process

- The **author** submits a PR
- Phase 0: Automation suggests **reviewers** and **approvers** for the PR
  - Determine the set of OWNERS files nearest to the code being changed
  - Choose at least two suggested **reviewers**, trying to find a unique reviewer for every leaf
    OWNERS file, and request their reviews on the PR
  - Choose suggested **approvers**, one from each OWNERS file, and list them in a comment on the PR
- Phase 1: Humans review the PR
  - **Reviewers** look for general code quality, correctness, sane software engineering, style, etc.
  - Anyone in the organization can act as a **reviewer** with the exception of the individual who
    opened the PR
  - If the code changes look good to them, a **reviewer** types `/lgtm` in a PR comment or review;
    if they change their mind, they `/lgtm cancel`
  - Once a **reviewer** has `/lgtm`'ed, [prow](https://prow.k8s.io)
    ([@k8s-ci-robot](https://github.com/k8s-ci-robot/)) applies an `lgtm` label to the PR
- Phase 2: Humans approve the PR
  - The PR **author** `/assign`'s all suggested **approvers** to the PR, and optionally notifies
    them (eg: "pinging @foo for approval")
  - Only people listed in the relevant OWNERS files, either directly or through an alias, as [described
    above](#owners_aliases), can act as **approvers**, including the individual who opened the PR.
  - **Approvers** look for holistic acceptance criteria, including dependencies with other features,
    forwards/backwards compatibility, API and flag definitions, etc
  - If the code changes look good to them, an **approver** types `/approve` in a PR comment or
    review; if they change their mind, they `/approve cancel`
  - [prow](https://prow.k8s.io) ([@k8s-ci-robot](https://github.com/k8s-ci-robot/)) updates its
    comment in the PR to indicate which **approvers** still need to approve
  - Once all **approvers** (one from each of the previously identified OWNERS files) have approved,
    [prow](https://prow.k8s.io) ([@k8s-ci-robot](https://github.com/k8s-ci-robot/)) applies an
    `approved` label
- Phase 3: Automation merges the PR:
  - If all of the following are true:
    - All required labels are present (eg: `lgtm`, `approved`)
    - Any blocking labels are missing (eg: there is no `do-not-merge/hold`, `needs-rebase`)
  - And if any of the following are true:
    - there are no presubmit prow jobs configured for this repo
    - there are presubmit prow jobs configured for this repo, and they all pass after automatically
      being re-run one last time
  - Then the PR will automatically be merged
