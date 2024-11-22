# 仓库简介
本仓库为GNU autoconf工具源码的镜像仓库，仅用于方便在如意玲珑沙箱下使用autoconf工具构建应用。

# 使用方法
1. 在linglong.yaml的[source]下加入如下内容:
``` yaml
  - kind: git
    url: https://github.com/rwenz2004/autoconf.git
```
2. 在linglong.yaml的[build]下加入如下内容:
``` bash
  cd /project/linglong/sources/autoconf.git
  mkdir -p ${PREFIX}/utils
  cd m4-install
  ./configure --prefix=${PREFIX}/utils
  make
  make install
  export PATH=${PREFIX}/utils/bin:$PATH
  cd ..
  ./configure --prefix=${PREFIX}/utils
  make
  make install
```
