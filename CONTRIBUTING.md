# Contributing

Contributions (pull requests, feature requests, and so on) are accepted on project Github.com page. Creating Issue before pull request is preffered. Acceptation is not automatic, project management can reject it, or request changes.

Issues (bugs and feature request) reports are accepted on project Github.

## Getting Started

These instructions will get you a copy of the role for your Ansible playbook. Once launched, it will install Mealie.

### Prerequisities

Ansible 5.2.0 version installed.

Molecule 3.x.x version installed.

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with [Docker](https://www.docker.com/) as driver and [Goss](https://github.com/aelsabbahy/goss) as verifier.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

```yml
- src: ansible-role-mealie
  version: 1.0.0
  name: laurivan.mealie
```

Install the role with ansible-galaxy command:

```sh
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```yml
---
- hosts: someserver
  roles:
    - role: laurivan.mealie
```

## Usage

Look to the [defaults](defaults/main.yml) properties file to see the possible configuration properties, it is very likely that you will not need to override any variables.

## Testing

### Install dependencies

```sh
pipenv sync
```

For more information read the [pipenv docs](https://pipenv-fork.readthedocs.io/en/latest/).

### Run test

```sh
pipenv run molecule test 
```

## Versioning

For the versions available, see the [tags on this repository](https://git.laurivan.com/Dev/ansible-role-mealie/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.
