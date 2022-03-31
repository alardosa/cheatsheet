# Setup and Document: Backend REST API with Python & Django

This is the supplementary cheat sheet document for our course: [Build a Backend REST API with Python & Django](https://www.linkedin.com/in/alardosa/)

<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Python](#python)
- [Atom](#atom)
- [Git](#git)
- [SSH Key Management](#ssh-key-management)
- [Docker](#docker)
- [Django Management Commands](#django-management-commands)
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
```
**Add Atom Packages**
```atom-django
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

**Git clone if theres existing repo in Github**
```
git clone git@github.com:<username>/<repository>.git
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

## Docker
**Install Docker**
```
Full intstructions:
https://docs.docker.com/engine/install/ubuntu/

IN TERMINAL:
sudo apt-get update

sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io

apt-cache madison docker-ce

EXAMPLE:
sudo apt-get install docker-ce=<VERSION_STRING> docker-ce-cli=<VERSION_STRING> containerd.io
sudo apt-get install docker-ce=5:20.10.14~3-0~ubuntu-impish docker-ce-cli=5:20.10.14~3-0~ubuntu-impish containerd.io

sudo docker run hello-world

Create 'Dockerfile' in your 'project directory'
or copy https://github.com/alardosa/cheatlist/blob/master/Dockerfile

List of available images for python: https://hub.docker.com/_/python

```
**Add Dockerfile and Install Python Packages**
```
Packges: https://pypi.org/

Under your 'project directory' create 'app' directory

Under your 'project directory' create 'requirements.txt'
or copy: https://github.com/alardosa/cheatlist/blob/master/requirements.txt

GET LATEST PACKES OF:
Django
djangorestframework
psycopg2
Pillow
flake8

IN TERMINAL
sudo docker build .
```
**Configure Docker Compose**
```
Full intstructions:
https://docs.docker.com/compose/install/

Under your 'project directory' create 'docker-compose.yml'
or copy https://github.com/alardosa/cheatlist/blob/master/docker-compose.yml

IN TERMINAL
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose

sudo docker-compose build
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
