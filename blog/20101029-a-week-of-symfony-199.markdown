---
layout: default
title: A week of symfony #199 (18->24 October 2010)
---

A week of symfony #199 (18->24 October 2010)
============================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/10/24/a-week-of-symfony-199-18-24-october-2010)）

<br />
<br />
<hr />

先週、symfony プロジェクトは 5 周年を迎え、これを記念して Symfony2 の最後のメジャーコンポーネントとなる <a href="http://github.com/fabpot/symfony/commit/f216f313e8909015fe9961a5604d179f64c35a90">Security コンポーネント</a>が公開されました。また、Form コンポーネントと Validation コンポーネントに多くのコミットとパッチが送られました。

 
開発メーリングリスト
-------------------

  * [Symfony2: フォームとデータバインディング](http://groups.google.com/group/symfony-devs/browse_thread/thread/9ac2eade1d4a1603)
  * [GET パラメータを含む機能テスト](http://groups.google.com/group/symfony-devs/browse_thread/thread/937f10994a5829f6)
  * [フラッシュメッセージのベストプラクティス](http://groups.google.com/group/symfony-devs/browse_thread/thread/514d9653cf068725)
  * [Symfony2: 新しいセキュリティレイヤーについてのいくつかのアイデア](http://groups.google.com/group/symfony-devs/browse_thread/thread/cfba48ca5c4f756b)
  * [サードパーティーのバンドルの統合性の向上について](http://groups.google.com/group/symfony-devs/browse_thread/thread/e46e5bb74fc3a78b)


Symfony2 開発ハイライト
-----------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [ef4f61b](http://github.com/symfony/symfony/commit/ef4f61bb9fcbfcb5bd7c5a0e2340a8dd30db8651 "ef4f61bb9fcbfcb5bd7c5a0e2340a8dd30db8651 commit on github"): \[DependencyInjection\] 生成されるコンテナクラスのシグニチャーに TaggedContainerInterface を追加
  * [5d4c80f](http://github.com/symfony/symfony/commit/5d4c80f27b68b8ac568e5bb0ca74b07aadcdbafd "5d4c80f27b68b8ac568e5bb0ca74b07aadcdbafd commit on github"): \[Validator\] DependencyInjection の統合を削除
  * [e1f8423](http://github.com/symfony/symfony/commit/e1f842344eedc796133f78dd6015c39507422926 "e1f842344eedc796133f78dd6015c39507422926 commit on github")、[7639fde](http://github.com/symfony/symfony/commit/7639fde3f247f28ccb85b3050478e3a0b97218b9 "7639fde3f247f28ccb85b3050478e3a0b97218b9 commit on github"): \[FrameworkBundle\] DIC タグベース制約バリデータファクトリを追加
  * [7225cf6](http://github.com/symfony/symfony/commit/7225cf64b1854753f6713664ac2a97ea6941f6dd "7225cf64b1854753f6713664ac2a97ea6941f6dd commit on github")、[c543692](http://github.com/symfony/symfony/commit/c543692891947a0ba694855ff3449e4501eab98c "c543692891947a0ba694855ff3449e4501eab98c commit on github")、[71ace34](http://github.com/symfony/symfony/commit/71ace348222348eda7bf0007ce2e4b6dfc0c6e51 "71ace348222348eda7bf0007ce2e4b6dfc0c6e51 commit on github")、[dbfa06c](http://github.com/symfony/symfony/commit/dbfa06c54feb81eecfc64d4e44447cbed5919df0 "dbfa06c54feb81eecfc64d4e44447cbed5919df0 commit on github"): ユニットテストを追加
  * [2dc357d](http://github.com/symfony/symfony/commit/2dc357d3a8233672997240d6c619a9e4c28cd2c4 "2dc357d3a8233672997240d6c619a9e4c28cd2c4 commit on github"): \[WebProfilerBundle\] ラベルの参照を修正、マークアップを修正、CSS と画像を最適化
  * [4a18624](http://github.com/symfony/symfony/commit/4a186249275f4c8b410714f0b892e318fe22c238 "4a186249275f4c8b410714f0b892e318fe22c238 commit on github"): \[Validator\] デフォルトの URL プロトコルから ftp と ftps を削除
  * [56d9830](http://github.com/symfony/symfony/commit/56d98305ca314c65ea9277f68f4c9892a35b4100 "56d98305ca314c65ea9277f68f4c9892a35b4100 commit on github"): フォームのフィールドグループのレンダリングを修正
  * [94347f7](http://github.com/symfony/symfony/commit/94347f73c5bff3040410605eb5de02dd14c2e60a "94347f73c5bff3040410605eb5de02dd14c2e60a commit on github"): \[HttpFoundation\] 現在の URI と指定したパスを元に URI を生成するメソッドを追加
  * [0fc6b15](http://github.com/symfony/symfony/commit/0fc6b15c1729035890cd137686f142b92c5f9650 "0fc6b15c1729035890cd137686f142b92c5f9650 commit on github"): \[HttpFoundation\] セッションの属性値をすべてクリアするメソッドを追加
  * [f216f31](http://github.com/symfony/symfony/commit/f216f313e8909015fe9961a5604d179f64c35a90 "f216f313e8909015fe9961a5604d179f64c35a90 commit on github")、[82f8ab8](http://github.com/symfony/symfony/commit/82f8ab839f13c30beaf29bb256a3b01e9e0320fe "82f8ab839f13c30beaf29bb256a3b01e9e0320fe commit on github")、[4027f75](http://github.com/symfony/symfony/commit/4027f751e39c8e96f7f960df49e5ddde736a3d02 "4027f751e39c8e96f7f960df49e5ddde736a3d02 commit on github"): セキュリティコンポーネント、およびコンポーネントの MVC フレームワークへの統合機能を追加
  * [71228b5](http://github.com/symfony/symfony/commit/71228b5f29321b78be71912d2ea2f354c9abc79a "71228b5f29321b78be71912d2ea2f354c9abc79a commit on github"): \[FrameworkBundle\] ログアウトパスを設定できるように
  * [4b32114](http://github.com/symfony/symfony/commit/4b321141f9b76eea4bbd4cce3f9f2cb1bf704f83 "4b321141f9b76eea4bbd4cce3f9f2cb1bf704f83 commit on github"): \[FrameworkBundle\] switch-user ビヘイビアを設定できるように
  * [bdb0510](http://github.com/symfony/symfony/commit/bdb051083cc686832dc3359d7f2ec1504bafbab4 "bdb051083cc686832dc3359d7f2ec1504bafbab4 commit on github"): \[FrameworkBundle\] ログイン用のデフォルトコントローラを削除
  * [dd4f87b](http://github.com/symfony/symfony/commit/dd4f87b8c24de204897926bcff478fc04865c140 "dd4f87b8c24de204897926bcff478fc04865c140 commit on github"): フォームログインを設定可能に
  * [dd7e33a](http://github.com/symfony/symfony/commit/dd7e33af6bcb135d00fa008da0a0188713df615b "dd7e33af6bcb135d00fa008da0a0188713df615b commit on github"): \[TwigBundle\] include タグの挙動を、Twig 標準の include タグと同じになるように修正
  * [0ccc980](http://github.com/symfony/symfony/commit/0ccc9805f54ca46d4ea9fdda026b0779e858c616 "0ccc9805f54ca46d4ea9fdda026b0779e858c616 commit on github"): 先頭のスラッシュに関する UniversalClassLoader の問題を修正
  * <del>[e8bcbcb](http://github.com/symfony/symfony/commit/e8bcbcba57b210246a1d6b5d0fcf688b0a2d8afc "e8bcbcba57b210246a1d6b5d0fcf688b0a2d8afc commit on github"): \[Routing\] XML ローダーで複数のルーティング要件を使えるように</del>
  * [0749038](http://github.com/symfony/symfony/commit/0749038e73b0def26abfefa5cc40f30683c7b460 "0749038e73b0def26abfefa5cc40f30683c7b460 commit on github"): \[Security\] パスワードの比較処理を変更し、タイミング攻撃を回避
  * [acfd09e](http://github.com/symfony/symfony/commit/acfd09eeb31dbf8592da44e0d3aa1091fc6076db "acfd09eeb31dbf8592da44e0d3aa1091fc6076db commit on github"): \[FrameworkBundle\] コンフィギュレーションでパスワードが指定されていない場合にランダムなパスワードを生成
  * [eaef939](http://github.com/symfony/symfony/commit/eaef939141b0b62cdbab9cba5271a1c486cbcdd7 "eaef939141b0b62cdbab9cba5271a1c486cbcdd7 commit on github"): \[Form\] Value Transformer で空の値を適切に処理し、チェーンできるように修正（この変更により、DateField に空の値が送信された場合に null を返さないバグを修正）
  * [733290c](http://github.com/symfony/symfony/commit/733290c112a86b7147b0c477d28bde6f74e702ef "733290c112a86b7147b0c477d28bde6f74e702ef commit on github"): \[Form\] UrlField を実装
  * [e4c2170](http://github.com/symfony/symfony/commit/e4c21708caedfaf7d3fc78a43003972ad7e66d9d "e4c21708caedfaf7d3fc78a43003972ad7e66d9d commit on github"): \[Form\] Normalization Transformer からValue Transformerを分離
  * [6c7fab2](http://github.com/symfony/symfony/commit/6c7fab212b1f715945001ca95616877b6d70570e "6c7fab212b1f715945001ca95616877b6d70570e commit on github"): \[Form\] DateField の年、月、日のバリデーションを追加
  * [72dcee5](http://github.com/symfony/symfony/commit/72dcee594a321a758bc5ee22c403ccdc0f32ddab "72dcee594a321a758bc5ee22c403ccdc0f32ddab commit on github"): \[Form\] TimeField の時、分、秒のバリデーションを追加
  * [96a0bff](http://github.com/symfony/symfony/commit/96a0bff9151d45660cfda178142a7851b7a0cccc "96a0bff9151d45660cfda178142a7851b7a0cccc commit on github"): \[Form\] InputField をインスタンス化できるように変更し、単純な入力フィールドを作成可能に
  * [d077ac4](http://github.com/symfony/symfony/commit/d077ac415887b2b8561ce9604d876b57b646c455 "d077ac415887b2b8561ce9604d876b57b646c455 commit on github"): \[Security\] エンコーダにおいて、可能であれば hash() 関数を使うように変更し、デフォルトの暗号化アルゴリズムを sha1 から sha256 へ変更



> **NOTE**
> 翻訳者コメント<br />
> [hidenorigoto]

