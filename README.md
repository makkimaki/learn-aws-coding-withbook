# learn-aws-coding-withbook

# 環境準備
## Node.js
参照：https://nullnull.dev/blog/how-to-use-volta-in-mac/
```
curl https://get.volta.sh | bash
source ~/.zshrc
volta -v  # 1.1.0
volta install node  # 最新のLTSが入る。
volta list all
node -v  # v18.13.0（12.0以上であればok）
```

## AWS CLI インストール
参考：https://docs.aws.amazon.com/ja_jp/cli/latest/userguide/getting-started-install.html

### CLIのインストール
今回は、macOSを参照して実行  
```
cat /var/log/install.log
```
でインストール履歴が確認できる。また、以下のようにも確認。
```
(base) ???@???MacBook-Pro ~ % which aws
/usr/local/bin/aws
(base) ???@???MacBook-Pro ~ % aws --version
aws-cli/2.9.13 Python/3.9.11 Darwin/21.6.0 exe/x86_64 prompt/off
```
### CLI設定
- アクセスキー、シークレットアクセスキーをあらかじめ取得して控えておく
```
(base) ???@???MacBook-Pro ~ % aws configure
AWS Access Key ID [None]: [入力する]
AWS Secret Access Key [None]: [入力する]
Default region name [None]: ap-northeast-1
Default output format [None]: json
```
**確認**
```
(base) ???@???MacBook-Pro ~ % cat ~/.aws/credentials
[default]
aws_access_key_id = [入力したもの]
aws_secret_access_key = [入力したもの]
(base) ???@???MacBook-Pro ~ % cat ~/.aws/config
[default]
region = ap-northeast-1
output = json
```
