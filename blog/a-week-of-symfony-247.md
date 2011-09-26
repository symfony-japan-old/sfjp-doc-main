A week of symfony #247 (19->25 September 2011)
==============================================

先週、いくつかのバグが修正されたSymfony2の [メンテナンスバージョン 2.0.3](http://symfony.com/blog/symfony-2-0-3-released)がリリースされました。
また、2.1 ブランチには [ユーザーパスワード用バリデータ](https://github.com/symfony/symfony/commit/7d3c2df98d993f5406e712e39b7b5a1b1059f814)、[繰り返しフィールドに異なるオプションを設定する機能](https://github.com/symfony/symfony/commit/8819db3923e9a2ea8b73b3d0eafcedc4ab899c6b)、クラスローダーにおける[PHP 5.4のトレイトサポート](https://github.com/symfony/symfony/commit/e5a23dbdaa0f33a282d425d706c8622f58776016)といった、興味深い機能が追加されました。
また、symfony 開発者が集まり、[さまざまなトピック](https://gist.github.com/1235987)についての議論が行われました。
 
開発メーリングリスト
--------------------

  * [IDEへのSymfonyのパッケージング](https://groups.google.com/forum/#!topic/symfony-devs/PLKiBU3HEQk)
  * [Sf2 HTTP CACHE - ESI での問題](https://groups.google.com/forum/#!topic/symfony-devs/93LdIp0rRAE)

Symfony2 開発ハイライト
-----------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [903ab81](http://github.com/symfony/symfony/commit/903ab81434269ec776030a25b3dbadf789c991a5 "903ab81434269ec776030a25b3dbadf789c991a5 commit on github"): \[Translation\] support Ini file format
  * [83199ae](http://github.com/symfony/symfony/commit/83199aec0093918c1820e738a8c3e2be9842c71f "83199aec0093918c1820e738a8c3e2be9842c71f commit on github"): \[FrameworkBundle\] fixed unintuitive merging behavior for assets_base_urls
  * [a0329c3](http://github.com/symfony/symfony/commit/a0329c37c9a00c594bd41fc178ad444926a86da3 "a0329c37c9a00c594bd41fc178ad444926a86da3 commit on github"): added lifetime/cleanup support for MongoDbProfilerStorage
  * [bca551e](http://github.com/symfony/symfony/commit/bca551e86fdba47064454fbabcaf88801aa5da7f "bca551e86fdba47064454fbabcaf88801aa5da7f commit on github"), [cf736cc](http://github.com/symfony/symfony/commit/cf736ccde38465dce8355c7ff2d9d69ef2deded6 "cf736ccde38465dce8355c7ff2d9d69ef2deded6 commit on github"): \[DomCrawler\] ChoiceFormField should take the content when value is unavailable
  * [022a9a7](http://github.com/symfony/symfony/commit/022a9a7a6e8af993957a490561e9ba0c0d4a804f "022a9a7a6e8af993957a490561e9ba0c0d4a804f commit on github"): \[Security\] made saving target_path extendible
  * [7d3c2df](http://github.com/symfony/symfony/commit/7d3c2df98d993f5406e712e39b7b5a1b1059f814 "7d3c2df98d993f5406e712e39b7b5a1b1059f814 commit on github"): \[SecurityBundle\] added a validator for the user password (this validator is useful when you want to validate that an input value is equal to the user current password)
  * [64d44fb](http://github.com/symfony/symfony/commit/64d44fbb9332f7973a21ca9c428d64b3c29ba23d "64d44fbb9332f7973a21ca9c428d64b3c29ba23d commit on github"): \[Translator\] fixed recursion when using a fallback that is the same as the locale
  * [3e90ba4](http://github.com/symfony/symfony/commit/3e90ba4f76ba231f828c50f5e22168e1ceb28e73 "3e90ba4f76ba231f828c50f5e22168e1ceb28e73 commit on github"), [56b6d53](http://github.com/symfony/symfony/commit/56b6d537d6f803e3b497292c14f16fdfd1514126 "56b6d537d6f803e3b497292c14f16fdfd1514126 commit on github"): \[WebProfileBundle\] added missing position attribute in XSD
  * [e98584e](http://github.com/symfony/symfony/commit/e98584e2f3aa931192642e5179cd9919330c612b "e98584e2f3aa931192642e5179cd9919330c612b commit on github"): \[WebProfilerBundle\] tweaked some templates
  * [c9ddd6f](http://github.com/symfony/symfony/commit/c9ddd6fd8b647764f2d2bca64d97cff2cab1ea34 "c9ddd6fd8b647764f2d2bca64d97cff2cab1ea34 commit on github"): \[WebProfilerBundle\] moved the token not found error to the new info page
  * [e5a23db](http://github.com/symfony/symfony/commit/e5a23dbdaa0f33a282d425d706c8622f58776016 "e5a23dbdaa0f33a282d425d706c8622f58776016 commit on github"): \[ClassLoader\] added support for PHP 5.4 traits
  * [98abc8e](http://github.com/symfony/symfony/commit/98abc8ed050d831b9a93b8da31c6453662d80d04 "98abc8ed050d831b9a93b8da31c6453662d80d04 commit on github"): \[DependencyInjection\] changed the default YAML indentation to 4 spaces instead of 2
  * [b6c8f63](http://github.com/symfony/symfony/commit/b6c8f639f071b0baa52dcfac3322a41dd26d1aa4 "b6c8f639f071b0baa52dcfac3322a41dd26d1aa4 commit on github"): \[TwigBridge\] fixed message keys extraction when no domain is defined in the template
  * [e0ace8e](http://github.com/symfony/symfony/commit/e0ace8eaee2756c60d79681d907b01875d06e7dc "e0ace8eaee2756c60d79681d907b01875d06e7dc commit on github"), [b8e5a15](http://github.com/symfony/symfony/commit/b8e5a155e4f0dad7e1d7a687e6e99e48d6447696 "b8e5a155e4f0dad7e1d7a687e6e99e48d6447696 commit on github"): \[DependencyInjection\] fixed array support for the ini loader
  * [ae3aded](http://github.com/symfony/symfony/commit/ae3aded83fbb03a0b043a8c13851c53f8086ed6d "ae3aded83fbb03a0b043a8c13851c53f8086ed6d commit on github"), [d830253](http://github.com/symfony/symfony/commit/d83025387636487163a96d37336be89885e452a0 "d83025387636487163a96d37336be89885e452a0 commit on github"), [e2945c9](http://github.com/symfony/symfony/commit/e2945c9f9b886d19d67291a5bce1ca6da572ae64 "e2945c9f9b886d19d67291a5bce1ca6da572ae64 commit on github"): added PCRE_DOTALL modifier to RouteCompiler to allow urlencoded linefeed in route parameters
  * [8819db3](http://github.com/symfony/symfony/commit/8819db3923e9a2ea8b73b3d0eafcedc4ab899c6b "8819db3923e9a2ea8b73b3d0eafcedc4ab899c6b commit on github"), [0679220](http://github.com/symfony/symfony/commit/0679220b45f9d1f541afbc238a972c15f4276c4e "0679220b45f9d1f541afbc238a972c15f4276c4e commit on github"), [f8a6a4b](http://github.com/symfony/symfony/commit/f8a6a4b1e56f4f3d8e7c32f5a6b6e3884c462945 "f8a6a4b1e56f4f3d8e7c32f5a6b6e3884c462945 commit on github"), [78ebe11](http://github.com/symfony/symfony/commit/78ebe11a0c74cde826c93c3da7228f0d34e1e16d "78ebe11a0c74cde826c93c3da7228f0d34e1e16d commit on github"): \[Form\] allow setting different options to repeating fields

