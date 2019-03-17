# Development Guide

Contributions via GitHub pull requests are gladly accepted from their original author. Along with any pull requests, please state that the contribution is your original work and that you license the work to the project under the project's open source license. Whether or not you state this explicitly, by submitting any copyrighted material via pull request, email, or other means you agree to license the material under the project's open source license and warrant that you have the legal authority to do so.

## Common Environment Setup

1. Clone the repository
2. Change directory to the repository root dir
3. Switch to the `devel` branch
4. Create a virtual environment
5. Activate the virtual environment
6. Install the SDK from Source

## New Function Development

Each function should meet the following requirements:

* Each function **must be idempontent**. Before making any configuration changes (post, patch, delete), you should first check to see if that change is necessary. If it's not, you must return a message formated as `No change required. {message}:` For example, the `assign_sla` function first checks to see if the Rubrik object is already assigned to the provided SLA Domain.
* Each API call made in the function should have a log call made explaining what the API call is doing. The log message should be formated as `function_name: message`.
* Each function also must have associated documentation.


Once a new function has been added you will then submit a new Pull Request which will be reviewed before merging into the `devel` branch.