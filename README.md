# AngularJS
AngularJS 打包apk小米，华为等手机不能正常运行出错
#报错：Mismachof CPU Architecture
#参照解决地址：https://stackoverflow.com/questions/49609647/cordova-cli-mismatch-of-cpu-architecture

1）安装https://github.com/MBuchalik/cordova-build-architecture插件添加到config.xml这样
<plugin name="cordova-build-architecture" spec="https://github.com/MBuchalik/cordova-build-architecture.git#v1.0.4" source="git" />

2）将此首选项添加到config.xml中的android部分：
<preference default="arm" name="buildArchitecture" />

3）
cordova clean

cordova build (This step only generates one apk, armv7)

cordova run --devices
