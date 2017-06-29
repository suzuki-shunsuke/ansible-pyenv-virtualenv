# ansible-pyenv-virtualenv

[![Build Status](https://travis-ci.org/suzuki-shunsuke/ansible-pyenv-virtualenv.svg?branch=master)](https://travis-ci.org/suzuki-shunsuke/ansible-pyenv-virtualenv)

ansible role to install pyenv-virtualenv.

* [suzuki-shunsuke.pyenv-virtualenv](https://galaxy.ansible.com/suzuki-shunsuke/pyenv-virtualenv/)

## Requirements

* git
* pyenv

## Role Variables

name | required | default | description
--- | --- | --- | ---
pyenv_root | no | $PYENV_ROOT >> $HOME/.pyenv | If pyenv_virtualenv_root is defined, this variable is ignored.
pyenv_virtualenv_root | no | pyenv_root | If this variable is undefined, pyenv_root is used.
pyenv_virtualenv_rc_path | no | "NOT ADD" | By default configuration is not added

## Dependencies

Nothing.

## Example Playbook

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.pyenv-virtualenv
    pyenv_root: "{{ ansible_env.HOME }}/.ghq/github.com/pyenv/pyenv"
    pyenv_virtualenv_rc_path: "{{ ansible_env.HOME }}/.bashrc"
```

## License

[MIT](LICENSE)
