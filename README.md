# Quora-Insincere-Questions-Classification
## Getting started
### Setup kaggle api credential
Download kaggle.json and place in the location: ~/.kaggle/kaggle.json.
See details: https://github.com/Kaggle/kaggle-api


```
#!/bin/bash
 
set -e
 
yum -y install fuse
su ec2-user -c "/home/ec2-user/SageMaker/go/bin/goofys quora-insincere-questions-classification ~/SageMaker/goofys-mount/"
```

```
#!/bin/bash

set -e
# goofysの依存パッケージをインストール
sudo yum -y install golang fuse
# GOPATHの設定(SageMakerフォルダ配下にしてください､理由は後述)
su ec2-user -c export GOPATH=~/SageMaker/go
# PATHの設定
su ec2-user -c export PATH=$GOPATH/bin/:$PATH"
# goofysをインストール
go get github.com/kahing/goofys
go install github.com/kahing/goofys
# S3をマウント
su ec2-user -c /home/ec2-user/SageMaker/go/bin/goofys quora-insincere-questions-classification ~/SageMaker/goofys-mount/
```
