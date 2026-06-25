# codeberg-tool

CLI tool for Codeberg (Forgejo/Gitea). Manage repos, authenticate, push, and mirror — similar to `gh` for GitHub or `glab` for GitLab.

## Install

```bash
sudo cp berg /usr/local/bin/berg
```

## Setup

```bash
# Authenticate with your Codeberg API token
# Generate one at: https://codeberg.org/user/settings/applications
berg auth --token "your_token_here"

# Or via environment variable
export BERG_TOKEN="your_token_here"
```

## Usage

```bash
# Check auth status
berg auth --check

# List your repos
berg repo list

# Create a new repo
berg repo create my-project

# Fork a repo
berg repo fork owner/repo

# Set up remote and push current directory
berg push

# Show repo details
berg repo get owner/repo
```

## Requirements

- Python 3.10+
- `requests`, `click`, `rich`, `pyyaml` (pip packages)

Berg stores its config in `~/.config/berg/config.yml`.

## Notes

Users of the AcreetionOS project: you will need to set up your own remotes
when using the setup scripts. See each project's README for instructions.

**Maintainer:** Natalie (AcreetionOS)
