# instrum

Some of my small scripts, commands, and utilities I use for my Linux setup.

Scripts are organized into categories, with each top-level directory acting as a
GNU Stow package. This makes it easy to install all tools or only the categories
you need.

## Requirements

- GNU Stow

## Installation

Clone the repository:

```sh
git clone https://github.com/glymphie/instrum.git
cd instrum
```

Install the packages:

```sh
stow -t "$HOME" */
```

Or install a specific package:

```sh
stow -t "$HOME" utilities
```

This links the scripts into:

```text
~/.local/bin
```

> [!NOTE]
> Make sure `~/.local/bin` is included in `PATH`.

## Structure

## Development

Scripts should be executable:

```sh
chmod +x <package>/.local/bin/<script>
```

This repository uses pre-commit with gitleaks to help prevent committing secrets.

Install the Git hooks:

```sh
pre-commit install
```

Run the hooks manually:

```sh
pre-commit run --all-files
```
