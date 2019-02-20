# PRBot

A bot for Slack that posts the name and link of a GitHub Pull Request that you have authored.

![PRBot Example Image](https://github.com/Daanikus/prbot/blob/master/prbot.png)

## Requirements
- [Go](https://golang.org/)\
- [Dep](https://github.com/golang/dep)\
- [Slack](https://slack.com/)

## Usage

- `dep ensure -v`
- `go install`
- `export GIT_TOKEN=<your GitHub access token>`
- `export SLACK_WEBHOOK=<your Slack webhook>`
- `prbot <your GitHub username> $GIT_TOKEN $SLACK_WEBHOOK`