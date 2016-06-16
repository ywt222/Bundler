# Bundler
- Bundler是管理gem依赖的工具。
- Gemfile和Gemfile.lock是Bundler依赖的配置文件。

### Bundler:
- 可以通过安装所需的指定gem及其版本来保证ruby项目的环境一致。  

### Gemfile:
- 将gem依赖写在Gemfile中。
- Gemfile会从source中寻找所声明的gem，通过`bundle install`来获取这些依赖。

### Gemfile.lock:
- 系统安装完所有需要的gem后，bundle会将所安装的gem及其version写入到Gemfile.lock中。
- 当其他人或其他机器运行代码时，可以从Gemfile.lock中获取到代码所依赖的准确的gem版本。
- 当运行bundle install时，bundle会安装你原有机器上相同的gem。

### bundle init:
- 生成Gemfile，默认的rubygems.org source。

### bundle install:
- 安装所需的gem，在执行bundle install时， 会根据Gemfile的设定，检查指定的gem依赖是否已安装，若安装则显示using，否则显示installing。
- 即使开发环境改变，Bundler也会帮你管理好你的应用程序所依赖的Gem。而Gemfile.lock文件里则记录了一系列依赖规则。

### bundle update:
- 更新某个特定的gem，例如 `bundle update sinatra`，可以更新sinatra gem及其依赖的其他gem。
- 更新Gemfile中的所有gem，`bundle update`。
