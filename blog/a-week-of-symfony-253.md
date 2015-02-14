---
layout: default
title: A week of symfony #253 (31 October -> 6 November 2011)
---

A week of symfony #253 (31 October -> 6 November 2011)
======================================================

先週、[Symfony 2.0.5 がリリースされました](http://symfony.com/blog/symfony-2-0-5-released)。
Symfony 2.0.5では、さまざまなバグフィックスやいくつかの機能改善が行われています([changelog](https://github.com/symfony/symfony/blob/2.0/CHANGELOG-2.0.md))。
一方、[前回の週次 IRC ミーティング](https://groups.google.com/forum/#!topic/symfony-devs/MDi_Yw-7cIY)では、Symfony2コンポーネントに関して、ドキュメントの充実を含む今後の方針などが議論されました。
 
開発メーリングリスト
--------------------

  * [Sonata Admin Bundle Split](https://groups.google.com/forum/#!topic/symfony-devs/15xCDUR9tGs)
  * [Week #44 IRC meeting](https://groups.google.com/forum/#!topic/symfony-devs/MDi_Yw-7cIY)
  * [ACL/Pager concerns](https://groups.google.com/forum/#!topic/symfony-devs/7g75BvgukPA)
  * [Symfony2 + Smarty](https://groups.google.com/forum/#!topic/symfony-devs/fQ78BPyr30E)

Symfony2 開発ハイライト
-----------------------

[2.0 ブランチ](http://github.com/symfony/symfony/commits/2.0):

  * [c9d05d7](http://github.com/symfony/symfony/commit/c9d05d72365aa2e20e17e3322b82d7a75f542b88 "c9d05d72365aa2e20e17e3322b82d7a75f542b88 commit on github"): let NumberFormatter handle integer type casting
  * [89cd64a](http://github.com/symfony/symfony/commit/89cd64a4a512009d11b027014fcb56e0a8fad104 "89cd64a4a512009d11b027014fcb56e0a8fad104 commit on github"): set error code when number cannot be parsed
  * [c5e2def](http://github.com/symfony/symfony/commit/c5e2defe5f6019bdd24ffa4ccb73b78afac90e47 "c5e2defe5f6019bdd24ffa4ccb73b78afac90e47 commit on github"): fixed ternary operator usage in RequestMatcher::checkIpv6()
  * [af6f0d5](http://github.com/symfony/symfony/commit/af6f0d55489e8cff5d9b753bf5e9e67f4657461e "af6f0d55489e8cff5d9b753bf5e9e67f4657461e commit on github"): \[Form\] removed some incomplete unit tests, added some new ones
  * [dbba796](http://github.com/symfony/symfony/commit/dbba79651ab8109c1337967a457d94966f76ee74 "dbba79651ab8109c1337967a457d94966f76ee74 commit on github"): \[Yaml\] fixed dumper for floats when the locale separator is not a dot


[master ブランチ](http://github.com/symfony/symfony/commits/master):

  * [cbd0c3c](http://github.com/symfony/symfony/commit/cbd0c3c8e98c55299066711f6a642cfe2e87dd23 "cbd0c3c8e98c55299066711f6a642cfe2e87dd23 commit on github"): \[Config\] implemented Serializable on resources
  * [d7a5351](http://github.com/symfony/symfony/commit/d7a5351aaa9a8f523b0ec90eb87a32115a0ddcf1 "d7a5351aaa9a8f523b0ec90eb87a32115a0ddcf1 commit on github"), [fc97472](http://github.com/symfony/symfony/commit/fc97472f64cd5494f1ec481cec762817cf638464 "fc97472f64cd5494f1ec481cec762817cf638464 commit on github"): updated composer.json files to contain information about autoloading and target dirs
  * [05a4e9d](http://github.com/symfony/symfony/commit/05a4e9d3861e0a561401ea495f95ee561ee81bfb "05a4e9d3861e0a561401ea495f95ee561ee81bfb commit on github"): \[Validators\] added support for ctype_* functions + tests
  * [149bdb9](http://github.com/symfony/symfony/commit/149bdb962b97e72fd788adf3c3008c3cc2320933 "149bdb962b97e72fd788adf3c3008c3cc2320933 commit on github"): enhanced error messages with regard to form type properties

