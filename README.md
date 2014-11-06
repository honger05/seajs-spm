seajs-spm
=========

###使用spm构建seajs项目###


spm3 已经发布，建议使用最新的构建工具。http://spmjs.io/documentation/develop-a-package#build

```
如果项目遵循推荐的标准目录结构：
foo-module/
  |-- dist                    存放构建好的文件
  |-- src                     存放 js、css 等源码
  |     |-- foo.js
  |     `-- style.css
  `-- package.json      模块信息
```

那么构建很简单。首先安装 spm 工具（spm2）：
$ npm install spm@2.x -g
$ npm install spm-build -g

然后运行构建命令：
$ cd foo-module
$ spm build

这样，就会根据 package.json 中的信息，将文件自动构建到 dist 目录下。构建后，还需要将 dist 目录下的文件部署到 sea-modules 目录中，比如 examples 中的 make deploy 命令：Makefile




example中的构建

First, you should install spm and spm-build:

$ npm install spm@2.x -g
$ npm install spm-build -g

Then, build it:
$ cd static/hello
$ make build
$ make deploy
