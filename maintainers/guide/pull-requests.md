# Pull Request Process

This doc explains the process and best practices for managing a pull request to a project. It should serve as a reference for all maintainers, and be useful especially to new and infrequent contributors.

The following graphic provides an overview of the PR process: 

![Pull Request Overview](/img/pr-process.png)

## Before You Submit a Pull Request

This guide is for contributors who already have a pull request to submit. If you're looking for information on setting up your developer environment and creating code to contribute to Rubrik Build, see the [development guide](/contributors/devel/development.md).

First time contributors should head to the [Contributor Guide](/contributors/guide/README.md) to get started.

## Pull Requests and the Release Cycle

If a pull request has been reviewed, but held or not approved, it might be due to the current phase in the [Release Management](). Occasionally, a maintainer may freeze their project code base when working towards a specific feature or goal that could impact other development. During this time, your pull request could remain unmerged while their release work is completed.

## Reviewing Pull Requests

If you still aren't getting any pull request love, here are some
things you can do to move the process along:

   * Make sure that your pull request has an assigned reviewer (assignee in GitHub). If not, reply to the pull request comment stream asking for a reviewer to be assigned. 

   * Ping the assignee (@username) on the pull request comment stream, and ask for an estimate of when they can get to the review.

   * Ping the assignee by email (many of us have publicly available email addresses).

   * If you're a member of the organization ping the [team](https://github.com/orgs/rubrikinc/teams) (via @team-name) that works in the area you're submitting code. Typically, this will be the [Build team](https://github.com/orgs/rubrikinc/teams/build).

## Closing Pull Requests

Pull requests older than 90 days will be closed. Exceptions can be made for pull requests that have active review comments, or that are awaiting other dependent pull requests. Closed pull requests are easy to recreate, and little work is lost by closing a pull request that subsequently needs to be reopened. We want to limit the total number of pull requests in flight to:

* Maintain a clean project
* Remove old pull requests that would be difficult to rebase as the underlying code has changed over time
* Encourage code velocity

## Best Practices for Faster Reviews

It's good to keep these best practices in mind when you're making a pull request.

Let's talk about best practices so your pull request gets reviewed quickly.

### 0. Familiarize yourself with project conventions

* [Project Architecture](https://github.com/rubrikinc/welcome-to-rubrik-build/blob/master/maintainers/guide/project-architecture.md)
* [Documentation Style Guide](https://github.com/rubrikinc/welcome-to-rubrik-build/blob/master/maintainers/guide/style-guide-documentation.md)
* [Code Style Guide](https://github.com/rubrikinc/welcome-to-rubrik-build/blob/master/maintainers/guide/style-guide-code.md)

### 1. Smaller Is Better: Small Commits, Small Pull Requests

Small commits and small pull requests get reviewed faster and are more likely to be correct than big ones.

Attention is a scarce resource. Help us review your PRs more quickly by following these guidelines:

1. Try not to touch a large number of files in a single PR if possible.
2. Don't change whitespace or line wrapping in parts of a file you are not editing for other reasons. Make sure your text editor is not configured to automatically reformat the whole file when saving.

### 2. Comments Matter

In your code, if someone might not understand why you did something (or you won't remember why later), comment it. Many code-review comments are about this exact issue.

Likewise, make sure to use PR comments appropriately to detail information needed for review and approval.

### 3. Test

Nothing is more frustrating than starting a review, only to find that the tests are inadequate or absent. Very few pull requests can touch code and NOT touch tests.

If you don't know how to test Feature-X, please ask!  We'll be happy to help you design things for easy testing or to suggest appropriate test cases.

### 4. It's OK to Push Back

It's ok to reject a PR; however, if you do so then ensure to leave appropriate comments. The submitter should be given clear guidelines as to what changes need to be made so that the PR will be accepted next time. 

### 5. Common Sense and Courtesy

No document can take the place of common sense and good taste. Don't be a jerk.