A week of symfony #201 (1->7 November 2010)
===========================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/11/07/a-week-of-symfony-201-1-7-november-2010)）

<br />
<br />
<hr />

今週のSymfony2の開発はユニットテストに集中して行われました。数百の新しいテストが追加され、その大部分はセキュリティコンポーネントに関連するものです。メーリングリストでも様々な議論が行われました。
 
開発メーリングリスト
------------------------

  * [コントローラ内における$this['servicename']の表記が適正かどうか](http://groups.google.com/group/symfony-devs/browse_thread/thread/1badb342882f2f7a)
  * [Symfony2 ログインフォームでリダイレクトのループが起こる](http://groups.google.com/group/symfony-devs/browse_thread/thread/3d7a80a5308256e8)
  * [Symfony2 DoctrineUserBundleを使った場合のフォームバリデーションについて](http://groups.google.com/group/symfony-devs/browse_thread/thread/97021a9b5739b39c)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [a4fbf74](http://github.com/symfony/symfony/commit/a4fbf74593cb81a5dc3f2fcde64c491e37a4de38 "a4fbf74593cb81a5dc3f2fcde64c491e37a4de38 commit on github"): DoctrineMongoDBBundleにユーザプロバイダーを追加
  * [a5d4acc](http://github.com/symfony/symfony/commit/a5d4acc54ddd8536404fd3348752865156702800 "a5d4acc54ddd8536404fd3348752865156702800 commit on github"): \[HttpFoundation\] get()メソッドの引数にデフォルト値を設定できるよう変更
  * [ae888b8](http://github.com/symfony/symfony/commit/ae888b80f65e4f28803dc28e9f869bcfd3289782 "ae888b80f65e4f28803dc28e9f869bcfd3289782 commit on github"): \[HttpFoundation\] バックアップ値(SERVER_NAME, SERVER_ADDR)と形式が一致するように、ヘッダーより取得するホスト名からポート番号を削除
  * [dd9b77e](http://github.com/symfony/symfony/commit/dd9b77ed96e768bd0c54755b0ea88272febea285 "dd9b77ed96e768bd0c54755b0ea88272febea285 commit on github"): \[HttpFoundation\] Response::setVary()メソッドを追加
  * [3d5054f](http://github.com/symfony/symfony/commit/3d5054f21fc92a9cff70b5e87f467295252c52a6 "3d5054f21fc92a9cff70b5e87f467295252c52a6 commit on github"): \[Security\] 認証機能のユニットテストを追加
  * [ec41757](http://github.com/symfony/symfony/commit/ec417578caa531a3854ef3c76914471ed22504e9 "ec417578caa531a3854ef3c76914471ed22504e9 commit on github"), [a19cdce](http://github.com/symfony/symfony/commit/a19cdce1bcd93cb30a34a3011f745439b9215d40 "a19cdce1bcd93cb30a34a3011f745439b9215d40 commit on github"): \[Security\] 認証機能のプロバイダーのためのユニットテストを追加 (セキュリティコンポーネントにおける現在のコードカバレッジは96%以上です)
  * [58bd4ac](http://github.com/symfony/symfony/commit/58bd4acdd167a6f47343abf5f9eeec99877ab0c5 "58bd4acdd167a6f47343abf5f9eeec99877ab0c5 commit on github"): \[Translation\] ユニットテストを追加
  * [556bfcb](http://github.com/symfony/symfony/commit/556bfcb804b11f2027522d108007e4f7dff86076 "556bfcb804b11f2027522d108007e4f7dff86076 commit on github"): \[HttpKernel\] ユニットテストを追加
  * [5bd03e1](http://github.com/symfony/symfony/commit/5bd03e1c588cc39ddd3cc211a468f72a1bcf8d20 "5bd03e1c588cc39ddd3cc211a468f72a1bcf8d20 commit on github"): \[HttpKernel\] ESIのユニットテストを追加
  * [e7ea2eb](http://github.com/symfony/symfony/commit/e7ea2eb433ff05ae4302b6e3b1c3e7b3fcefacae "e7ea2eb433ff05ae4302b6e3b1c3e7b3fcefacae commit on github"): \[FrameworkBundle\] レスポンスの形式が不明な場合も、確実に例外を飛ばすよう修正

<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> 来年の2月、3月に行われるSymfony Live 2011の参加受付が始まっています。
> 日本Symfonyユーザ会からも何人かの有志が参加する予定です。
> [こちらのページ](http://symfony.gr.jp/events/20101103-symfony-live-2011)にて参加者募集を行っているので、興味のある方はぜひJoinしてみてください！
> [yuchimiri]
