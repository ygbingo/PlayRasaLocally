# 0. Hello Rasa by Ubuntu for Windows

> My system is win10 without GPU, maybe better if you had GPU. However, I vaguely felt that there might be a lot of pits to build this environment for Windows. In order to avoid complicated problems, I didn't want to continue, so I used the Ubuntu subsystem of Win10 to play Rasa.

## 0-1. Prequirement
1. First you have to have a Win10 system computer (of course, this is more casual, Mac is better).
2. Installing the app: Ubuntu for Windows (if you are using a virtual machine).
3. Next go to Ubuntu (change the mirror source if you in the Greatwall 😋).
4. Setting up a Python environment (Python 3.6+, PIP)
``` shell
~$ python3 --version
# Python 3.8.5

~$ sudo apt install python3-pip
~$ pip3 --version
~$ pip3 install -U pip
# pip 21.0.1 from /home/bingo/.local/lib/python3.8/site-packages/pip (python 3.8)

~$ pip3 install rasa
```

## 0-2. Enjoy rasa first time
1. Open a new terminal.
2. Make a new dir in your home.
3. Initial a rasa project. (The comments in the code below are important.)
``` shell
~$ mkdir rasa
~$ cd rasa
~$ rasa init
# (A few minutes later...)
# input project name like 'hello_rasa'. If rasa ask you some question, ask yes is ok.
# ? Please enter a path where the project will be created [default: current directory] hello_rasa
# ? Path 'hello_rasa' does not exist 🧐. Create path?  Yes
# (A few minutes later...)
# ? Do you want to train an initial model? 💪🏽  Yes
# (A few minutes later...)
# Core model training completed.
# Your Rasa model is trained and saved at '/home/bingo/rasa/hello_rasa/models/20210402-125445.tar.gz'.
# ? Do you want to speak to the trained assistant on the command line? 🤖  Yes
```
4. OK! Let's play with Rasa first time.
``` shell
# 2021-04-02 12:56:19 INFO     rasa.model  - Loading model hello_rasa/models/20210402-125445.tar.gz...
# 2021-04-02 12:56:20 INFO     root  - Starting Rasa server on http://localhost:5005
# 2021-04-02 12:56:20 INFO     rasa.model  - Loading model hello_rasa/models/20210402-125445.tar.gz...
# 2021-04-02 12:56:30 INFO     root  - Rasa server is up and running.
# Bot loaded. Type a message and press enter (use '/stop' to exit):
```
![first_talk]("https://github.com/yanhuibin315/PlayRasaLocally/blob/main/imgs/first_talk.png")
5. And then you can open your project locally.<br>
Project Path (Maybe a little different in other system): ```C:\Users\User\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_79rhkp1fndgsc\LocalState\rootfs\home\bingo\rasa\hello_rasa\```<br>
You can show like this.

``` linux
.
├── actions
│   ├── __init__.py
│   └── actions.py
├── config.yml
├── credentials.yml
├── data
│   ├── nlu.yml
│   └── stories.yml
├── domain.yml
├── endpoints.yml
├── models
│   └── <timestamp>.tar.gz
└── tests
   └── test_stories.yml
```

6. Congratulations~ 🎊