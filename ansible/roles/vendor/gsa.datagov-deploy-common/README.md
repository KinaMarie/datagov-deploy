[![CircleCI](https://circleci.com/gh/GSA/datagov-deploy-common.svg?style=svg)](https://circleci.com/gh/GSA/datagov-deploy-common)

# datagov-deploy-common

Common configuration and baseline for all Data.gov platform nodes.


## Usage

Install the role with a requirements.yml.

```yaml
# requirements.yml
---
- src: https://github.com/GSA/datagov-deploy-common
  version: v1.0.0
  name: gsa.datagov-deploy-common
```

And install with ansible-galaxy.

    $ ansible-galaxy install -r requirements.yml

An example playbook.


```yaml
---
- name: install application
  roles:
    - role: gsa.datagov-deploy-common
```


### Variables

**`common_python_version_number`** string (default: 2.7.10)

Custom version of python to install.


**`common_python_version_directory`** string (default: `/usr/local/lib/python{{ common_python_version_number }}`)

Directory to install custom python to.


**`common_python_version_url`** string (default: `https://www.python.org/ftp/python/{{ common_python_version_number}}/{{ common_python_version_name }}.tgz`)

URL to download python from.


**`common_python_version_name`** string (default: `Python-{{ common_python_version_number }}`)

Python filename.


## Contributing

See [CONTRIBUTING](CONTRIBUTING.md) for additional information.


## Development

Install dependencies.

    $ pipenv install --dev

Run the playbook with molecule.

    $ pipenv run molecule converge

Run the tests.

    $ pipenv run molecule test

For more information on how to use
[Molecule](https://molecule.readthedocs.io/en/latest/) for development, see [our
wiki](https://github.com/GSA/datagov-deploy/wiki/Developing-Ansible-roles-with-Molecule).


## Public domain

This project is in the worldwide [public domain](LICENSE.md). As stated in
[CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright
> and related rights in the work worldwide are waived through the [CC0 1.0
> Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication.
> By submitting a pull request, you are agreeing to comply with this waiver of
> copyright interest.