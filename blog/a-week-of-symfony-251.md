---
layout: default
title: A week of symfony #251 (17->23 October 2011)
---

A week of symfony #251 (17->23 October 2011)
============================================

先週、Symfony2 にはコードのプロファイリングを行うための [ストップウォッチ](https://github.com/symfony/symfony/commit/106ebdbe184b0cd9ff8f3a12232cf242b0696f58) が追加されました。
また、このストップウォッチの機能を使い、Web プロファイラーに [タイムラインパネル](https://github.com/symfony/symfony/commit/842ac36f339a65e3e31fd345a01ba4002a7430ae) が追加されました。
これらの新機能は、[Symfony Day 2011](http://www.symfonyday.com/en/) カンファレンスで発表されました。
 
開発メーリングリスト
--------------------

  * [Doctrine2 Inheritance](https://groups.google.com/forum/#!topic/symfony-devs/kJwLcRhrtmM)
  * [Chain an additional display function in Twig](https://groups.google.com/forum/#!topic/symfony-devs/GrYkFF7eo9s)

Symfony2 開発ハイライト
-----------------------

[master ブランチ](http://github.com/symfony/symfony/commits/master):

  * [97d6591](http://github.com/symfony/symfony/commit/97d6591985cb1c427b55cabb15664a882c55f532 "97d6591985cb1c427b55cabb15664a882c55f532 commit on github"): \[WebProfilerBundle\] tweaked the default layout to make more room for interesting content
  * [347053c](http://github.com/symfony/symfony/commit/347053c363aac66e79e91a3c0a205e417521c153 "347053c363aac66e79e91a3c0a205e417521c153 commit on github"): moved most of the logic from ResponseListener to the Response::prepare() method (this allows projects that only use HttpFoundation and not HttpKernel to be able to enforce the HTTP specification rules)
  * [312b20f](http://github.com/symfony/symfony/commit/312b20f94b5a2fed200908c5d41eb97917a8ba52 "312b20f94b5a2fed200908c5d41eb97917a8ba52 commit on github"): \[FrameworkBundle\] added more info to debug command output
  * [fbc422b](http://github.com/symfony/symfony/commit/fbc422b978cc2b5840c3452d21e62b1044f6e03d "fbc422b978cc2b5840c3452d21e62b1044f6e03d commit on github"): \[BrowserKit\] added the standard output when an error occurs during the request execution
  * [106ebdb](http://github.com/symfony/symfony/commit/106ebdbe184b0cd9ff8f3a12232cf242b0696f58 "106ebdbe184b0cd9ff8f3a12232cf242b0696f58 commit on github"): \[HttpKernel\] added a Stopwatch
  * [842ac36](http://github.com/symfony/symfony/commit/842ac36f339a65e3e31fd345a01ba4002a7430ae "842ac36f339a65e3e31fd345a01ba4002a7430ae commit on github"): added Stopwatch support in debug mode, added a timeline representing the stopwatch events in the web profiler
  * [c5ca40c](http://github.com/symfony/symfony/commit/c5ca40c711511c245039c4a4cafb204c4ccd46bf "c5ca40c711511c245039c4a4cafb204c4ccd46bf commit on github"): \[Routing\] added support for _scheme requirement in UrlMatcher
  * [46a69f1](http://github.com/symfony/symfony/commit/46a69f1ca004f712d39478d9c23076e03b781e88 "46a69f1ca004f712d39478d9c23076e03b781e88 commit on github"), [ad7fcf5](http://github.com/symfony/symfony/commit/ad7fcf5206cc4f1f98effcb4feaf1cc18c8f23f2 "ad7fcf5206cc4f1f98effcb4feaf1cc18c8f23f2 commit on github"): define a WarmableInterface and only warm the cache if it implements warmable to allow replacing the core router
  * [3134ef1](http://github.com/symfony/symfony/commit/3134ef132a00267a6aded6f3b0075ec2d40e51e0 "3134ef132a00267a6aded6f3b0075ec2d40e51e0 commit on github"): \[HttpKernel\] removed usage of assertCount which has been introduced in PHPUnit 3.6
  * [2e1344e](http://github.com/symfony/symfony/commit/2e1344eb7ef1e4a6c5cc21e098fd2a6404f2b289 "2e1344eb7ef1e4a6c5cc21e098fd2a6404f2b289 commit on github"): \[Routing\] added the possibility to define default values and requirements for placeholders in prefix

[2.0 ブランチ](http://github.com/symfony/symfony/commits/2.0):

  * [e81c710](http://github.com/symfony/symfony/commit/e81c71078464d32a4537cc8dcbec6db29d44c447 "e81c71078464d32a4537cc8dcbec6db29d44c447 commit on github"), [1a43505](http://github.com/symfony/symfony/commit/1a43505a3e690394bef2ecdf75c5ce194f687a7e "1a43505a3e690394bef2ecdf75c5ce194f687a7e commit on github"): \[FrameworkBundle\] increased the priority of the profiler request listener
  * [HttpKer](http://github.com/symfony/symfony/commit/HttpKernel "HttpKernel commit on github"): check if cache_warmer service is available before doing the actual cache warmup


