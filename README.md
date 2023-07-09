[![Build and Push to Docker Hub](https://github.com/onezero1010101/seafile-client/actions/workflows/Build%20and%20Push%20to%20Docker%20Hub%20Weekly.yml/badge.svg)](https://github.com/onezero1010101/seafile-client/actions/workflows/Build%20and%20Push%20to%20Docker%20Hub%20Weekly.yml)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/onezero1010101/seafile-client/Build%20and%20Push%20to%20Docker%20Hub%20Weekly.yml?label=Build%20and%20Push%20to%20Docker%20Hub)
![GitHub issues](https://img.shields.io/github/issues-raw/onezero1010101/seafile-client)
![Docker Stars](https://img.shields.io/docker/stars/onezero1010101/seafile-client)

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/nopenix/seafile-client/Build%20and%20Push%20to%20Docker%20Hub.yml?label=Build%20and%20Push%20to%20Docker%20Hub)
![GitHub issues](https://img.shields.io/github/issues-raw/nopenix/seafile-client)
![Docker Stars](https://img.shields.io/docker/stars/nopenix/seafile-client)
![GitHub Repo stars](https://img.shields.io/github/stars/nopenix/seafile-client?label=GitHub%20Stars)
![GitHub top language](https://img.shields.io/github/languages/top/nopenix/seafile-client)
# seafile-client
Seafile Client Docker Image

## Where to find my Files?
You can find all files from the Library in ```/app/lib/```

## Security
The Container gets automatically build every week with the freshed updates available. 

## Example docker-compose:
```yml
version: "3"
services:
    app:
        image: nopenix/seafile-client
        volumes:
            - SeafileData:/app/seafiles/
            - LibraryData:/app/lib
        environment:
            - SERVER=ServerURI # e.g. https://share.example.com
            - LIB_ID=000aaaaa-a0aa-0a00-0aa0-000a0000a000 # Library ID
            - SEAFILE_USERNAME= # E-Mail address of the user
            - SEAFILE_PASSWORD=

volumes:
    SeafileData:
    LibraryData:

```
