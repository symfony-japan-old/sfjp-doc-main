A week of symfony #255 (14->20 November 2011)
=============================================

先週、重要なセキュリティフィックスが含まれる [Symfony 2.0.6 がリリースされました](http://symfony.com/blog/security-release-symfony-2-0-6)。
一方、[公式 Symfony コミュニティ](https://connect.sensiolabs.com/)は最初の1週間でメンバーの数が 1000 を越え、さまざまな改善も行われました。
 
開発メーリングリスト
--------------------

  * [Monolog swiftmailer handler configuration](https://groups.google.com/forum/#!topic/symfony-devs/IZ4a_-Oyt2c)
  * [\[RFC\] Symfony2 CI server](https://groups.google.com/forum/#!topic/symfony-devs/cjlktnXGmN0)
  * [LTS release](https://groups.google.com/forum/#!topic/symfony-devs/bp2QyeKRQR8)

symfony 1 開発ハイライト
------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=20%2F11%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r33208](http://trac.symfony-project.org/changeset/33208 "33208 revision on trac"): \[1.4\] fixed ob_start usage (to avoid warning in PHP 5.4)
  * [r33214](http://trac.symfony-project.org/changeset/33214 "33214 revision on trac"): \[1.4\] fixed ob_start() behavior on CLI

Symfony2 開発ハイライト
-----------------------

[2.0 ブランチ](http://github.com/symfony/symfony/commits/master):

  * [0462a89](http://github.com/symfony/symfony/commit/0462a895620bee27053c7b2444f7a31fed69db9b "0462a895620bee27053c7b2444f7a31fed69db9b commit on github"): \[Security\] fixed HttpUtils::checkRequestPath() to not catch all exceptions
  * [d67fbe9](http://github.com/symfony/symfony/commit/d67fbe9e48b90c29c7e0d3ce19e5d1ef643ace7a "d67fbe9e48b90c29c7e0d3ce19e5d1ef643ace7a commit on github"): \[HttpFoundation\] added an exception to MimeTypeGuesser::guess() when no guesser are available
  * [f7c5bf1](http://github.com/symfony/symfony/commit/f7c5bf1db2d18dfb480ac4dc1e6b1be160952edf "f7c5bf1db2d18dfb480ac4dc1e6b1be160952edf commit on github"): \[HttpKernel\] fixed Content-Length header when using ESI tags
  * [86a8b9f](http://github.com/symfony/symfony/commit/86a8b9f567d8d30a1c629c46a6a8950944d2a4bb "86a8b9f567d8d30a1c629c46a6a8950944d2a4bb commit on github"): allow vendors checkout transport method to be overridden manually (http, https, git)
  * [79ae3fc](http://github.com/symfony/symfony/commit/79ae3fced982331aa89885289b942a5961646846 "79ae3fced982331aa89885289b942a5961646846 commit on github"): \[Form\] fixed radio and checkbox when data is not bool

[master ブランチ](http://github.com/symfony/symfony/commits/master):

  * [6d7e6a8](http://github.com/symfony/symfony/commit/6d7e6a87a8eb76b8a18de42bd04eed5e0d1be9f7 "6d7e6a87a8eb76b8a18de42bd04eed5e0d1be9f7 commit on github"): \[DoctrineBundle\] enhanced error reporting during mapping validation when nested exceptions occur
  * [62fb019](http://github.com/symfony/symfony/commit/62fb019c6283ee0510f34ea188159cdb83fee47b "62fb019c6283ee0510f34ea188159cdb83fee47b commit on github"): added event priorities in the profiler
  * [43e6c36](http://github.com/symfony/symfony/commit/43e6c3690908ba59c9a7eb9bee5cdd62b60dff19 "43e6c3690908ba59c9a7eb9bee5cdd62b60dff19 commit on github"): \[FrameworkBundle\] changed the session listeners to be subscribers
  * [264a033](http://github.com/symfony/symfony/commit/264a033728e6063bb19702463e3c3c0989d924fd "264a033728e6063bb19702463e3c3c0989d924fd commit on github"): fixed uncompatible closure declaraction in FileldTypeValidatorExtensionTest
  * [e3655f3](http://github.com/symfony/symfony/commit/e3655f3a5ccfdf866d4cd629c283203330516d67 "e3655f3a5ccfdf866d4cd629c283203330516d67 commit on github"): changed priorities for kernel.request listeners (the Firewall is now executed after the Router)
  * [5e4b7cb](http://github.com/symfony/symfony/commit/5e4b7cb1ba06445dd5370d861caeb5cc5eacf912 "5e4b7cb1ba06445dd5370d861caeb5cc5eacf912 commit on github"): renamed Propel Bridge from Propel to Propel1

