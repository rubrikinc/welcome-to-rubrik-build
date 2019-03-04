# Issue Triage Guidelines

Speed up issue management.

The issues are listed on the Projects tab at the organization level. Project boards are in use to track and manage issues as well as pull requests. 

* [Rubrik-SDK-Tracking](https://github.com/orgs/rubrikinc/projects/1)
* [Rubrik-Integration-Tracking](https://github.com/orgs/rubrikinc/projects/2)

## Labels

Use labels! A detailed list of labels can be found [here](). 

While working on triaging issues, you may not have privilege to assign a specific label and in that case simply add a comment in the issue with your findings.

Most people can leave comments and open issues. They don't have the ability to set labels, change milestones, and close other peoples issues. As a maintainer, you will need to ensure that proper labels are applied.

## Support Requests

Sometimes users ask for support requests in issues; these are usually requests from people who need help configuring some aspect of Kubernetes. These issues should be labeled with `support` and directed to appropriate support personnel. Keep in mind

Support requests should be directed to the following:

* User documentation
* Support portal (if customer)

## Define priority

We use GitHub issue labels for prioritization. The absence of a priority label means the bug has not been reviewed and prioritized yet.

We try to apply these priority labels consistently across the entire project, but if you notice an issue that you believe to be incorrectly prioritized, please do let us know and we will evaluate your counter-proposal.

- **priority/p0**: Must be actively worked on as someone's top priority right now. Stuff is burning. If it's not being actively worked on, someone is expected to drop what they're doing immediately to work on it. Owners are responsible for making sure that all the issues, labeled with this priority, in their area are being actively worked on. Examples include
user-visible bugs in core features, broken builds or tests and critical security issues.

- **priority/p1**: Must be staffed and worked on either currently, or very soon, ideally in time for the next release.

- **priority/p2**: Important over the long term, but may not be currently staffed and/or may require multiple releases to complete.

- **priority/p3**: There appears to be general agreement that this would be good to have, but we may not have anyone available to work on it right now or in the immediate future. Community contributions would be most welcome in the mean time (although it might take a while to get them reviewed if reviewers are fully occupied with higher priority issues, for example immediately before a release).

## Set Ownership

If you think you can fix the issue and you are an issue reporter or an organization member, assign it to yourself. If you can not self-assign, leave a comment that you are willing to work on it and work on creating a PR.

## Reminders

If you see any issue which is owned by a developer but a PR is not created in 30 days, a maintainer should contact the issue owner and ask for PR or release ownership as needed.

## Closing Issues
Issues that are identified as a support request, duplicate, not-reproducible or lacks enough information from reporter should be closed following guidelines explained in this file. Also, any issues that can not be resolved because of any particular reason should be closed. These issues should have one or more of following self-readable labels:

* `resolution/answered` - indicates that the support request was answered.
* `resolution/duplicate`- indicates an issue is a duplicate of other open issue.
* `status/more-info-needed` - indicates an issue needs more information in order to work on it.
* `resolution/won't-fix` - indicates an issue that can not be resolved.

## Help Wanted Issues

We use two labels `first-timer` and `exp/beginners` to identify issues that have been specially groomed for new contributors.

We have specific [guidelines](/maintainers/guide/labels.md) for how to use these labels. 
