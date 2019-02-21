# PRBot

A bot for Slack that posts the name and link of a GitHub Pull Request that you have authored.

![PRBot Example Image](https://github.com/Daanikus/prbot/blob/master/prbot.png)

## Requirements
- [Go](https://golang.org/)
- [Dep](https://github.com/golang/dep)
- [Slack](https://slack.com/)

## Usage

- `dep ensure -v`
- `go install`
- `export GIT_TOKEN=<your GitHub access token>`
- `export SLACK_WEBHOOK=<your Slack webhook>`
- `prbot <your GitHub username> $GIT_TOKEN $SLACK_WEBHOOK`

## Run in Docker
- `CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o main .`
- `docker build -t prbot -f Dockerfile.scratch`
- `docker run -it prbot -e TOKEN=$GIT_TOKEN -e HOOK=$SLACK_WEBHOOK`
