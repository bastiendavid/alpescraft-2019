## Prerequisites

### Clone the submodule 

There's a submodule and in order to use the deploy.sh script to 
publish a new version you need it.

    cd public
    git submodule update --init --recursive

### Docker

This project can be run using Docker with the following command :
```
docker run --rm -it -v ${PWD}:/src -p 1313:1313 klakegg/hugo:0.61.0-ext-alpine server
``` 

### Hugo Extended

If not using Docker, you can run this project using Hugo Extended : https://gohugo.io/

For windows install : https://chocolatey.org/packages/hugo-extended

#### Run dev mode

```
hugo server -D
```

ou avec Docker, sans installer Hugo :

```
./startDockerHugo.sh
```

#### Prod mode

```
hugo
```

## Deploy
Don't forget to clone the submodule beforehand, see top of Readme 

```
hugo
./deploy.sh
```
