# ansible-osx-env
An Ansible playbook for provisioning a local OS X system. Heavily based on ansible-osx-env by github.com/richardrowe modified for my own use.

# Prerequisites

1. Install Xcode
  ```bash
  $ xcode-select --install
  ```
  (select the **Get Xcode** option and install the full suite)

2. Agree to the xcode license
  ```bash
  $ sudo xcrun cc
  ```

3. Install Homebrew
  ```bash
  $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  $ brew doctor
  ```

4. Install Python / Pipenv
  ```bash
  $ brew install python
  $ pip install pipenv
  ```

4. Clone this repository and install Ansible
  ```bash
  $ git clone https://github.com/stoggi/ansible-osx-env.git
  $ cd ansible-osx-env
  $ pipenv install
  ```

5. Run ansible
  ```bash
  $ pipenv run ansible-playbook --ask-sudo-pass -i ./inventory local.yml --connection=local
  ```
