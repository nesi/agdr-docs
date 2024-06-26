---
title: Contributing
---

**[CLICK TO VIEW THIS PAGE RENDERED IN MKDOCS](https://nesi.github.io/agdr-docs/CONTRIBUTING)**{ .hidden }

!!! prerequisite "See also"
    - For examples of markdown use, [see FORMAT](FORMAT.md).
    - For information about page creation, [see NEWPAGE](NEWPAGE.md).

Any changes made should be merged via a pull request.

## Minor edits through GitHub

Press `.`, will open up Visual Studio Code in browser.

## Major edits through GitHub

This repository has been configured to be usable with [GitHub Codespaces](https://github.com/features/codespaces).
It allows accessing a full featured preconfigured development environment remotely, without installing anything on your local machine.

Clicking on the following link will open a VS Code instance ready to be used with the latest version of the documentation files.

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/nesi/agdr-docs?quickstart=1)

## Local Development Environment

A local development environment is not required to make doc edits, but if you are making lots of changes, the real time rendering can be quite helpful.

### First Time Setup

You will need to have Python **3.10** or later installed on your computer.

Clone this repository and create a Python virtual environment using:

```sh
git clone https://github.com/nesi/agdr-docs.git
cd agdr-docs
python -m venv .venv
source .venv/bin/activate
pip3 install -r requirements.txt
```

### Make Development Branch

```sh
git checkout -b my_development_branch
```

### Build and deploy

```sh
source .venv/bin/activate
mkdocs serve -c
```

Take note of any warnings or errors.

A link to the deployment will be printed once served.

### VS Code configuration

You can use any IDE you want, but various tools have been configured for use with VS Code.

#### Recommended Extensions

When opening the workspace for the first time, you should be prompted to install the <a href="https://github.com/nesi/agdr-docs/blob/main/.vscode/extensions.json">Recommended VS Code Plugins</a>.

#### Snippets

`ctrl` + `space` can be used to aid by auto-completing.

e.g. starting to type an image include `![my image](` then pressing `ctrl` + `space` will show all the valid paths.

Custom snippets can be added in <a href="https://github.com/nesi/agdr-docs/blob/main/.vscode/includes.code-snippets.json">`../.vscode/includes.code-snippets`</a>

#### Tasks

Some of the same checks run during the GitHub CI, can also be run in VS Code.

This is shown with word underlining, and in the 'PROBLEMS' tab in the terminal.

Tasks allow continuous checks to be run in the background, these can be defined in <a href="https://github.com/nesi/agdr-docs/blob/main/.vscode/tasks.json">`../.vscode/tasks.json`</a>, also include in <a href="https://github.com/nesi/agdr-docs/blob/main/.vscode/settings.json">`../.vscode/settings.json`</a> in order to trigger on save.

## Making a Merge Request

The `main` branch is protected, changes can be made via a pull request.

Make a pull request for your development branch into `main`.

If you are using a local development environment,

```sh
git checkout -b <branchname>
```

When you are done with your changes

```sh
git push origin <branchname>
```

CI checks will run on your branch, you can check them under 'Actions'
Might be worth having a quick look at these before making a pull request.

Make a pull [request](https://github.com/nesi/agdr-docs/pulls)

Assign a reviewer if you wish.

Pull will merge automatically if all checks passed. (add timer too maybe?)

## Reviewing A Merge Request

Under the 'pull requests' tab, open one of the pending requests.

Clicking on the 'Files Changed' tab, will give a convenient diff of the changes, as well as inline errors identified by the CI checks.

If some of the CI checks failed (make sure they are not important ones), you will have to click the  `Merge without waiting for requirements to be met (bypass branch protections)` button before proceeding with the merge.

Feel free to raise an issue, make a proposal or [add words to the dictionary](#adding-words-to-dictionary) if you feel you are being unfairly targeted by the CI checks.

## Update Remote Assets

Certain files need to be fetched from other repos for up to date info. This will be automated, but for not the proccess is manual.

1. Run the [![Fetch Remote Assets](https://github.com/nesi/agdr-docs/actions/workflows/fetch_includes.yml/badge.svg?branch=main&event=workflow_run)](https://github.com/nesi/agdr-docs/actions/workflows/fetch_includes.yml) workflow in this repo.
2. A branch `new-assets` will be created, which can be merged into main.

## Adding Words to Dictionary

If the CI is failing the spellcheck phase, and you believe the identified words are not typos, (double check your capitalisation and apostrophes first) you can update the dictionary being used.

1. Visit the [NeSI Word List](https://github.com/nesi/nesi-wordlist), follow the instructions there on adding words.
2. Once changes to the word list have been merged, return to this repo and run [update remote assets](#update-remote-assets).
3. You should see your new words in the [Dictionary](assets/glossary/dictionary.txt) if your words included a definition, they will also be in the <a href="https://github.com/nesi/agdr-docs/blob/main/overrides/Glossary.md">Glossary</a>.

## Raise an issue

*Not documented at the moment (TODO)*
