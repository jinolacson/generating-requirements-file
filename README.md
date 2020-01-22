# Generating a requirements file

1. Install dependencies from `Pipfile`.

```
dev@jino:~/goal-tracking-app$ pipenv install
Creating a virtualenv for this project…
Pipfile: /home/dev/goal-tracking-app/Pipfile
Using /usr/bin/python3.6m (3.6.9) to create virtualenv…
⠼ Creating virtual environment...Already using interpreter /usr/bin/python3.6m
Using base prefix '/usr'
New python executable in /home/dev/.local/share/virtualenvs/goal-tracking-app-HFp0ArRb/bin/python3.6m
Also creating executable in /home/dev/.local/share/virtualenvs/goal-tracking-app-HFp0ArRb/bin/python
Installing setuptools, pip, wheel...
done.
Running virtualenv with interpreter /usr/bin/python3.6m
✔ Successfully created virtual environment! 
Virtualenv location: /home/dev/.local/share/virtualenvs/goal-tracking-app-HFp0ArRb
Installing dependencies from Pipfile.lock (fa77be)…
  🐍   ▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉▉ 12/12 — 00:00:15
To activate this project's virtualenv, run pipenv shell.
Alternatively, run a command inside the virtualenv with pipenv run.
```

2. Activate shell.

```
dev@jino:~/goal-tracking-app$ pipenv shell
Launching subshell in virtual environment…
 . /home/dev/.local/share/virtualenvs/goal-tracking-app-HFp0ArRb/bin/activate
dev@jino:~/goal-tracking-app$  . /home/dev/.local/share/virtualenvs/goal-tracking-app-HFp0ArRb/bin/activate
```

3. Now we need to generate the file using [Pip freeze](https://pip.pypa.io/en/stable/reference/pip_freeze/#pip-freeze). 

```
(goal-tracking-app) dev@jino:~/goal-tracking-app$ pip freeze > requirements.txt
```

4. Check if `requirements.txt` already generated.

```
(goal-tracking-app) dev@jino:~/goal-tracking-app$ ls
backend  Pipfile  Pipfile.lock  requirements.txt
```

5. Display dependencies.


```
(goal-tracking-app) dev@jino:~/goal-tracking-app$ cat requirements.txt
asgiref==3.2.3
cffi==1.13.2
cryptography==2.8
Django==3.0.2
django-cors-headers==3.2.1
django-rest-knox==4.1.0
django-restframework==0.0.1
djangorestframework==3.11.0
pycparser==2.19
pytz==2019.3
six==1.13.0
sqlparse==0.3.0
(goal-tracking-app) dev@jino:~/goal-tracking-app$ 
```

6. Done!, you are able to install this dependencies by running `pip install -r requirements.txt` (Python 2), or `pip3 install -r requirements.txt` (Python 3) 


###  Resources

- [Pip freeze](https://pip.pypa.io/en/stable/reference/pip_freeze/#pip-freeze)

- [Requirements files Documentation](https://pip.pypa.io/en/stable/user_guide/#requirements-files)
