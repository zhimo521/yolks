# Yolks

A curated collection of core images that can be used with Pterodactyl's Egg system. Each image is rebuilt
periodically to ensure dependencies are always up-to-date.

Images are hosted on `ghcr.io` and exist under the `games`, `installers`, and `yolks` spaces. The following logic
is used when determining which space an image will live under:

* `oses` — base images containing core packages to get you started.
* `games` — anything within the `games` folder in the repository. These are images built for running a specific game
or type of game.
* `installers` — anything living within the `installers` directory. These images are used by install scripts for different
Eggs within Pterodactyl, not for actually running a game server. These images are only designed to reduce installation time
and network usage by pre-installing common installation dependencies such as `curl` and `wget`.
* `yolks` — these are more generic images that allow different types of games or scripts to run. They're generally just
a specific version of software and allow different Eggs within Pterodactyl to switch out the underlying implementation. An
example of this would be something like Java or Python which are used for running bots, Minecraft servers, etc.

All of these images are available for `linux/amd64` and `linux/arm64` versions, unless otherwise specified, to use
these images on an arm64 system, no modification to them or the tag is needed, they should just work.

## Contributing

When adding a new version to an existing image, such as `java v42`, you'd add it within a child folder of `java`, so
`java/42/Dockerfile` for example. Please also update the correct `.github/workflows` file to ensure that this new version
is tagged correctly.

## Available Images

* [`base oses`](https://github.com/pterodactyl-china/yolks/tree/master/oses)
  * [`alpine`](https://github.com/pterodactyl-china/yolks/tree/master/oses/alpine)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:alpine`
  * [`debian`](https://github.com/pterodactyl-china/yolks/tree/master/oses/debian)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:debian`
* [`games`](https://github.com/pterodactyl-china/yolks/tree/master/games)
  * [`rust`](https://github.com/pterodactyl-china/yolks/tree/master/games/rust)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/games:rust`
  * [`source`](https://github.com/pterodactyl-china/yolks/tree/master/games/source)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/games:source`
* [`golang`](https://github.com/pterodactyl-china/yolks/tree/master/go)
  * [`go1.14`](https://github.com/pterodactyl-china/yolks/tree/master/go/1.14)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:go_1.14`
  * [`go1.15`](https://github.com/pterodactyl-china/yolks/tree/master/go/1.15)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:go_1.15`
  * [`go1.16`](https://github.com/pterodactyl-china/yolks/tree/master/go/1.16)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:go_1.16`
  * [`go1.17`](https://github.com/pterodactyl-china/yolks/tree/master/go/1.17)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:go_1.17`
* [`java`](https://github.com/pterodactyl-china/yolks/tree/master/java)
  * [`java8`](https://github.com/pterodactyl-china/yolks/tree/master/java/8)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_8`
  * [`java8 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/8j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_8j9`
  * [`java11`](https://github.com/pterodactyl-china/yolks/tree/master/java/11)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_11`
  * [`java11 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/11j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_11j9`
  * [`java16`](https://github.com/pterodactyl-china/yolks/tree/master/java/16)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_16`
  * [`java16 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/16j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_16j9`
  * [`java17`](https://github.com/pterodactyl-china/yolks/tree/master/java/17)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_17`
  * [`java17 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/17j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_17j9`
  * [`java18`](https://github.com/pterodactyl-china/yolks/tree/master/java/18)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_18`
  * [`java18 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/18j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_18j9`
* [`nodejs`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs)
  * [`node12`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/12)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_12`
  * [`node14`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/14)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_14`
  * [`node15`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/15)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_15`
  * [`node16`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/16)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_16`
  * [`node17`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/17)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_17`
  * [`node18`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/18)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_18`
* [`python`](https://github.com/pterodactyl-china/yolks/tree/master/python)
  * [`python3.7`](https://github.com/pterodactyl-china/yolks/tree/master/python/3.7)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:python_3.7`
  * [`python3.8`](https://github.com/pterodactyl-china/yolks/tree/master/python/3.8)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:python_3.8`
  * [`python3.9`](https://github.com/pterodactyl-china/yolks/tree/master/python/3.9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:python_3.9`
  * [`python3.10`](https://github.com/pterodactyl-china/yolks/tree/master/python/3.10)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:python_3.10`

### Installation Images

* [`alpine-install`](https://github.com/pterodactyl-china/yolks/tree/master/installers/alpine)
  * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/installers:alpine`

* [`debian-install`](https://github.com/pterodactyl-china/yolks/tree/master/installers/debian)
  * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/installers:debian`
