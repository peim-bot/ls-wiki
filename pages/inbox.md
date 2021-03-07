---
title: Inbox
---

## [[CSS]]
### LATER 文本中间省略号
:PROPERTIES:
:later: 1615123399645
:END:
## [[Go]]
### 使用 go mod
先在项目根目录`go mod init projectName`，生成 go.mod 文件，之后 `go get module`会自动更新到 go.mod
## [[Mac]]
### vscode 中允许重复按键 #Vim
```shell
$ defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false         # For VS Code
$ defaults write com.microsoft.VSCodeInsiders ApplePressAndHoldEnabled -bool false # For VS Code Insider
$ defaults write com.visualstudio.code.oss ApplePressAndHoldEnabled -bool false    # For VS Codium
$ defaults delete -g ApplePressAndHoldEnabled                                      # If necessary, reset global default
```
## [[cURL]]
### 文件上传
```
curl -F 'file=@photo.png' https://google.com/profile
