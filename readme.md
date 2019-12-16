# Introduction
The main discovery here is the way to install the PySide2 and other PyQt modules. It took a feat of Googling to discover this well hidden in the [Qt Bug Reports](https://bugreports.qt.io/browse/PYSIDE-802) site. Note that installing them with apt seems to be incompatible with the Python venv. I do not know why.

# Establish a python venv locally
```python3 -m venv venv
source venv/bin/activate
````

# Pull Balena base image
Refer to the [Balena documentation](https://www.balena.io/blog/running-a-gui-application-with-balenacloud/)


```git clone git@github.com:balena-io-playground/balena-vnc-example.git
mv balena-vnc-example/* .
rm -Rf balena-vnc-example
```



# Create the Requirements files
This just makes the install a little nicer
## A Pip Requirements.txt
./vnc-app/Requirements.txt

## An apt Requirement.apt
./vnc-app/Requirements.apt


# Edit Dockerfile.template

See the file as it is. Kind of self explanatory, but the venv stuff is commented out.

## Add Python venv to Dockerfile
See documentation on [Python venv in Docker](https://pythonspeed.com/articles/activate-virtualenv-dockerfile/) here.

# Push to Balena
```balena login
balena push MyApp
```



help("modules qt")

## Things I tried in app.conf
/opt/venv/bin/
environment=PATH="/opt/venv/bin:$PATH"
