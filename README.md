# LXFUpdatePodTool
fastlane 自动化更新私有库工具

- 一个帮助我们自动化更新私有库的工具
- 与[iOS 组件化开发（四）：fastlane实现pod自动化](https://juejin.im/post/5ac6eb6351882555731c5e9e)配合使用，味道更佳～

## 使用

1. 将fastlane拷贝到你的本地仓库的根目录
2. 打开Fastfile，找到pod_push并进行修改

```
# repo：将 LXFSpecs 修改为你自己的本地私有索引库的名称
pod_push(path: "#{podspecName}.podspec", repo: "LXFSpecs")

```
3. 打开终端，cd到你的组件仓库的根目录下

```
# fastlane LXFUpdatePodTool tag:版本号 specName:podspec文件名字

# 如：
fastlane LXFUpdatePodTool tag:0.1.1 specName:LXFMain
```
