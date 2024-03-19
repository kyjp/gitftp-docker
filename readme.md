[git-ftp]
	url = ftp://localhost:21
[git-ftp "stg"]
	user = uname
	password = uP@ssw0rd
	syncroot = /home/ubuntu

## git ftp設定
git config git-ftp.stg.url "ftp://ステージングのFTPホスト/指定ディレクリ"
git config git-ftp.stg.user "ステージングのFTPユーザー"
git config git-ftp.stg.password "パスワード"
git config git-ftp.stg.syncroot pushしたいディレクトリ

## 確認
cat .git/config

# コマンド
## 初期１回目
git ftp init -v

## 2回目以降
git ftp push

## ユーザーとパスワードをつけて実行
git ftp push -u uname -p uP@ssw0rd

## 使い方
docker-compose up -d


## ftpサーバ 接続
docker-compose exec -it ftp_server /bin/bash
/home/ubuntuにあがる
