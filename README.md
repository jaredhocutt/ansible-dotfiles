# Dotfiles

Clones my dotfile repo and enables the dotfiles specified by the user.

## Requirements

None

## Role Variables

| Variable           | Required           | Default | Description                                                                                                            |
| ------------------ | ------------------ | ------- | ---------------------------------------------------------------------------------------------------------------------- |
| `dotfiles_enabled` | :heavy_check_mark: | `[]`    | The list of dotfiles to enable. Each item in the list should have a `name` and `dotfile` (see example playbook below). |

## Dependencies

None

## Example Playbook

```yaml
- hosts: localhost
  vars:
    dotfiles_enabled:
      - name: git
        dotfile: ~/.gitconfig
      - name: vim
        dotfile: ~/.vimrc
      - name: zsh
        dotfile: ~/.zshrc
  roles:
      - jaredhocutt.dotfiles
```
