Establish a python venv locally
python3 -m venv venv
source venv/bin/activate

# Pull Balena base image
Refer to the [Balena documentation](https://www.balena.io/blog/running-a-gui-application-with-balenacloud/)
```git clone git@github.com:balena-io-playground/balena-vnc-example.git
mv balena-vnc-example/* .
rm -Rf balena-vnc-example
```



# Create the Requirements files

## A Pip Requirements.txt
./vnc-app/Requirements.txt

## An apt Requirement.apt




# Edit Dockerfile.template

## Add Python venv to Dockerfile
See documentation on [Python venv in Docker](https://pythonspeed.com/articles/activate-virtualenv-dockerfile/) here.

Log in to Balena
```balena login
balena push Elgato1
```





/opt/venv/bin/
environment=PATH="/opt/venv/bin:$PATH"
