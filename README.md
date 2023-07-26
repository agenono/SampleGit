# Git 入門

## 自己紹介：オサミー

- ソフトウェアエンジニア。株式会社プレジニア代表取締役。
- iPhone アプリ開発歴 10 年。企画開発した iPhone アプリ 160 万ダウンロード以上。
- Git 歴 10 年。

## ３部構成になってます

1. 理論編
2. 手を動かしてみよう Sourcetree 編
3. 手を動かしてみよう コマンドライン編

---

# 1.理論編

## 理論編アジェンダ

- なぜ Git を覚える必要があるのか？
- Git とは
- Git がなぜうまれたか
- Git の何が便利？
- 用語説明

## なぜ Git を覚える必要があるのか？

- ソフトウェア開発の現場で、Git を使っていないプロジェクトは「ない」
- ソフトウェアエンジニアになるのに、Git 使えるのはマスト
- Web アプリ/ゲーム/ネイティブアプリ/機械学習 etc.領域問わずすべてのソフトウェアエンジニアに有用

## Git とは

- ソースコードの変更履歴を記録・追跡するバージョン管理システム。
- See [サル先生の Git 入門](https://backlog.com/ja/git-tutorial/)

## Git がなぜうまれたか

### バージョン管理システムがないと...

- 変更履歴を残すためにファイルをたくさん残していた...！（写真で説明）
  - どのファイルが最新のものか区別できない
- チームで共有して作業している場合
  - 編集者の名前を入れておくことがある。誰がどのような変更を行ったか簡単にはわからない。
  - 二人で同時に編集してしまったために、先に編集した人の変更内容がわからず消してしまうこともありうる
- それらを解決するためにうまれたのは Git をはじめとする「バージョン管理システム」
  - 他　 SVN (SubVersion)

## Git の何が便利？

1. 「誰が」「何を」「いつ」ソースコードに修正を加えたのかわかる(変更履歴機能)
2. 超簡単にソースコードのバックアップがとれる(バックアップ機能)
3. 修正を並行でできる(ブランチ機能)

## 用語説明

### リポジトリとは

- ファイルやディレクトリの状態を記録する場所
- 比喩：「貯蔵庫」
- 変更履歴を管理したいディレクトリ(フォルダ)をリポジトリの管理下に置くことで、
  - そのディレクトリ内の変更履歴を記録することができる
- 自分の手元にリポジトリを作成する方法は二種類ある
  - 一つ目は全く新しいリポジトリを作成する方法
  - 二つ目はリモートリポジトリをコピーして作成する方法(クローン)

### コミットとは

- 記録すること
- 比喩：「(~~ポロライドカメラ~~ インスタントカメラ「チェキ」で)写真を取る」

### プッシュとは

- コミットしたものをリモートリポジトリに反映させること
- 比喩：「できた写真をコピーして宛先に送る」

## 作業の流れ

- 絵で説明
- 例えるならば
  - ① 作業(変更)=肉をいためる
  - ② ステージへ移動=料理をステージに上げる
  - ③ コミット=写真を撮る
  - ④ プッシュ=できた写真(紙)をコピーして宛先に送る
- 修正したら、add して commit して push!

---

# 2.手を動かしてみよう Sourcetree 編

## GUI(Sourcetree)か？CLI か？

- GUI: Graphical User Interface。視覚的にぱっとみてわかるインターフェース。マウスで操作可能。
- CLI: Command-line Interface。コマンド入力するインターフェース。マウスで操作不可。キーボードで操作。
- ソフトウェアエンジニアになりたければ、CLI(コマンド入力での操作)もある程度覚えておいたほうがよい
  - 普段使ってるのは GUI(Sourcetree)であるが、裏側でどんなコマンドが動いてるか理解をしておいたほうがよい
  - コマンド自体はすべて覚える必要ない。理解してれば OK。
- Git で何ができるかだけ知りたいのであれば、GUI(今回は Sourcetree)で OK。

## なぜ Sourcetree をインストールすべきか？

- 現場のソフトウェアエンジニアはほとんど（体感 8 割以上）は Sourcetree 使ってる
- もちろん CLI も使える

## Sourcetree とは？

- アトラシアン製の Git のクライアントアプリケーション。
- サイトみてみよう
  - https://www.sourcetreeapp.com
- Windows/Mac に対応

## 実践

### 前準備

- Git インストール(Mac はデフォルト入ってる)
- Sourcetree インストール

### 編集してコミットしてプッシュ！

- ① ローカルリポジトリ追加
- ② テキスト追加/編集
- ③ 変更をステージにあげる
- ④ コミット
- ⑤ 履歴を見る
- （Github でリポジトリ作成して）
- ⑥ プッシュ

### Git インストール

- Windows の人向け
  - [その他の環境での Git - Powershell で Git を使う](https://git-scm.com/book/ja/v2/Appendix-A%3A-%E3%81%9D%E3%81%AE%E4%BB%96%E3%81%AE%E7%92%B0%E5%A2%83%E3%81%A7%E3%81%AEGit-Powershell%E3%81%A7Git%E3%82%92%E4%BD%BF%E3%81%86)

---

# 3. 手を動かしてみよう CLI 編

## Git 使い方 基礎編として

- コマンドを使っていく
  - Visual Studio Code 付属のターミナルでよい。もしくは..
  - Mac のターミナル.app / iTerm.app
  - Windows の PowerShell
- Windows の人向け
  - [その他の環境での Git - Powershell で Git を使う](https://git-scm.com/book/ja/v2/Appendix-A%3A-%E3%81%9D%E3%81%AE%E4%BB%96%E3%81%AE%E7%92%B0%E5%A2%83%E3%81%A7%E3%81%AEGit-Powershell%E3%81%A7Git%E3%82%92%E4%BD%BF%E3%81%86)

## 絶対覚えておくべきコマンド

- 覚えておくべきコマンド 5 個だけ選べと言われたら、というのを選んでみた
- この 5 個だけは覚えてほしいっっっ！
- status, log, add, commit, push
- 他、init, clone

## ただし、全部は覚えてなくてもなんとかなる！

- Sourcetree など GUI で操作すれば、コマンド覚えなくてもなんとかなるから。
- でも、GUI の裏側で何の処理をしてるか **理解はしておくべき**
  - 現場のプロのエンジニアもすべてのコマンドを覚えてるわけではない
  - その都度ググっている
  - 理解はしている

## やってみよう！

- 前準備
  - Git は brew でインストールする(Mac デフォルトの Git は脆弱性がある)
  - 日本語ファイル名の文字化け回避
  - ユーザー名とメアド設定（グローバル or ローカル）
- パターン 1:ローカルリポジトリを作成する
  - リポジトリの作成(init)
  - ファイルの追跡(add)
  - ファイルのコミット(commit)
  - ファイルのプッシュ(push)
- パターン 2: リモートで作成済みリポジトリをクローン
  - クローン(clone)

### Homebrew で Git インストール

- もし Homebrew 未インストールだったら今すぐインストール！https://brew.sh/
  - Homebrew は Mac 用のパッケージ管理ツール。
  - これを使えば色々ツールを Mac にインストールできる。
- Homebrew で git をインストール
  - `brew install git` をたたく
- ~/.bash_profile に → を追記 `export PATH="/usr/local/Cellar/git/2.5.0/bin:$PATH"`
  - 方法は 2 つ。① エディタで編集する ② コマンドで一発で追加する
  - ① エディタで編集する場合
    - VSCode で　~/.bash_profile をひらいて編集
    - .bash_profile は不可視ファイルなので、Finder 上で Command+Shift+. で表示させる
    - もし、.bash_profile がない場合はつくりましょう
    - "~" は Home ディレクトリの意味。私の場合は `/Users/osamusuzuki/`
  - ② コマンドで一発で追加する
    - これ叩けば OK。
    - `echo 'export PATH="/usr/local/Cellar/git/2.5.0/bin:$PATH"' >> ~/.bash_profile`
- 最後に。~/.bash_profile を有効化
  - これ叩く → `source ~/.bash_profile`

### 日本語文字化け回避

- `git config --global core.quotepath false`

### ユーザー名とメアド設定

- `git config --global user.name "osuzukiy"`
- `git config --global user.email "osuzuki@example.com"`

### 基本コマンド

- `git init`
  - ローカルリポジトリを作成する
- `git add`
  - ファイルの追跡を開始する
  - `git add [file_name]`
  - `git add *`
- `git commit`
  - 変更履歴を記録する
  - `git commit -m "[Commit message]"`
  - `git commit -m "句読点を追加。"`
- `git push`
  - ローカルの変更履歴をリモートリポジトリへアップロードする
  - `git push [alias] [branch]`
  - `git push origin master`
- `git clone`
  - リモートリポジトリをダウンロードする
  - `git clone [url]`
  - `git clone https://github.com/osmszk/SampleGit.git`

#### 確認系コマンド

- `git status`
  - 追跡対象等ファイルの状態を確認する
  - どのファイルが変更されたか？
- `git diff`
  - ファイルがどのように変更されたか「変更の中身」を確認する
- `git log`
  - 過去の変更履歴を確認する
  - `git log --pretty=format:"%h %s" --graph`

#### リモートリポジトリ系

- `git remote`
  - リモートリポジトリ確認など
  - `git remote add origin https://github.com/osmszk/SampleGit.git`
- `git pull`
  - リモートリポジトリからダウンロードし差分を反映する
- `git fetch`
  - リモートリポジトリから履歴データをダウンロードする

#### ブランチ系(中級)

- `git branch`
  - ブランチを確認するなど(作成, 削除)
  - `git branch [branch_name]`
- `git checkout [branch_name]`
  - 指定されたブランチに切り替え、作業ディレクトリを更新
- `git merge [branch-name]`
  - ブランチを統合する

## 最後に

### ソフトウェアエンジニアとして仕事で使うためには..

- これだけでは足りない
- 下記も理解しておく必要がある
  - ブランチ
    - プルリクエスト
    - レビュー
    - コンフリクト
    - マージ
    - ブランチ戦略 git-flow
  - タグ
  - .gitignore
    - 無視したいファイル
- ニーズがあれば次回解説！

## ドキュメント読みましょう！

- Book
  - 日本語版　https://git-scm.com/book/ja/v2
- チートシート
  - コマンドを覚えたい方向け[日本語版](https://github.github.com/training-kit/downloads/ja/github-git-cheat-sheet/)
  - [PDF](https://github.github.com/training-kit/downloads/ja/github-git-cheat-sheet.pdf)

---

今回の動画は以上です。

## このチャンネルについて

このチャンネルは、
プログラミングの話を中心にしていくチャンネルです。

自分はエンジニアでもあり、起業家でもあるので、
開発ネタだけでなく、ビジネスについても、今後も語っていきたいと思います。

よかったら、いいねとチャンネル登録、よろしくおねがいします〜！

みんなでテクノロジー勉強して
面白い世界を、つくっていきましょう！

ご視聴ありがとうございました！
ではまた！
