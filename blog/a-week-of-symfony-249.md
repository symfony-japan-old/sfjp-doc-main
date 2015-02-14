---
layout: default
title: A week of symfony #249 (3->9 October 2011)
---

A week of symfony #249 (3->9 October 2011)
==========================================

Symfony2 の更新は速いペースを維持しており、先週 [Symfony 2.0.4 がリリースされました](http://symfony.com/blog/symfony-2-0-4-released)。
また、独立した [Symfony2 のコードのセキュリティ監査](http://symfony.com/blog/symfony2-security-audit) と Twig のコードのセキュリティ監査の結果が公開されました。
最後に、これはとても重要なことですが、後方互換性のない変更が master ブランチにコミットされました。ロケール管理が Session クラスから Request クラスへ移動されました [詳細はこちら](https://github.com/symfony/symfony/commit/74bc699b270122b70b1de6ece47c726f5df8bd41)。
 
開発メーリングリスト
--------------------

  * [Session](https://groups.google.com/forum/#!topic/symfony-devs/0j1IdfekOHQ)
  * [\[RFC\] \[AsseticBundle\] バンドルのコンフィギュレーション](https://groups.google.com/forum/#!topic/symfony-devs/nWddMcXLbh8)
  * [symfony 2 - 再利用可能なディストリビューション](https://groups.google.com/forum/#!topic/symfony-devs/1HyK24Zs0I8)
  * [API バージョニングのサポート](https://groups.google.com/forum/#!topic/symfony-devs/O2EClN1-Q-I)

symfony 1 開発ハイライト
------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=09%2F10%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r33121](http://trac.symfony-project.org/changeset/33121 "33121 revision on trac"): \[1.4\] fixed protocol relative URL in the asset helper
  * [r33122](http://trac.symfony-project.org/changeset/33122 "33122 revision on trac"): \[1.4\] fixed include|get_component when sfPartialView class is customized
  * [r33125](http://trac.symfony-project.org/changeset/33125 "33125 revision on trac"): \[1.4\] fixed the possibility to include files included in an exclude rule in the deploy task

sfDoctrinePlugin:

  * [r33123](http://trac.symfony-project.org/changeset/33123 "33123 revision on trac"): \[1.4\] fixed virtual columns in sfFormFilterDoctrine

Symfony2 開発ハイライト
-----------------------

[2.0 branch](http://github.com/symfony/symfony/commits/2.0):

  * [cf4a91e](http://github.com/symfony/symfony/commit/cf4a91e923c1192308311c390f42485d27721d10 "cf4a91e923c1192308311c390f42485d27721d10 commit on github"): \[ClassLoader\] fixed usage of trait_exists()
  * [92d1906](http://github.com/symfony/symfony/commit/92d19063a843c53537e49a3c74a052287b4792b2 "92d19063a843c53537e49a3c74a052287b4792b2 commit on github"): \[Translation\] changed some unit tests for PHPUnit 3.6.0 compatibility
  * [828b18f](http://github.com/symfony/symfony/commit/828b18f4673f09832be1692bd99bfe6de9112689 "828b18f4673f09832be1692bd99bfe6de9112689 commit on github"): \[Form\] fixed lacking attributes in DateTimeType
  * [a74ae9d](http://github.com/symfony/symfony/commit/a74ae9d325e23747e274448c69d688bcc2705d42 "a74ae9d325e23747e274448c69d688bcc2705d42 commit on github"): \[HttpFoundation\] made X_REWRITE_URL only available on Windows platforms
  * [95049ef](http://github.com/symfony/symfony/commit/95049ef902fa4818bb4c221dc2ed2d582e792cc9 "95049ef902fa4818bb4c221dc2ed2d582e792cc9 commit on github"): \[Form\] added type check to ScalarToChoiceTransformer
  * [18a83c6](http://github.com/symfony/symfony/commit/18a83c67f41c2052cb1037f629838371d2aea202 "18a83c67f41c2052cb1037f629838371d2aea202 commit on github"): \[Form\] simplified a bit FormUtil and extended test coverage
  * [ae0685a](http://github.com/symfony/symfony/commit/ae0685a3142a2c58866f6dcde4145258e673d0c1 "ae0685a3142a2c58866f6dcde4145258e673d0c1 commit on github"): \[Translation\] loader should only load local files

[Master branch](http://github.com/symfony/symfony/commits/master):

  * [6b16757](http://github.com/symfony/symfony/commit/6b16757199000a53d733d5568828e3f6e5b038ab "6b16757199000a53d733d5568828e3f6e5b038ab commit on github"): \[Security\] changed a RuntimeException to LogicException for consistencies between the different Token classes
  * [3f567b8](http://github.com/symfony/symfony/commit/3f567b82089e2bdeb6fb731231d398e416cc38a5 "3f567b82089e2bdeb6fb731231d398e416cc38a5 commit on github"): \[FrameworkBundle\] moved a parameter in the same file as the one where the service is defined for better consistency
  * [d7c9644](http://github.com/symfony/symfony/commit/d7c9644d291ff17b430912b67cc295dbf15200f2 "d7c9644d291ff17b430912b67cc295dbf15200f2 commit on github"): \[Validator\] extend and fix DateValidator & TimeValidator tests
  * [deb6dea](http://github.com/symfony/symfony/commit/deb6dea76dec7d38671afa5ff3f2c278ea28dd65 "deb6dea76dec7d38671afa5ff3f2c278ea28dd65 commit on github"): \[Translation\] added failing tests to verify that UTF-8 lang files can't be used with another charset
  * [5473d3b](http://github.com/symfony/symfony/commit/5473d3b6c94ac38d0658f9745c582f840d49464e "5473d3b6c94ac38d0658f9745c582f840d49464e commit on github"): \[Translation\] allowed use of UTF-8 encoded catalogues into non-UTF-8 applications
  * [395f580](http://github.com/symfony/symfony/commit/395f580fd7e9fd49ba850198da0c333bc6d28d3b "395f580fd7e9fd49ba850198da0c333bc6d28d3b commit on github"): rebuilt resource files with genrb from ICU 4.2. as ICU 4.4 by default builds them in newer format
  * [8b55541](http://github.com/symfony/symfony/commit/8b55541aeefc78366daa0296fc67151edd1977c9 "8b55541aeefc78366daa0296fc67151edd1977c9 commit on github"): added an UPGRADE file
  * [74bc699](http://github.com/symfony/symfony/commit/74bc699b270122b70b1de6ece47c726f5df8bd41 "74bc699b270122b70b1de6ece47c726f5df8bd41 commit on github"): [BC BREAK] moved management of the locale from the Session class to the Request class


  
