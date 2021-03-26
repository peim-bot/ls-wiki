---
title: Inbox
---

## [[Vim]]
### css module styles marco
`0f"da"i{styles[pa]}`
## [[CSS]]
### LATER 文本中间省略号
:PROPERTIES:
:later: 1615123399645
:END:
## [[Go]]
### 使用 go mod
先在项目根目录`go mod init projectName`，生成 go.mod 文件，之后 `go get module`会自动更新到 go.mod
### 使用`.env`文件配置环境变量 `go get github.com/joho/godotenv`
```go
func init() {
	err := godotenv.Load()
	if err != nil {
		log.Fatal("Error loading .env file")
	}
}
```
### 时间格式化`2006-01-02 15:04:05`
```go
time.Now().Format("2006/01/02/20060102150405")
```
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
```shell
curl -F 'file=@photo.png' https://google.com/profile
```
## [[GitHub]]
### [[GitHub Action]] 部署到服务器：[easingthemes/ssh-deploy: GitHub Action for deploying code via rsync over ssh](https://github.com/easingthemes/ssh-deploy
## [[FFmpeg]]
### 添加和去除黑边
```shell
ffmpeg -i 2160.mp4 -vf crop=1920:1080:120:0 1920.mp4 # 去除黑边
ffmpeg -i 1920.mp4 -vf pad=2160:1080:120:0:black  2160-2.mp4 #添加黑边
```
## [[JavaScript]]
### `URL.host` vs `URL.hostname`
前者包办端口号，后者不包含
###
## [[React]]
### `useEffect` 和异步函数
https://juliangaramendy.dev/blog/use-promise-subscription
