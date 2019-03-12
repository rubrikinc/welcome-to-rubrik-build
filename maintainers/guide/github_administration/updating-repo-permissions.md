# Build GitHub Automation

## Adding Permissions

All permissions in `rubrikinc` are controlled via Teams. At a minimum, each repo will have an associated team that matches the name of the reposiotry. We also have teams in place that can span multiple repos.

**Slack Dialog**

| Variable    | Required | Notes                                                                             |
|-------------|----------|-----------------------------------------------------------------------------------|
| Team        | True     | Dynamically populated list                                                        |
| Slack Users | True     | Dynamically populated list -- will be associated with GitHub username in Database |

### Approval

Once the new permission dialog been submitted, a direct message will be sent to the Teams maintainer requesting approval. This message will include the following information:

* Submitter Name
* Users Slack name
* Users GitHub username
* Users GitHub avatar
* Team Name

If the original submitter is the Teams maintainer this step will be skipped.

### Response after approval

A message will be sent to the specific Rubrik User and the Team Maintainer letting them no approval has beeng granted.
