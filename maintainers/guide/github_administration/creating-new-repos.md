# Build GitHub Automation

## Creating a new repository

Using the `/build-repo` Slack Slash Command, the user will start the new repo creation process. The first step in this process involves checking the users `Slack ID` against an internal database to validate they have the correct permissions to create a new repo. Once that has been validated they will receive a new dialog window with the following information:

| Variable         | Required |
|------------------|----------|
| Rubrik Team      | True     |
| Repo Name        | True     |
| Repo description | True     |

The provided Rubrik team name will determine who is added as the repos `CODEOWNERS` along with who has write permissions to the repo. The only currently supported teams are:

* OCTO
* Engineering

### OCTO Specific Settings

* `CODEOWNERS` file will include `*       @rubrikinc/octo`
* `OCTO` added as a Team on the repo with `write` permissions

### Engineering Specific Settings

*  New GitHub team will be created that matches the name of the repository
* `CODEOWNERS` file will include `*       @rubrikinc/{repo-name}`
* `{repo-creators-github-username}` added to the new team

### Repository Standards

* Naming convention: `{repo-name}` (i.e all lowercase with dashes)
* License: `MIT`
* Default branch: `master`
* Branch protection rules: `enabled` (master)
  * Require pull request reviews before merging: `enabled`
    * Required approving reviews: `1`
    * Dismiss stale pull request approvals when new commits are pushed: `enabled`
    * Require review from Code Owners: `enabled`
  * Require status checks to pass before merging: `enabled` (Note: User will still need to select which status checks are required. By default, none are selected as a requirement.)
    * Require branches to be up to date before merging: `enabled`
  * Require signed commits: `enabled`
  * Include administrators: `disabled`
* Files created
  * top level `README.md`
  * `CODE_OF_CONDUCT.md`
  * `CONTRIBUTING.md`
  * `.github/CODEOWNERS`
  * `.github/pull_request_template.md`
  * `.github/ISSUE_TEMPLATE/bug-report.md`
  * `.github/ISSUE_TEMPLATE/`
  * `.github/enhancement_request.md`
* Labels

## Adding a new user to the `rubrikinc` GitHub organization

**Slack Dialog Variables**

| Variable        | Required | Notes                                                                                                              |
|-----------------|----------|--------------------------------------------------------------------------------------------------------------------|
| Slack Username  | True     | dynamically populated list of all Rubrik Slack users                                                               |
| GitHub Username | True     | entered twice for validation                                                                                       |
| Team            | False    | dynamically populated list of current GitHub teams -- if no team selected the the user will not be added to a team |

### Approval

Once the new user dialog has been submitted, a direct message will be sent to the `rubrikinc` organization owners requesting approval. This message will include the following information:

* Submitter Name
* New users GitHub username
* The team the new user will be added to
* The new users GitHub avatar
* Wheter or not a new GitHub user seat will need to be purchased

#### Approved

A direct message will be sent to the provided `Slack Username` informing them that they have been added to the `rubrikinc` organization along with the team they have been added to if applicable. If the request was not submitted by the new user, a similar message will be sent to the requester.

We will also update an internal database with the users information which may be useful for additional automation workflows.

#### Not approved

A direct message will be sent to the provided `Slack Username` letting them know their request has not be approved and that they should reach out to the Rubil Build owner team for additional information.
