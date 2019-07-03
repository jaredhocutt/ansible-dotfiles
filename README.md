# Dotfiles

This role handles installing the dotfiles repo for Jared Hocutt and then
enabling the specified dotfiles from that repo.

## Requirements

The hosts you are targeting should have the following packages:

- git >= 1.7.1
- python >= 2.6
- python-dnf

## Role Variables


| Variable                  | Required | Default | Description                                                                     |
| ------------------------- | -------- | ------- | ------------------------------------------------------------------------------- |
| dotfiles_enabled | &#9989; | `[]` | A list of dotfiles to enable.<br><br>Each item in the list should be a dictionary containing a `name` and `dotfile`. |

## Dependencies

None

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: jaredhocutt.vscode
      vars:
        dotfiles_enabled:
          - name: git
            dotfile: ~/.gitconfig
          - name: vim
            dotfile: ~/.vimrc
          - name: zsh
            dotfile: ~/.zshrc

```

## License

MIT

## Author Information

Jared Hocutt (@jaredhocutt)
