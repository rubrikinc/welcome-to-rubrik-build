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
