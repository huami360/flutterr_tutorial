# flutter配环境少踩坑指南

## macOS

### flutter换源

终端执行
```
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```
替换flutter/package/flutter_toools/lib/src/http_host_validator.dart
```
const String kCloudHost = 'https://storage.googleapis.com/';
const String kCocoaPods = ' https://maven.aliyun.com/repository/google/';
const String kGitHub = 'https://github.com/';
const String kMaven = ' https://maven.aliyun.com/repository/google/';
const String kPubDev = 'https://mirrors.tuna.tsinghua.edu.cn/dart-pub;
```

### homebrew安装
```
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"
```

### git安装
```
brew install git
```

### cocoapods安装
```
brew install cocoapods
```

### cocoapods添加清华源
```
pod repo add tuna https://mirrors.tuna.tsinghua.edu.cn/git/CocoaPods/Specs.git
```

### podfile第一行加上
```
source 'https://mirrors.tuna.tsinghua.edu.cn/git/CocoaPods/Specs.git'
```

### 初次安装Xcode
```
sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer
```

### 直到自检合格
```
flutter doctor -V
```

### 运行流程
```
flutter pub get
cd ios
pod install
```
