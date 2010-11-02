A week of symfony #199 (18->24 October 2010)
============================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/10/03/a-week-of-symfony-196-27-september-3-october-2010)）

<br />
<br />
<hr />

先週、symfonyプロジェクトは5周年を迎え、これを記念してSymfony2の最後のメジャーコンポーネントとなる<a href="http://github.com/fabpot/symfony/commit/f216f313e8909015fe9961a5604d179f64c35a90">セキュリティコンポーネントt</a>が公開されました。また、フォームコンポーネントとバリデーションコンポーネントに多くのコミットとパッチが送られました。

 
開発メーリングリスト
-------------------

  * [Symfony2: フォームとデータバインディング](http://groups.google.com/group/symfony-devs/browse_thread/thread/9ac2eade1d4a1603)
  * [GET パラメーターを含む機能テスト](http://groups.google.com/group/symfony-devs/browse_thread/thread/937f10994a5829f6)
  * [フラッシュメッセージのベストプラクティス](http://groups.google.com/group/symfony-devs/browse_thread/thread/514d9653cf068725)
  * [Symfony2: 新しいセキュリティレイヤーについてのいくつかのアイデア](http://groups.google.com/group/symfony-devs/browse_thread/thread/cfba48ca5c4f756b)
  * [サードパーティのバンドルの](http://groups.google.com/group/symfony-devs/browse_thread/thread/e46e5bb74fc3a78b)


Symfony2 開発ハイライト
-----------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [ef4f61b](http://github.com/symfony/symfony/commit/ef4f61bb9fcbfcb5bd7c5a0e2340a8dd30db8651 "ef4f61bb9fcbfcb5bd7c5a0e2340a8dd30db8651 commit on github"): \[DependencyInjection\] added TaggedContainerInterface to signature of generated container classes
  * [5d4c80f](http://github.com/symfony/symfony/commit/5d4c80f27b68b8ac568e5bb0ca74b07aadcdbafd "5d4c80f27b68b8ac568e5bb0ca74b07aadcdbafd commit on github"): \[Validator\] removed DependencyInjection integration
  * [e1f8423](http://github.com/symfony/symfony/commit/e1f842344eedc796133f78dd6015c39507422926 "e1f842344eedc796133f78dd6015c39507422926 commit on github"), [7639fde](http://github.com/symfony/symfony/commit/7639fde3f247f28ccb85b3050478e3a0b97218b9 "7639fde3f247f28ccb85b3050478e3a0b97218b9 commit on github"): \[FrameworkBundle\] added a DIC tag-based constraint validator factory
  * [7225cf6](http://github.com/symfony/symfony/commit/7225cf64b1854753f6713664ac2a97ea6941f6dd "7225cf64b1854753f6713664ac2a97ea6941f6dd commit on github"), [c543692](http://github.com/symfony/symfony/commit/c543692891947a0ba694855ff3449e4501eab98c "c543692891947a0ba694855ff3449e4501eab98c commit on github"), [71ace34](http://github.com/symfony/symfony/commit/71ace348222348eda7bf0007ce2e4b6dfc0c6e51 "71ace348222348eda7bf0007ce2e4b6dfc0c6e51 commit on github"), [dbfa06c](http://github.com/symfony/symfony/commit/dbfa06c54feb81eecfc64d4e44447cbed5919df0 "dbfa06c54feb81eecfc64d4e44447cbed5919df0 commit on github"): added more unit tests
  * [2dc357d](http://github.com/symfony/symfony/commit/2dc357d3a8233672997240d6c619a9e4c28cd2c4 "2dc357d3a8233672997240d6c619a9e4c28cd2c4 commit on github"): \[WebProfilerBundle\] fixed label reference, fixed markup, optimized css and images
  * [4a18624](http://github.com/symfony/symfony/commit/4a186249275f4c8b410714f0b892e318fe22c238 "4a186249275f4c8b410714f0b892e318fe22c238 commit on github"): \[Validator\] removed ftp and ftps from default url protocols
  * [56d9830](http://github.com/symfony/symfony/commit/56d98305ca314c65ea9277f68f4c9892a35b4100 "56d98305ca314c65ea9277f68f4c9892a35b4100 commit on github"): fixed form field groups rendering
  * [94347f7](http://github.com/symfony/symfony/commit/94347f73c5bff3040410605eb5de02dd14c2e60a "94347f73c5bff3040410605eb5de02dd14c2e60a commit on github"): \[HttpFoundation\] added a way to generate a URI based on the current one and a path
  * [0fc6b15](http://github.com/symfony/symfony/commit/0fc6b15c1729035890cd137686f142b92c5f9650 "0fc6b15c1729035890cd137686f142b92c5f9650 commit on github"): \[HttpFoundation\] added a way to clear the session attributes
  * [f216f31](http://github.com/symfony/symfony/commit/f216f313e8909015fe9961a5604d179f64c35a90 "f216f313e8909015fe9961a5604d179f64c35a90 commit on github"), [82f8ab8](http://github.com/symfony/symfony/commit/82f8ab839f13c30beaf29bb256a3b01e9e0320fe "82f8ab839f13c30beaf29bb256a3b01e9e0320fe commit on github"), [4027f75](http://github.com/symfony/symfony/commit/4027f751e39c8e96f7f960df49e5ddde736a3d02 "4027f751e39c8e96f7f960df49e5ddde736a3d02 commit on github"): added the Security Component and its integration into the MVC framework
  * [71228b5](http://github.com/symfony/symfony/commit/71228b5f29321b78be71912d2ea2f354c9abc79a "71228b5f29321b78be71912d2ea2f354c9abc79a commit on github"): \[FrameworkBundle\] added a way to configure the logout paths
  * [4b32114](http://github.com/symfony/symfony/commit/4b321141f9b76eea4bbd4cce3f9f2cb1bf704f83 "4b321141f9b76eea4bbd4cce3f9f2cb1bf704f83 commit on github"): \[FrameworkBundle\] added a way to configure the switch-user behavior
  * [bdb0510](http://github.com/symfony/symfony/commit/bdb051083cc686832dc3359d7f2ec1504bafbab4 "bdb051083cc686832dc3359d7f2ec1504bafbab4 commit on github"): \[FrameworkBundle\] removed default controller for login
  * [dd4f87b](http://github.com/symfony/symfony/commit/dd4f87b8c24de204897926bcff478fc04865c140 "dd4f87b8c24de204897926bcff478fc04865c140 commit on github"): made form login configurable
  * [dd7e33a](http://github.com/symfony/symfony/commit/dd7e33af6bcb135d00fa008da0a0188713df615b "dd7e33af6bcb135d00fa008da0a0188713df615b commit on github"): \[TwigBundle\] fixed the include tag to behave like the standard Twig include tag
  * [0ccc980](http://github.com/symfony/symfony/commit/0ccc9805f54ca46d4ea9fdda026b0779e858c616 "0ccc9805f54ca46d4ea9fdda026b0779e858c616 commit on github"): fixed UniversalClassLoader issues with leading slashes
  * <del>[e8bcbcb](http://github.com/symfony/symfony/commit/e8bcbcba57b210246a1d6b5d0fcf688b0a2d8afc "e8bcbcba57b210246a1d6b5d0fcf688b0a2d8afc commit on github"): \[Routing\] allowed multiple routing requirement with xml loader</del>
  * [0749038](http://github.com/symfony/symfony/commit/0749038e73b0def26abfefa5cc40f30683c7b460 "0749038e73b0def26abfefa5cc40f30683c7b460 commit on github"): \[Security\] changed the way passwords are compared to avoid timing attacks
  * [acfd09e](http://github.com/symfony/symfony/commit/acfd09eeb31dbf8592da44e0d3aa1091fc6076db "acfd09eeb31dbf8592da44e0d3aa1091fc6076db commit on github"): \[FrameworkBundle\] generate a random password if none is provided in the configuration
  * [eaef939](http://github.com/symfony/symfony/commit/eaef939141b0b62cdbab9cba5271a1c486cbcdd7 "eaef939141b0b62cdbab9cba5271a1c486cbcdd7 commit on github"): \[Form\] changed value transformers to be responsible for processing empty values to be able to chain them properly (this change fixes the bug that DateField did not return NULL when submitted without values)
  * [733290c](http://github.com/symfony/symfony/commit/733290c112a86b7147b0c477d28bde6f74e702ef "733290c112a86b7147b0c477d28bde6f74e702ef commit on github"): \[Form\] implemented UrlField
  * [e4c2170](http://github.com/symfony/symfony/commit/e4c21708caedfaf7d3fc78a43003972ad7e66d9d "e4c21708caedfaf7d3fc78a43003972ad7e66d9d commit on github"): \[Form\] separated value transformers from normalization transformers
  * [6c7fab2](http://github.com/symfony/symfony/commit/6c7fab212b1f715945001ca95616877b6d70570e "6c7fab212b1f715945001ca95616877b6d70570e commit on github"): \[Form\] added validation of years, months and days to DateField
  * [72dcee5](http://github.com/symfony/symfony/commit/72dcee594a321a758bc5ee22c403ccdc0f32ddab "72dcee594a321a758bc5ee22c403ccdc0f32ddab commit on github"): \[Form\] added validation of hours, minutes and seconds to TimeField
  * [96a0bff](http://github.com/symfony/symfony/commit/96a0bff9151d45660cfda178142a7851b7a0cccc "96a0bff9151d45660cfda178142a7851b7a0cccc commit on github"): \[Form\] made InputField instantiable so that simple input fields can be created on the fly
  * [d077ac4](http://github.com/symfony/symfony/commit/d077ac415887b2b8561ce9604d876b57b646c455 "d077ac415887b2b8561ce9604d876b57b646c455 commit on github"): \[Security\] changed encoders to use hash() function whenever possible and replaced sha1 with sha256 as default algorithm



> **NOTE**
> 翻訳者コメント<br />
> まだまだ「実案件で使うのはクレイジーだ」と [fabien さんのスライド](http://www.slideshare.net/fabpot/the-state-of-symfony2-symfonyday-2010)でも書かれている Symfony2 ですが、徐々にいろいろな機能が形になってきているようです。また Symfony2 とは別に、Doctrine2 自体もかなり開発が進んでお> [hidenorigoto]

