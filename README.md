# GitHub CLI (`gh`) Commands Reference

A comprehensive list of `gh` commands for working with GitHub from the terminal.

---

## Authentication

| Command | Description |
|---|---|
| `gh auth login` | Log in to GitHub |
| `gh auth logout` | Log out of GitHub |
| `gh auth status` | View authentication status |
| `gh auth refresh` | Refresh authentication token |
| `gh auth token` | Print the current auth token |

---

## Configuration

| Command | Description |
|---|---|
| `gh config list` | List all configuration settings |
| `gh config get <key>` | Get the value of a config key |
| `gh config set <key> <value>` | Set a configuration value |
| `gh config set editor <editor>` | Set default editor (e.g. `vim`, `nano`, `code`) |
| `gh config set git_protocol <protocol>` | Set Git protocol: `https` or `ssh` |
| `gh config set prompt enabled` | Enable interactive prompts |
| `gh config set prompt disabled` | Disable interactive prompts |
| `gh config set pager <pager>` | Set pager (e.g. `less`, `more`) |
| `gh config set browser <browser>` | Set default browser |
| `gh config set http_unix_socket <path>` | Set Unix socket for HTTP |

### Common `gh config set` Examples

```bash
# Set default editor
gh config set editor "code --wait"

# Use SSH instead of HTTPS for Git operations
gh config set git_protocol ssh

# Disable interactive prompts (useful in CI)
gh config set prompt disabled

# Set a custom pager
gh config set pager "less -R"

# Apply setting for a specific host
gh config set git_protocol ssh --host github.com
```

> Config is stored at `~/.config/gh/config.yml`

---

## Repository

| Command | Description |
|---|---|
| `gh repo create` | Create a new repository |
| `gh repo clone <repo>` | Clone a repository |
| `gh repo fork <repo>` | Fork a repository |
| `gh repo view [repo]` | View repository details |
| `gh repo list [owner]` | List repositories |
| `gh repo delete <repo>` | Delete a repository |
| `gh repo rename <name>` | Rename a repository |
| `gh repo archive <repo>` | Archive a repository |
| `gh repo sync` | Sync a fork with its upstream |

---

## Pull Requests

| Command | Description |
|---|---|
| `gh pr create` | Create a pull request |
| `gh pr list` | List pull requests |
| `gh pr view [number]` | View a pull request |
| `gh pr checkout <number>` | Check out a pull request branch |
| `gh pr merge [number]` | Merge a pull request |
| `gh pr close [number]` | Close a pull request |
| `gh pr reopen [number]` | Reopen a closed pull request |
| `gh pr review [number]` | Add a review to a pull request |
| `gh pr diff [number]` | View the diff of a pull request |
| `gh pr comment [number]` | Add a comment to a pull request |
| `gh pr status` | Show PR status for current branch |
| `gh pr edit [number]` | Edit a pull request |
| `gh pr ready [number]` | Mark a draft PR as ready |

---

## Issues

| Command | Description |
|---|---|
| `gh issue create` | Create a new issue |
| `gh issue list` | List issues |
| `gh issue view <number>` | View an issue |
| `gh issue close <number>` | Close an issue |
| `gh issue reopen <number>` | Reopen a closed issue |
| `gh issue edit <number>` | Edit an issue |
| `gh issue comment <number>` | Add a comment to an issue |
| `gh issue status` | Show issue status |
| `gh issue delete <number>` | Delete an issue |
| `gh issue pin <number>` | Pin an issue |
| `gh issue unpin <number>` | Unpin an issue |
| `gh issue transfer <number> <repo>` | Transfer issue to another repo |
| `gh issue develop <number>` | Create a branch for an issue |

---

## Workflows & Actions

| Command | Description |
|---|---|
| `gh workflow list` | List workflows |
| `gh workflow view [workflow]` | View a workflow |
| `gh workflow run <workflow>` | Trigger a workflow |
| `gh workflow enable <workflow>` | Enable a workflow |
| `gh workflow disable <workflow>` | Disable a workflow |
| `gh run list` | List workflow runs |
| `gh run view [run-id]` | View a workflow run |
| `gh run watch [run-id]` | Watch a workflow run in real-time |
| `gh run rerun [run-id]` | Rerun a workflow run |
| `gh run cancel [run-id]` | Cancel a workflow run |
| `gh run download [run-id]` | Download run artifacts |
| `gh run delete [run-id]` | Delete a workflow run |

---

## Releases

| Command | Description |
|---|---|
| `gh release create <tag>` | Create a new release |
| `gh release list` | List releases |
| `gh release view [tag]` | View a release |
| `gh release edit <tag>` | Edit a release |
| `gh release delete <tag>` | Delete a release |
| `gh release upload <tag> <files>` | Upload assets to a release |
| `gh release download [tag]` | Download release assets |

---

## Gists

| Command | Description |
|---|---|
| `gh gist create [files]` | Create a new gist |
| `gh gist list` | List gists |
| `gh gist view [id]` | View a gist |
| `gh gist edit [id]` | Edit a gist |
| `gh gist delete [id]` | Delete a gist |
| `gh gist clone <id>` | Clone a gist |

---

## SSH Keys & GPG Keys

| Command | Description |
|---|---|
| `gh ssh-key list` | List SSH keys |
| `gh ssh-key add <key-file>` | Add a new SSH key |
| `gh ssh-key delete <id>` | Delete an SSH key |
| `gh gpg-key list` | List GPG keys |
| `gh gpg-key add <key-file>` | Add a new GPG key |
| `gh gpg-key delete <id>` | Delete a GPG key |

---

## Codespaces

| Command | Description |
|---|---|
| `gh codespace create` | Create a new codespace |
| `gh codespace list` | List codespaces |
| `gh codespace code` | Open a codespace in VS Code |
| `gh codespace ssh` | SSH into a codespace |
| `gh codespace delete` | Delete a codespace |
| `gh codespace stop` | Stop a codespace |
| `gh codespace ports` | List forwarded ports |

---

## Projects

| Command | Description |
|---|---|
| `gh project list` | List projects |
| `gh project view <number>` | View a project |
| `gh project create` | Create a new project |
| `gh project delete <number>` | Delete a project |
| `gh project edit <number>` | Edit a project |
| `gh project item-list <number>` | List project items |
| `gh project item-add <number>` | Add item to a project |

---

## Secrets & Variables

| Command | Description |
|---|---|
| `gh secret list` | List secrets |
| `gh secret set <name>` | Set a secret |
| `gh secret delete <name>` | Delete a secret |
| `gh variable list` | List variables |
| `gh variable set <name>` | Set a variable |
| `gh variable delete <name>` | Delete a variable |

---

## Labels

| Command | Description |
|---|---|
| `gh label list` | List labels |
| `gh label create <name>` | Create a label |
| `gh label edit <name>` | Edit a label |
| `gh label delete <name>` | Delete a label |
| `gh label clone <repo>` | Clone labels from another repo |

---

## Search

| Command | Description |
|---|---|
| `gh search repos <query>` | Search repositories |
| `gh search prs <query>` | Search pull requests |
| `gh search issues <query>` | Search issues |
| `gh search commits <query>` | Search commits |
| `gh search code <query>` | Search code |

---

## Aliases

| Command | Description |
|---|---|
| `gh alias list` | List aliases |
| `gh alias set <name> <expansion>` | Create an alias |
| `gh alias delete <name>` | Delete an alias |

---

## Extensions

| Command | Description |
|---|---|
| `gh extension list` | List installed extensions |
| `gh extension install <repo>` | Install an extension |
| `gh extension upgrade [extension]` | Upgrade an extension |
| `gh extension remove <name>` | Remove an extension |
| `gh extension search <query>` | Search for extensions |

---

## Global Flags

These flags work with most `gh` commands:

| Flag | Description |
|---|---|
| `--help` | Show help for a command |
| `--repo <repo>` | Target a specific repository |
| `--json <fields>` | Output in JSON format |
| `--jq <expression>` | Filter JSON output with jq |
| `--template <string>` | Format output with Go template |
| `-R, --repo` | Select another repository |
| `--hostname` | Target a specific GitHub hostname |

---

## Useful Tips

```bash
# Open any view in the browser
gh pr view 42 --web
gh issue view 10 --web
gh repo view --web

# Filter lists
gh pr list --state closed --author "@me"
gh issue list --label "bug" --assignee "@me"

# Output as JSON and pipe to jq
gh pr list --json number,title,state | jq '.[] | select(.state == "OPEN")'
```

---

> **Docs:** https://cli.github.com/manual  
> **Install:** `brew install gh` or see https://github.com/cli/cli#installation
