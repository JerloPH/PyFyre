# PyNani
PyNani is a Python web user interface framework for building reactive static websites. Pynani is free and open source project.

Note: Master Branch is not stable, if you want to use PyNani please use Stable branch, thank you!

## Stay Updated
If you would like to get updates about the PyNani framework, we created a [Facebook Page](https://www.facebook.com/pynaniframework) where we are going to post all the updates like newly created widgets, adjustments, core updates, and more. Please consider liking it also. Thank you so much!

## Documentation
Documentation for PyNani is still in development.

## Examples
We have examples in ```/examples``` folder. But here is the super simple example:

```py
# Import PyNani
from pynani.core.pynani import Component, RunApp
from pynani.core.widgets import Widgets

widgets = Widgets()


# Create class called MyApp extends Component from PyNani Core
class MyApp(Component):

    # Where all rendering stuff began in a component...
    def build(self):

        # Returing widgets.container A.K.A <div> in HTML
        # widgets.container(child[Widget], onClick[Javascript], styles[List of CSS Styles])
        return widgets.container(

            # With a child widgets.header1 A.K.A <h1> in HTML
            # widgets.header1(text[String], onClick[Javascript], styles[List of CSS styles])
            child=widgets.header1(
                text="Hello, Jabez!",
                styles=[
                    "margin-top: 10px"
                ]
            )
        )

## To render the widgets into the screen, you need to call RunApp() to compile your code into raw HTML
RunApp(MyApp())
```
Rendered PyNani:
![image](https://user-images.githubusercontent.com/64759159/111236942-fc090800-862e-11eb-9889-4c079e65823c.png)


## Installation
Install Python3 on your local machine/PC.

Create a folder called 'PyNani' on your C:\ folder.
```
C:\pynani\
```
Get the source code from PyNani repo on GitHub.
```
C:\pynani> git clone https://github.com/jabezborja/pynani.git -b stable
```
### Update your path
If you wish to run PyNani commands in the regular Windows console, take these steps to add PyNani to the PATH environment variable:

* From the Start search bar, enter ‘env’ and select Edit environment variables for your account and click Environment Variables in the bottom right.
* Under User variables check if there is an entry called Path:
-   If there is path, double click into it, and click ```new``` then type ```C:\pynani\PyNani\bin```.
-   If there is none, click ```new``` and type ```Path``` as the Variable name and ```C:\pynani\PyNani\bin``` as value.

And now, you have the PyNani on your local machine!

### Create an App
To create a Web App, go to the folder where you want PyNani to install in then go to CMD or command line and type:
```
pynani.py create-app <App_Name>
```

in real world example, it should be:
```
pynani.py create-app my_cool_app
```

Then it will create a boilerplate code for you.

Now, locate to your created folder called the app name you entered. Then type in the Command Line or CMD:
```
py -m venv env
```
This command creates a environment for your app. 

It should take few seconds or minutes. Once it's done, go to the ```C:\pynani\``` and clone the PyNani folder to ```env\lib\site-packages```.

And type:
```
env\scripts\activate
```
To activate your virtual environment.

For Hot Reload, you need to install a package called ```Watchdog``` for file changes watcher. To install that type 
```
pip install watchdog
```
It will install and wait for few seconds.

Now, locate to the main workspace navigate to ```src``` folder and type:
```
pynani.py runserver
```
It will run the watchdog and now the HOT RELOAD is now HOT!!!

To make your website live on your local machine, you can use XAMPP or Live Server in VSCode

#### Live Server
Install VSCode or Visual Studio Code on your PC.

Once you have the VS Code go to extensions, you can see it on your left then click the 4 blocks logo. Then type: ```Live Server```

and it will install.

Now, open your PyNani App folder on VSCode by typing on CMD located on your PyNani Folder:
```
C:\users\<your_username>\desktop\pynani>code .
```
it will load for few seconds and click ```Go Live``` on bottom right.

#### XAMPP
See https://www.apachefriends.org/index.html

## Contributing
Please read [CONTRIBUTING.md](CONTRIBUTING.md) for this.
