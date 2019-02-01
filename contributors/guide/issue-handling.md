# Issue Submission

Issues are used to keep track of bugs, enhancements, questions, documentation, or other requests. Any GitHub user can create an issue in a public repository where issues aren’t disabled.

|**NOTE:** See [documentation](https://help.github.com/articles/creating-an-issue/) for how to create an issue.|
|---|

## Overview

The high level workflow for Issue handling is as follows:

1. **Submit:** Someone submits an Issue to a project on GitHub.

    * This generates an alert to the project maintainer(s) and any linked Slack channels.
    
2. **Review:** The project maintainers and any linked Bots inspect the Issue to provide labels.

    * The issue is assigned a Priority level.
    * The issue is optionally assigned any other labels needed to describe and categorize the issue. For more information, see the Labels section.
    
3. **Discuss:** Project maintainers respond with any needed information to address gaps in the Issue.

    * Ideally, we are responding within 24 business hours with reassurance that we’ve read the issue. This can also be coordinated with a Bot.
    
4. **Decide:** Project maintainers ultimately commit or decline the Issue.

    * For declined Issues, a clearly defined reason should be stated.
    * For committed Issues, the steps necessary to resolve the Issue should be stated.
    
5. **Resolve:** Once a Pull Request is submitted to resolve a committed Issue, an association between the Issue and Pull Request is generated.

    * Closing the PR will automatically close the Issue.

## Issue Submission Template

Each repository will contain files in the `.github` folder for `Bug Report` and `Enhancement Request` templates. This is a special folder that will insert a form, written in markdown, into the start of a new issue. The user submitting the issue then follows the form to ensure all necessary information has been gathered for review of the issue.
