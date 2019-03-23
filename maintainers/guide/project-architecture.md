# Project Architecture

The look and feel of each published project is important. Consistency is key. All existing and new projects should contain several mandatory items, such as a Code of Conduct, templates for GitHub flow, MIT licensing, and guidelines for contributing. 

This page is intended to provide all information required to begin a new project. 

## Basics

All new and existing projects must contain the following: 

* [README](/maintainers/guide/sample-readme.md)
* [Code of Conduct](/code-of-conduct.md)
* [MIT licensing](/LICENSE)
* [Contributing  Guidelines](/CONTRIBUTING.md)
* `.github` folder containing the following templates:

    * [Bug Report](/Templates/bug-report.md) 
    * [Enhancement Request](/Templates/enhancement_request.md)
    * [Pull Request](/Templates/pull_request_template.md)

* [Release Notes](/maintainers/guide/release-notes.md)
* `docs` folder containing the following:

    * Quick Start Guide - document intended to provide a way for a contributor or user to easily get started consuming the project
    * Documentation - a collection of markdown files that can be aggregated as a Gitbook to provide a thorough understanding of all functions and options available. This is not required for Uses Cases, but is for SDKs and Integrations
    * `docs/img` - this folder will hold all images used in documentation, quick start, and README

## README

The README file is generally the first thing seen by a new contributor. Thus making it very important to be welcoming and easy to read and navigate. 

At a minimum, it should clearly state what the project does, any prerequisites, links to documentation (and quick start guide, blogs, getting started videos, etc.), the code of conduct, licensing, and how to contribute. 

Don't be afraid to use emojis or be lighthearted. Exude the friendly helpfulness that will encourage others to contribute. An example README can be found [here](/maintainers/guide/sample-readme.md).

## Contributor Resources

Three files in each repo make up contributor resources:

* Code of Conduct: Contributors Covenant
* License: MIT
* [Contributing  Guidelines](/CONTRIBUTING.md)

These resources are recommended by Rubrik's legal team and are a required component of each project. Please clear any variations by emailing build@rubrik.com.

The CONTRIBUTING.md file provides a boilerplate statement that is required. However, as a maintainer, feel free to add additional verbiage about how and where a contributor can help out and be involved in the project. 