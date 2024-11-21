# ITS Propagation Library Wiki Contribution Guide

Thank you for your interest in contributing to this wiki. This document was adapted
from [GitHub's own](https://github.com/github/docs/blob/main/.github/CONTRIBUTING.md),
and provides guidelines and helpful links.

In this guide you will get an overview of the contribution workflow from opening
an issue, creating a PR, reviewing, and merging the PR. The workflow we recommend
and describe here follows from best and common practices in the Git and GitHub
ecosystems. We aim to leverage this workflow, especially the elements of code review
and approval, to enable open source development of a robust, high quality wiki for
the ITS Propagation Library.

## Background for new contributors

Here are some resources to help you get started with open source contributions:

- [Set up Git](https://docs.github.com/en/get-started/getting-started-with-git/set-up-git)
- [GitHub flow](https://docs.github.com/en/get-started/using-github/github-flow)
- [Collaborating with pull requests](https://docs.github.com/en/github/collaborating-with-pull-requests)

## Getting Started

### Issues

#### Create a new issue

If you spot a problem with the wiki,
[search if an issue already exists](https://docs.github.com/en/github/searching-for-information-on-github/searching-on-github/searching-issues-and-pull-requests#search-by-the-title-body-or-comments).
If a related issue doesn't exist, we encourage you to open one (even if you don't
plan to contribute a resolution yourself). Issues may be opened for content requests,
typos, erroneous content, or anything else which you think should be changed.

#### Solve an issue

Scan through our existing issues to find one that interests you. You can narrow
down the search using `labels` as filters. You may wish to comment on the issue
to let others know if you plan to resolve it with a pull request.

### Make Changes

1. Fork the repository.
    - Using GitHub Desktop:
      - [Getting started with GitHub Desktop](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop/getting-started-with-github-desktop)
      will guide you through setting up Desktop.
      - Once Desktop is set up, you can use it to [fork the repo](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/cloning-and-forking-repositories-from-github-desktop)!

    - Using the command line:
      - [Fork the repo](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo#fork-an-example-repository)
      so that you can make your changes without affecting the original project until
      you're ready to merge them.

1. Install and set up [Quarto](https://quarto.org/docs/get-started/) by following
their guide.

1. Create a working branch and start with your changes! Use Quarto to preview how
the changes will render when the site is deployed.

### Commit your update

Commit the changes once you are happy with them.

### Pull Request

When you're finished with the changes, create a pull request, also known as a PR.

- Write a meaningful description of the changes you've made.
- Don't forget to [link PR to issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue)
if you are solving one.
- Enable the checkbox to [allow maintainer edits](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/allowing-changes-to-a-pull-request-branch-created-from-a-fork)
so the branch can be updated for a merge.
Once you submit your PR, a Docs team member will review your proposal. We may ask
questions or request additional information.
- We may ask for changes to be made before a PR can be merged, either using
[suggested changes](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/incorporating-feedback-in-your-pull-request)
or pull request comments. You can apply suggested changes directly through the UI.
You can make any other changes in your fork, then commit them to your branch.
- As you update your PR and apply changes, mark each conversation as [resolved](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/commenting-on-a-pull-request#resolving-conversations).
- If you run into any merge issues, checkout this
[git tutorial](https://github.com/skills/resolve-merge-conflicts) to help you
resolve merge conflicts and other issues.

### Your PR is merged

When your PR is approved and merged, your changes will automatically be deployed
to the live wiki site.

## Updating USWDS

This repository contains static elements from the [U.S. Web Design System](https://designsystem.digital.gov/),
but does not use the recommended installation method with Node and npm. Instead, the static files are
included directly from GitHub. To update to a newer release of USWDS, follow these steps:

1. Check the current version of the USWDS assets included in this repository.
The version number is shown in a comment at the top of `uswds/css/usdws.css`.

1. Check if a newer version of the USWDS is available [here](https://github.com/uswds/uswds/releases)

1. If a new release is available, review the included changelog to determine if any breaking changes
need to be accounted for as part of your update. Most likely, there will not be any, since this site
uses relatively few USWDS components. If there are, make the necessary modifications to support the
newer version of the USWDS.

1. Download the new release (`.tgz`) and extract it. Copy the contents of `package/dist/` to this
repository's `usdws` directory. Overwrite all conflicted files. The rest of the files from the downloaded
release can be discarded.

1. Test the site by rendering with Quarto. Ensure that the USWDS components have not broken.

1. Commit your changes, and open a pull request.
