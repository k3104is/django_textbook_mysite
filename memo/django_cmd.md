# 覚えておきたいDjango管理コマンド

## 1. startproject(新しいプロジェクトのひな形を作成)

```sh
django-admin startproject <プロジェクト名> [<ディレクトリ>]
```

第二引数を省略した場合は現在のディレクトリの直下にベースディレクトリが作成される。  
「.」を指定した場合はベースディレクトリが作成される。

## 2. startapp(プロジェクトにアプリケーションのひな形を追加)

```sh
python3 manage.py startapp <アプリケーション名>
```

## 3. makemigrations(マイグレーションファイルを生成)

モデルの変更差分から、マイグレーションファイルを自動生成する。

```sh
python3 manage.py makemigrations[<アプリケーション名>]
```

## 4. migrae(マイグレーションファイルからテーブルを作成・変更)

```sh
python3 manage.py migrate [<アプリケーション名>]
```

## 5. createsuperuser(システム管理者を作成)

superuser(システム管理者)のレコードを作成

```sh
python3 manage.py createsuperuser
```

## 6. loaddata(ファイルに書かれたレコードをデータベースにインポート)

テスト実施前にまとまったデータを準備するいつ用があるときなどで重宝

```sh
python3 manage.py loaddata <ファイルパス>
```

## 7. runserver(開発用のwebサーバを起動)

```sh
python3 manage.py runserber[<IPアドレス>:<ポート番号>]
```

## 8. Shell(Djangoのプロジェクト設定を読み込んだREPLを起動)

Djangoの設定ファイルが読み込まれてセットアップが完了したREPL

```sh
python3 manage.py shell
```

## 9. collectstatic(静的ファイルを公開用ディレクトリに収集)

```sh
python3 manage.py collectstatic
```

## 10. test(ユニットソフトを実行)

「test」で始まるモジュール内の、TestCaseクラスを継承したクラスの名前が「test」で始まるメソッドをテスト実行対象として自動で収集して実行

```
python3 manage.py test
```

