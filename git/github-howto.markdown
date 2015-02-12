---
layout: default
title: GitHub の使い方
---

GitHub の使い方
===============


GitHub への登録
---------------

GitHub は無料でアカウントを登録することができます。
Symfony ユーザー会コンテンツの編集などは、すべて無料のアカウントのみで行うことができます。

アカウントの登録は、[GitHub のアカウント種別ページ](http://github.com/plans)で「Free!」欄の「Sign Up!」をクリックし、フォームに適宜情報を入力するのみです。


### アイコンの登録

GitHub のアカウントアイコンは、GRAVATAR という外部サービスを利用しています。
ご自分のアイコン画像を登録したい場合は、[Gravatar](http://ja.gravatar.com/) のサイトにもアカウントを登録し、お好きな画像を登録してください。

> **CAUTION**
> GitHub に登録したメールアドレスと Gravatar に登録したメールアドレスが一致していないと、正しくアイコン画像が表示されないことに注意して下さい。



既存リポジトリのフォーク（Fork）
--------------------------------

既存のリポジトリをフォークするには、単にフォークしたいリポジトリに Web ブラウザでアクセスし、「フォーク」ボタンをクリックするだけです。

![フォークボタン](images/github/fork.png)


しばらくすると、自分のダッシュボードにフォークされたリポジトリが追加されます。



リポジトリのコンテンツの編集（簡易）
------------------------------------

リポジトリのコンテンツは、GitHub の Web サイトで、Web ブラウザから直接編集することができます。手順は以下のとおりです。

1. GitHub の自分のリポジトリで編集したいコンテンツのページを表示する。
2. コンテンツの右上にある「edit」ボタンをクリックする。
   ![edit ボタン](images/github/edit.png)
3. 適宜内容を編集する。
4. 編集が完了したら、編集内容の説明を「Commit Message」欄に入力し、「Commit」ボタンをクリックする。

これだけで、コンテンツを編集できます。



リポジトリのコンテンツの編集（上級者向け）
------------------------------------------

多くのドキュメントを編集する場合などは、ウェブブラウザでは作業効率がよくありません。
ご自分のローカルコンピューターに Git の環境をセットアップすれば、お気に入りのテキストエディタなどでコンテンツの編集を行えます。

これには以下のような作業が必要になり、説明が高度になるため、ここでは参考となるブログへのリンクのみ紹介します。

### 必要な作業

- Git のインストール
- SSH 鍵ペアの作成、登録


### 参考リンク

- [Windows 上に Git 環境を構築する方法(TortoiseGit と msysGit)](setup-git-windows)
- [はじめてのgithub - blog.katsuma.tv](http://blog.katsuma.tv/2009/02/first_github.html)
- [CygwinでGit(GitHub)を始めるための準備・設定メモ - Rewish](http://rewish.org/tools/cygwin_github)
- [github を使うためのメモ。 - WOMO](http://womo.nconc.net/2010/03/04/github)



編集したコンテンツを元のリポジトリに反映する（プルリクエスト）
--------------------------------------------------------------

フォークした自分のリポジトリでコンテンツの編集が完了したら、自分の変更を元のリポジトリに反映（マージ）してもらうために、元のリポジトリの管理者へプルリクエスト（Pull Request）を送信します。

プルリクエストを送信するには、単に自分のリポジトリに Web ブラウザでアクセスし、右上にある「プルリクエスト」ボタンを押すだけです。

![プルリクエストボタン](images/github/pullrequest.png)

> **NOTE**
> Commit メッセージと同様に、プルリクエスト送信時に変更箇所の概要などをメッセージ欄に記入してください。



プルリクエストを受け取った場合のマージの仕方
--------------------------------------------

自分のリポジトリに対して他の人が修正などを行い、プルリクエストを受信した場合、以下の手順でマージします。

  1. 修正した人のリポジトリを自分の作業リポジトリのリモートに追加する。
  2. 修正した人のブランチに切り替え、pull する。
  3. 自分の元のブランチに戻り、マージする。

コマンドは、例えば以下のようになります。

    # リモートに追加
    $ git remote add hidenorigoto git://github.com/hidenorigoto/sfjp-doc-main.git

    # ブランチの切り替え
    $ git checkout -b hidenorigoto/master

    # 最新をpull
    $ git pull hidenorigoto master

    # 元のブランチに戻る
    $ git checkout master

    # マージする
    $ git merge hidenorigoto/master


コンフリクトのないマージであれば、単に pull するだけでもできます。

    $ git remote add hidenorigoto git://github.com/hidenorigoto/sfjp-doc-main.git
    $ git checkout master
    $ git pull hidenorigoto master



参考リンク（その他）
--------------------

Git を使う上での参考となるページなどを紹介します。

  - [Pro Git](http://progit.org/book/ja/)<br />
    すべてオンラインでフリーで読める Git の解説書。内容も新しく Git を使う上では必読。
  - [Git入門](http://www8.atwiki.jp/git_jp/)
  - [git(1) Manual Page](http://www.kernel.org/pub/software/scm/git/docs/)<br />
    git コマンドのリファレンス
  - [Gitの使い方 - SourceForge.JPドキュメント管理](http://sourceforge.jp/docs/Git%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9)
  - [知らないと損をするgit - Absolute Playing!](http://d.hatena.ne.jp/Kiske/20081003/1223008270)
  - [GitとGitHubを覚えよう](http://osc-tokyo-git.phper.jp/)<br />
    OSC Tokyo 2011 Springのセミナーで使った資料です。
