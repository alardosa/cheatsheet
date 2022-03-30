# Setup and Document: Backend REST API with Python & Django

This is the supplementary cheat sheet document for our course: [Build a Backend REST API with Python & Django](https://www.linkedin.com/in/alardosa/)

<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Python](#python)
- [Atom](#atom)
- [Git](#git)
- [SSH Key Management](#ssh-key-management)
- [Virtual Environments](#virtual-environments)
- [Django Management Commands](#django-management-commands)
- [Vagrant](#vagrant)
- [Terminal / GitBash Commands](#terminal-gitbash-commands)
- [ModHeader](#modheader)

<!-- /TOC -->

## Python
```
sudo apt install python3 python3-pip build-essential python3-dev

python3 -V
```

## Atom
```
Download and Install: https://atom.io/download/deb

Type in terminal:
python3 -m pip install python-language-server[all]
python3 -m pip install git+https://github.com/tomv564/pyls-mypy.git

Add Packages:
atom-django
autocomplete-python-jedi

auto-complete-python
Python Executable Paths: /usr/bin/python3
Extra Paths For Packages: /usr/bin/python3/site-packages

ide-python
atom-ide-base
atom-ide-debugger
atom-ide-console
platformio-ide-terminal
script
tom-django
```

## Git
```
Download and Install: https://git-scm.com/download/linux
```

Use the below Git commands in the Windows Command Prompt or macOS Terminal.

**Configure default email and name**

*Note: This only needs to be done the first time you use Git on your machine*

```
git config --global user.email "your@email.com"
git config --global user.name "Your Name"
```


**Use git under your project directory**
```
example Go to 'profiles-rest-api' directory 'Git Bash Here'
```

**Initialise a new Git repository**
```
git init
```

**Commit changes to Git**
```
git add .
git commit -am "Commit message"
```

**SSH Key Management**

The below commands are used to manage SSH keys on your local development machine.

**Checking for existing SSH key**

```
ls ~/.ssh/ or ls -al ~/.ssh
```

**Print contents of public key**

```
cat ~/.ssh/id_rsa.pub
```

**Generate new SSH key on your local machine**

```
ssh-keygen -t rsa -b 4096 -C "EMAIL ADDRESS"
```

**Login and Setup SSH to your GitHub:**
```
Setup Your Key: https://github.com/settings/ssh/new
Create a new repository: https://github.com/new
```

**Set Git remote**

*Note: This only needs to be done once, the details are provided by GitHub after creating a new project*

```
git remote add origin git@github.com:username/repository.git
```

**Push changes to GitHub**

```
git push -u origin master
yes

or

git push origin
```


## Virtual Environments

The below commands are used for managing Virtual Environments using Python3-env. Use these commands when connected to your Vagrant server.

**Create new environment**

```
python -m venv ~/env
```

**Activate virtual environment**

```
source ~/env/bin/activate
```

**De-activate virtual environment**

```
deactivate
```

**Install requirements from requirements.txt**

*Note: Virtual environment must be activated*

```
pip install -r requirements.txt
```

## Django Management Commands

**Create new Django project**

```
django-admin.py startproject profiles_project  .
```

**Create new Django app**

```
python manage.py startapp profiles_api
```

**Start Django development server**

```
python manage.py runserver 0.0.0.0:8000
```

**Create database migrations file**

```
python manage.py makemigrations
```

**Run migrations**

```
python manage.py migrate
```

**Create new superuser**

```
python manage.py createsuperuser
```

## Vagrant

These commands are used for managing Vagrant using the GitBash or Terminal windows.

**Initialise Vagrant on project**

```
vagrant init ubuntu/bionic64
```

**Start Vagrant box**

```
vagrant up
```

**Connect to Vagrant box**

```
vagrant ssh
```

**Disconnect from Vagrant box**

*Note: This command is a standard linux command for ending an SSH session*

```
exit
```

**Stop Vagrant box**

```
vagrant halt
```

**Remove Vagrant box**

```
vagrant destroy
```

**Update Vagrant box image**

*Note: you must rebuild the image after updating*

```
vagrant box update
```

## Terminal / GitBash Commands

Change directory

```
cd /directory_name
```

Change to parent directory

```
cd ..
```

## ModHeader
```
Download and Install: https://chrome.google.com/webstore/detail/modheader/idgpnmonknjnojddfkpgkljpfnnfcklj?hl=en
```
