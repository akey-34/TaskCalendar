﻿# シフト管理をするカレンダーシステム
カレンダーの予定管理機能にバイトのシフト管理機能を入れたプログラムはどのように書かれているのかと思い、グループワークの一環で作成した。

# 機能
ログイン機能、ユーザ登録機能、カレンダーや日付ごとの予定を出力するホーム画面、予定登録機能、予定更新機能、予定削除機能、予定のメモを残すメモ機能、バイトの情報を登録し、テンプレートを作成する機能、テンプレートを用いて、バイトの予定を登録する機能が含まれている。

# 必要要件
requirements.txtに記載されている物が必要。
また別途でMySQLを用いてデータベースを作成する必要がある。

# データベースの構成

アカウント管理では、id, ユーザ名、パスワード、メールアドレスが必要。
予定管理では、id, ユーザ名、予定のタイトル、開始日時、終了日時、予定が終日であるかの判断が必要。
メモの投稿管理では、id, メッセージ内容、送信日時、ユーザ名が必要。
バイト情報のテンプレート管理では、id, ユーザ名、バイトの名前、時給、交通費、開始、終了が必要。
シフトの情報管理は、id, 時給、交通費、開始する年月日、開始する時間、開始する分、終了する年月日、終了する時間、終了する分、ユーザ名が必要。

# インストール
```
python -m venv venv
```
を用いて仮想環境を作成する。
その後
```
venv\Scripts\Activate
pip install -r requirements.txt
```
で実行環境が生成される。

# 使用方法
まずログイン画面に遷移し、アカウントを持っていない場合はユーザ登録画面に移動する。そこで必要事項の入力を行い、ログインする。
ホーム画面に遷移すると様々な機能がある。
予定登録で必要事項の入力を行いホーム画面に戻ると、予定が表示される。
予定削除では予定を選択することで、その予定を削除することができる。
予定更新では予定を選択し、必要事項の入力を行うことで更新を行う。
メモでは予定に関するメモの投稿や削除、更新を行うことが可能。
テンプレート追加ではバイト情報のテンプレートを作成することができる。
保存されたテンプレートはシフト追加の中で表示され、選択することでカレンダーにシフトを登録することができる。
テンプレート削除で、バイト情報のテンプレートの削除を行うことができる。
logoutでログアウトする。

# 担当箇所
ログイン画面、ユーザ登録画面、ホーム画面、予定追加、予定削除、予定更新とカレンダーに予定を表示する箇所に関わった。
