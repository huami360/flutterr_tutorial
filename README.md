# flutter配环境少踩坑指南

## macOS

### homebrew安装
```
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"
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
