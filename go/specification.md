# Go 代码规范

> 前言
    
       Go语言比较常见并且使用广泛的代码规范就是官方提供的 Go Code Review Comments，无论你是短期还是长期使用Go语言编程，都应该至少完整地阅读一遍这个官方的代码规范指南，它既是我们在写代码时应该遵守的规则，也是在代码审查时需要注意的规范。

---
> 规范

- [Uber开源的编码规范](https://github.com/Hex-Techs/specifications/tree/main/go/uber.md)

---
> IDE配置
- 在配置IDE之前，设置GOPROXY全局环境变量，因为很多Go项目和工具是需要翻墙的，如果自己有翻墙工具可以省略此步骤。
```bash
$ echo 'export GOPROXY="https://goproxy.cn"' >> /etc/profile
$ echo 'export GOPROXY="https://goproxy.cn"' >> /etc/zshrc
$ reboot
```
- VsCode
  - 在插件中心直接下载Go插件
  - 在设置 -> Extensions -> Go -> Format Tool 中选择 goreturns，这是go官方默认的格式化插件
  - 打开go项目代码， vscode会自动提示安装go工具包，点击安装即可
  - go工具包中包括了go fmt和goimports等格式化工具

- Goland
  - 在初始界面选择，不要打开项目，这样的设置是全局的设置，适用所有go项目
  - Preferences -> Tools -> File Watchers
  - 点击左下角的‘+’号，选择添加 go fmt 和 goimports，点击Apply，保存即可。
  - 这样会在代码保存的时候自动格式化代码