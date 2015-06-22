# docker-centos-nodejs-gm-base
Base Docker image running nodejs on centos with GraphicsMagick installed

## Installed
 
 * CentOS (6.6)
 * NodeJS (v0.10.36)
 * NPM (1.3.6)
 * GraphicsMagick (1.3.21)

## Usage

Put the following into your own Dockerfile within the root of your node app. The example assumes a boilerplate install of ExpressJS, so change accordingly:

```
FROM colyn/centos-nodejs-gm-base

COPY . /src

RUN cd /src; npm install

EXPOSE  3000

CMD ["node", "/src/bin/www"]
```
