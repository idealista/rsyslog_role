![Logo](https://raw.githubusercontent.com/idealista/rsyslog_role/master/logo.gif)

[![Build Status](https://travis-ci.org/idealista/rsyslog_role.png)](https://travis-ci.org/idealista/rsyslog_role)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-idealista.rsyslog__role-B62682.svg)](https://galaxy.ansible.com/idealista/rsyslog_role)

# RSYSLOG Ansible role

This Ansible role installs a RSYSLOG server in a Debian environment.

- [Getting Started](#getting-started)
	- [Prerequisities](#prerequisities)
	- [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

## Getting Started

These instructions will get you a copy of the role for your Ansible playbook. Once launched, it will install a [RSYSLOG](https://www.rsyslog.com/) server in a Debian system.

### Prerequisities

Ansible 4.0.0 version installed.
Inventory destination should be a Debian environment.

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with [Docker](https://www.docker.com/) as driver.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

```
- src: idealista.rsyslog_role
  version: 2.2.0
  name: rsyslog
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```
---
- hosts: someserver
  roles:
    - { role: rsyslog }
```

## Usage

Look to the [defaults vars](defaults/main.yml) file to see the possible configuration vars.

## Testing

```
$ pipenv sync
$ MOLECULE_DISTRO=(debian8|debian9|debian10) pipenv run molecule test
```

Note: Debian9 (Debian Stretch) will be used as default linux distro if none is provided.

See [molecule.yml](https://github.com/idealista/rsyslog_role/blob/master/molecule/default/molecule.yml) to check possible testing platforms.

## Built With

![Ansible](https://img.shields.io/badge/ansible-4.0.0-green.svg)
![Molecule](https://img.shields.io/badge/molecule-3.3.2-green.svg)

## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/rsyslog_role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](https://github.com/idealista/rsyslog_role/blob/master/CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/rsyslog_role/contributors) who participated in this project.

## License

![Apache 2.0 License](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE) file for details.

## Contributing

Please read [CONTRIBUTING.md](https://github.com/idealista/rsyslog_role/blob/master/.github/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.
