---
layout: default
title: A week of symfony #252 (24->30 October 2011)
---

A week of symfony #252 (24->30 October 2011)
============================================

先週、Symfony 1.4.15 がリリースされました。
symfony 1.4.15 では幾つかのバグ修正が行われています。
1.4.x ブランチのサポートが 2012 年末まで続けられるということの証でもあります。
一方、Symfony2 にはルーティングのデバッグを行いやすくするための [マッチャー](https://github.com/symfony/symfony/commit/24b93928bf783290c0df193f1b9948a174b01d1b) と [コマンド](https://github.com/symfony/symfony/commit/8cc3158d8901b8aefadde7f24be92fd9ed2b07e7) が追加されました。
 
開発メーリングリスト
--------------------

  * [getRouter() instead of get('router')](https://groups.google.com/forum/#!topic/symfony-devs/HcWILuuvZ3U)
  * [Official AdminGenerator?](https://groups.google.com/forum/#!topic/symfony-devs/HMmMSQPGMZg)
  * [Making Symfony 2.0 forwards compatible](https://groups.google.com/forum/#!topic/symfony-devs/CibR6gKmRug)

symfony 1 開発ハイライト
------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=30%2F10%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r33151](http://trac.symfony-project.org/changeset/33151 "33151 revision on trac"): \[1.4\] fixed usage of mb_strlen in tasks
  * [Milestone 1.4.15 completed](http://trac.symfony-project.org/milestone/1.4.15)

sfDoctrinePlugin:

  * [r33149](http://trac.symfony-project.org/changeset/33149 "33149 revision on trac"): \[1.4\] added missing admin.delete_object event


Symfony2 開発ハイライト
-----------------------

[2.0 ブランチ](http://github.com/symfony/symfony/commits/master):

  * [cbb4bba](http://github.com/symfony/symfony/commit/cbb4bbae977eb7e0651b9963cbef84fa75349c3d "cbb4bbae977eb7e0651b9963cbef84fa75349c3d commit on github"): \[Routing\] fixed side-effect in the PHP matcher dumper
  * [808088a](http://github.com/symfony/symfony/commit/808088a3ca607bf62f6c70ef7d3a3066f0cfac98 "808088a3ca607bf62f6c70ef7d3a3066f0cfac98 commit on github"): added the ability to use dot and single quotes in the keys and values
  * [27d0809](http://github.com/symfony/symfony/commit/27d080984ca8f972241cd3e38f0181d1a8722e93 "27d080984ca8f972241cd3e38f0181d1a8722e93 commit on github"), [e314931](http://github.com/symfony/symfony/commit/e3149318f522c14717041db3ff6b7e64421ce033 "e3149318f522c14717041db3ff6b7e64421ce033 commit on github"): updated Monolog to 1.0.2
  * [6343bef](http://github.com/symfony/symfony/commit/6343bef55e8f0cee33ef185081f128deb3c06656 "6343bef55e8f0cee33ef185081f128deb3c06656 commit on github"): \[HttpKernel\] updated mirror method to check for symlinks before dirs and files
  * [8dcde3c](http://github.com/symfony/symfony/commit/8dcde3c076b5c485dd133466bf20c45e53227dca "8dcde3c076b5c485dd133466bf20c45e53227dca commit on github"): \[DependencyInjection\] fixed int casting for XML files (based on what is done in the YAML component)
  * [4bbb685](http://github.com/symfony/symfony/commit/4bbb685557c9aebc54d6ee6fb268941695cde4f4 "4bbb685557c9aebc54d6ee6fb268941695cde4f4 commit on github"): \[DependencyInjection\] added tests for Definition and DefinitionDecorator exceptions
  * [80f0b98](http://github.com/symfony/symfony/commit/80f0b980baa4dbbd9a4f1dd2f75c7a6e0bbcb0bc "80f0b980baa4dbbd9a4f1dd2f75c7a6e0bbcb0bc commit on github"): \[DependencyInjection\] fixed DefinitionDecorator::getArgument() for replacements
  * [851eb73](http://github.com/symfony/symfony/commit/851eb737784b06619485c844882e98c800a8f7fb "851eb737784b06619485c844882e98c800a8f7fb commit on github"): removed a ton of unused use statements

[master ブランチ](http://github.com/symfony/symfony/commits/master):

  * [24b9392](http://github.com/symfony/symfony/commit/24b93928bf783290c0df193f1b9948a174b01d1b "24b93928bf783290c0df193f1b9948a174b01d1b commit on github"), [8cc3158](http://github.com/symfony/symfony/commit/8cc3158d8901b8aefadde7f24be92fd9ed2b07e7 "8cc3158d8901b8aefadde7f24be92fd9ed2b07e7 commit on github"): \[Routing, FrameworkBundle\] added a matcher and a command that help debugging matching problems
  * [8fa061c](http://github.com/symfony/symfony/commit/8fa061cc6e6635d403cca9b98e934a3b4021b892 "8fa061cc6e6635d403cca9b98e934a3b4021b892 commit on github"): \[WebProfilerBundle\] added a profiler panel for the router
  * [70e0dba](http://github.com/symfony/symfony/commit/70e0dba77c0f30154477b4f603be8ff336cf2192 "70e0dba77c0f30154477b4f603be8ff336cf2192 commit on github"): moved the Swiftmailer data collector to the Swifmailer bridge
  * [9077f6a](http://github.com/symfony/symfony/commit/9077f6a9711730559fe6e8432358c1c8b00a5ca7 "9077f6a9711730559fe6e8432358c1c8b00a5ca7 commit on github"): \[SwiftmailerBundle\] replaced MessageLogger class with the one from Swiftmailer 4.1.3
  * [95ec41b](http://github.com/symfony/symfony/commit/95ec41b075fcff99d0dee0769a7ec688bdd7a420 "95ec41b075fcff99d0dee0769a7ec688bdd7a420 commit on github"): \[Console\] made the defaults in Application more easily customizable
  * [f8065d1](http://github.com/symfony/symfony/commit/f8065d180574703dee6a7b114dbf7524ecc7408e "f8065d180574703dee6a7b114dbf7524ecc7408e commit on github"): \[HttpKernel\] added a way to get the original values returned by the router
  * [c2fa73d](http://github.com/symfony/symfony/commit/c2fa73d33aa0a07e8fba0ce49e1de4b16fd53d61 "c2fa73d33aa0a07e8fba0ce49e1de4b16fd53d61 commit on github"): \[HttpKernel\] removed the _route entry from _route_params


