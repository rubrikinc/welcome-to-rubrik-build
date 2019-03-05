|---
IN PROGRESS
---|

# Release Cycle Management

If you want your PR to get merged, it needs the following required labels and milestones, represented here by the Prow /commands it would take to add them:
<table>
<tr>
<td></td>
<td>Normal Dev</td>
<td>Code Freeze and Review</td>
<td>Release</td>
</tr>
<tr>
<td></td>
<td>Weeks 1-8</td>
<td>Weeks 9-11</td>
<td>Weeks 11+</td>
</tr>
<tr>
<td>Required Labels</td>
<td>
<ul>
<!--Weeks 1-8-->
<li>/sig {name}</li>
<li>/kind {type}</li>
<li>/lgtm</li>
<li>/approved</li>
</ul>
</td>
<td>
<ul>
<!--Weeks 9-11-->
<li>/milestone {v1.y}</li>
<li>/sig {name}</li>
<li>/kind {bug, failing-test}</li>
<li>/priority critical-urgent</li>
<li>/lgtm</li>
<li>/approved</li>
</ul>
</td>
<td>
<!--Weeks 11+-->
Return to 'Normal Dev' phase requirements:
<ul>
<li>/sig {name}</li>
<li>/kind {type}</li>
<li>/lgtm</li>
<li>/approved</li>
</ul>

Merges into the 1.y branch are now via cherrypicks, approved by release branch manager.
</td>
<td>
<ul>
</td>
</tr>
</table>

The general labeling process should be consistent across artifact types.

---

## The Release Cycle

Rubrik Build releases currently happen bi-weekly.  The release process can be thought of as having three main phases:

* Feature Definition and Implementation
* Code Review
* Release 

