# start up a vue project

##  PROXY
* NPM
``` bash
npm config set proxy http://user:passwd@host:port
npm config set https-proxy http://user:passwd@host:port
```

*  other tool proxy
``` bash
export http_proxy=http://user:passwd@host:port
export https_proxy=http://user:passwd@host:port
```

##  install vue cli
``` bash
npm install -g vue-cli
```

##  create a project
```bash
vue init webpack  <project-name>
```
*  example:
```bash
vue init webpack  kxvue
```

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## install other js library
``` bash
# install vue-axios
npm install --save axios vue-axios
```
