# Git入門

## 自己紹介：オサミー
- ソフトウェアエンジニア。株式会社プレジニア代表取締役。
- iPhoneアプリ開発歴10年。企画開発したiPhoneアプリ160万ダウンロード以上。
- Git歴10年。

## ３部構成になってます
1. 理論編
2. 手を動かしてみよう Sourcetree編
3. 手を動かしてみよう コマンドライン編

---

# 1.理論編
## 理論編アジェンダ
- なぜGitを覚える必要があるのか？
- Gitとは
- Gitがなぜうまれたか
- Gitの何が便利？
- 用語説明

## なぜGitを覚える必要があるのか？
- ソフトウェア開発の現場で、Gitを使っていないプロジェクトは「ない」
- ソフトウェアエンジニアになるのに、Git使えるのはマスト
- Webアプリ/ゲーム/ネイティブアプリ/機械学習etc.領域問わずすべてのソフトウェアエンジニアに有用

## Gitとは
- ソースコードの変更履歴を記録・追跡するバージョン管理システム。
- See [サル先生のGit入門](https://backlog.com/ja/git-tutorial/)

## Gitがなぜうまれたか
### バージョン管理システムがないと...
- 変更履歴を残すためにファイルをたくさん残していた...！（写真で説明）
    - どのファイルが最新のものか区別できない    
- チームで共有して作業している場合
    - 編集者の名前を入れておくことがある。誰がどのような変更を行ったか簡単にはわからない。
    - 二人で同時に編集してしまったために、先に編集した人の変更内容がわからず消してしまうこともありうる
- それらを解決するためにうまれたのはGitをはじめとする「バージョン管理システム」
    - 他　SVN (SubVersion)

## Gitの何が便利？
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
    - ①作業(変更)=肉をいためる
    - ②ステージへ移動=料理をステージに上げる
    - ③コミット=写真を撮る
    - ④プッシュ=できた写真(紙)をコピーして宛先に送る
- 修正したら、addしてcommitしてpush!


----------------------------


# 2.手を動かしてみよう Sourcetree編

## GUI(Sourcetree)か？CLIか？
- GUI: Graphical User Interface。視覚的にぱっとみてわかるインターフェース。マウスで操作可能。
- CLI: Command-line Interface。コマンド入力するインターフェース。マウスで操作不可。キーボードで操作。
- ソフトウェアエンジニアになりたければ、CLI(コマンド入力での操作)もある程度覚えておいたほうがよい
    - 普段使ってるのはGUI(Sourcetree)であるが、裏側でどんなコマンドが動いてるか理解をしておいたほうがよい
    - コマンド自体はすべて覚える必要ない。理解してればOK。
- Gitで何ができるかだけ知りたいのであれば、GUI(今回はSourcetree)でOK。

## なぜSourcetreeをインストールすべきか？
- 現場のソフトウェアエンジニアはほとんど（体感8割以上）はSourcetree使ってる
- もちろんCLIも使える

## Sourcetreeとは？
- アトラシアン製のGitのクライアントアプリケーション。
- サイトみてみよう
    - https://www.sourcetreeapp.com
- Windows/Macに対応

## 実践
### 前準備
- Gitインストール(Macはデフォルト入ってる)
- Sourcetreeインストール
### 編集してコミットしてプッシュ！
- ①ローカルリポジトリ追加
- ②テキスト追加/編集
- ③変更をステージにあげる
- ④コミット
- ⑤履歴を見る
- （Githubでリポジトリ作成して）
- ⑥プッシュ

### Gitインストール
- Windowsの人向け
    - [その他の環境でのGit - PowershellでGitを使う](https://git-scm.com/book/ja/v2/Appendix-A%3A-%E3%81%9D%E3%81%AE%E4%BB%96%E3%81%AE%E7%92%B0%E5%A2%83%E3%81%A7%E3%81%AEGit-Powershell%E3%81%A7Git%E3%82%92%E4%BD%BF%E3%81%86)


----------------------------

# 3. 手を動かしてみよう CLI編
## Git使い方 基礎編として
- コマンドを使っていく
    - Visual Studio Code付属のターミナルでよい。もしくは..
    - Macのターミナル.app / iTerm.app
    - WindowsのPowerShell
- Windowsの人向け
    - [その他の環境でのGit - PowershellでGitを使う](https://git-scm.com/book/ja/v2/Appendix-A%3A-%E3%81%9D%E3%81%AE%E4%BB%96%E3%81%AE%E7%92%B0%E5%A2%83%E3%81%A7%E3%81%AEGit-Powershell%E3%81%A7Git%E3%82%92%E4%BD%BF%E3%81%86)



## 絶対覚えておくべきコマンド
- 覚えておくべきコマンド5個だけ選べと言われたら、というのを選んでみた
- この5個だけは覚えてほしいっっっ！
- status, log, add, commit, push
- 他、init, clone

## ただし、全部は覚えてなくてもなんとかなる！
- SourcetreeなどGUIで操作すれば、コマンド覚えなくてもなんとかなるから。
- でも、GUIの裏側で何の処理をしてるか **理解はしておくべき**
    - 現場のプロのエンジニアもすべてのコマンドを覚えてるわけではない
    - その都度ググっている
    - 理解はしている

## やってみよう！
- 前準備
    - Gitはbrewでインストールする(MacデフォルトのGitは脆弱性がある)
    - 日本語ファイル名の文字化け回避
    - ユーザー名とメアド設定（グローバルorローカル）
- パターン1:ローカルリポジトリを作成する
    - リポジトリの作成(init)
    - ファイルの追跡(add)
    - ファイルのコミット(commit)
    - ファイルのプッシュ(push)
- パターン2: リモートで作成済みリポジトリをクローン
    - クローン(clone)

### HomebrewでGitインストール
- もしHomebrew未インストールだったら今すぐインストール！https://brew.sh/
    - HomebrewはMac用のパッケージ管理ツール。
    - これを使えば色々ツールをMacにインストールできる。
- Homebrewでgitをインストール
    - `brew install git` をたたく
- ~/.bash_profileに→を追記 `export PATH="/usr/local/Cellar/git/2.5.0/bin:$PATH"`
    - 方法は2つ。①エディタで編集する②コマンドで一発で追加する
    - ①エディタで編集する場合
        - VSCodeで　~/.bash_profileをひらいて編集
        - .bash_profileは不可視ファイルなので、Finder上でCommand+Shift+. で表示させる
        - もし、.bash_profileがない場合はつくりましょう
        - "~" は Homeディレクトリの意味。私の場合は `/Users/osamusuzuki/`
    - ②コマンドで一発で追加する
        - これ叩けばOK。
        - `echo 'export PATH="/usr/local/Cellar/git/2.5.0/bin:$PATH"' >> ~/.bash_profile`
- 最後に。~/.bash_profileを有効化 
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

-------------

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










