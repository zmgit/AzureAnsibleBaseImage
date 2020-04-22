# Prepare OS
We assume you have already `python3-pip`, `virtualenv`, and `az-cli` installed on your OS.

# MacOS
```bash
brew install python3
pip3 install virtualenv
brew install azure-cli
```

# Prepare venv
```bash
ANSIBLE_VERSION=v2.9.7
pip3 install --upgrade virtualenv
virtualenv -p python3 venv
source venv/bin/activate
pip3 install --upgrade pip
pip3 install ansible==${ANSIBLE_VERSION}
pip3 install --no-cache --upgrade -r https://raw.githubusercontent.com/ansible/ansible/${ANSIBLE_VERSION}/packaging/requirements/requirements-azure.txt
```

# Login to the Azure
```bash
az login
```

# Run
```bash
ansible-playbook -i inventory/main.yml main.yml
```