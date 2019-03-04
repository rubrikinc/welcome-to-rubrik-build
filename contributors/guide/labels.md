# Using Labels

Labels are a highly useful feature of GitHub that allows for metadata to be appended to projects, issues, pull requests, and so forth. Rubrik Build makes heavy use of labels in order to drive automated tasks and express intent.

Labels will be structured in the following manner:

```
label_major-label_minor
```

The labels available are as follows:


| **Major**     | **Minor**                                                                                                                                                                          | **Description & Color Code**                                                                                                                    | **Type** |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| `area`        | rcdm <br><br>  polaris <br><br> partner                                                                                                                                              | The functional area. <br><br> #84b6eb                                                                                                           | Issue    |
| `exp`         | beginner <br><br> intermediate <br><br> expert <br>                                                                                                                                  | The expertise necessary. <br><br>  #ffc5a8                                                                                                      | Issue    |
| `first-timer` | n/a                                                                                                                                                                                | Indicates an Issue that is reserved for a complete novice user. <br><br>  #51ef63                                                               | Issue    |
| `help-wanted` | n/a                                                                                                                                                                                | Indicates a need for investment. <br><br>  #159818                                                                                              | Issue    |
| `kind`        | bug <br><br> docs <br><br> enhancement <br><br> experimental <br><br> feature <br><br> question <br>                                                                                       | Indicates the type of Issue. <br><br>  #b5152d                                                                                                  | Issue    |
| `platform`    | windows <br><br> linux <br><br> mac                                                                                                                                                  | Indicates a platform requirement or association. <br><br>  #cccccc                                                                              | Issue    |
| `priority`    | p0 <br><br> p1 <br><br> p2 <br><br> p3                                                                                                                                                 | Indicates the priority level when determining where to invest effort.  All customer specific requests should be marked as p0. <br><br>  #fbca04 | Issue    |
| `roadmap`     | n/a                                                                                                                                                                                | Indicates an item that will be addressed in the future roadmap. <br><br>  #0b008c                                                               | Issue    |
| `resolution`  | answered <br><br> by-design <br><br> duplicate <br><br> external <br> fixed <br><br> won't-fix                                                                                         | Indicates the status of the issue. <br><br>  #ffdddd                                                                                            | Issue    |
| `status`      | failing-ci <br><br> more-info-needed <br><br> needs-attention <br><br> needs-vendoring <br><br> 0-triage <br><br> 1-design-review <br><br> 2-code-review <br><br> 3-code-review <br><br> 4-merge | Indicates the status of the PR. <br><br>   #006b75 & #004b75                                                                                    | PR       |
| `version`     | master <br><br> {versions}                                                                                                                                                         | Indicates the affected version. <br><br>  #b2482a                                                                                               | Issue    |

## Example 1 
An Issue is submitted that requires a bug fix to one of our SDK projects. It’s not easy enough for a first time developer to fix, but also doesn’t require expert level expertise. After reviewing the bug with the team, we determine it’s a P1 priority.

* Issue Labels: kind-bug, exp-intermediate, priority-p1
* PR Labels: status-* (handled by CI tool)

## Example 2 
An Issue is submitted that highlights a broken link in our documentation. It’s a trivial fix to perform and affects those using a Windows desktop machine.

* Issue Labels: kind-docs, platform-windows
* PR Labels: status-* (handled by CI tool)
