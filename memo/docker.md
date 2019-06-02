# Docker準備

## docker desktop for Mac インストール



## Djangoプロジェクト作成

「~/PycharmProject/mysite」にDjangoプロジェクトが作成されているものとする

## DockerfileからDockerイメージを作成

DockerfileをDjangoプロジェクトの直下に作成する。

次のコマンドを実行し、DockerfileからDockerイメージを作成する。

```sh
docker build -t mysite:1.0 ~/PycharmProjects/mysite/
```



## Dockerコンテナを実行

```sh
docker run -it -p <ホスト側のポート番号>:<コンテナ側のポート番号> -v <ホストOS側のディレクトリ>:<マウント先のコンテナ側のディレクトリ> --name <コンテナ名> <イメージ名>:<タグ名> <起動時のコマンド>
```

```sh
docker run -it -p 8000:8000 -v ~/PycharmProjects/mysite:/root/mysite/ --name mysite mysite:1.0 /bin/bash
```

```sh
docker run -it -p 8000:8000 -v ~/Dropbox/workspace/py_study/django_study/django_textbook/mysite/:/root/mysite/ --name mysite mysite:1.0 /bin/bash
```



## Docker上で事前準備

必要なものを適宜インストール

```sh
apt-get install -y sqlite3
```

requiremtns.txtでまとめてインストール

```sh
pip3 install -r requirements.txt
```

あるいはpipでひとつずつインストール

```
pip3 install "Django==2.2"
```



## 動作確認

runserverを実行して、macOS上のブラウザで動作確認

```
python3 manage.py runserver 0.0.0.0:8000
```

