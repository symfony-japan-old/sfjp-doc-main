---
layout: default
title: A week of symfony #261 (26 December 2011 -> 1 January 2012)
---

A week of symfony #261 (26 December 2011 -> 1 January 2012)
===========================================================

2011年の最後の週には、[Symfony 2.0.8](http://symfony.com/blog/symfony-2-0-8-released) がリリースされ、次期バージョンである Symfony 2.1 で [ストリームレスポンス](https://github.com/symfony/symfony/commit/0038d1bac4a8d2dbe83f12b6a5236e8a2161b7d9) が追加されることなどがアナウンスされました。

開発メーリングリスト
--------------------

  * [コントローラ、テンプレート、リポジトリの相対パス](https://groups.google.com/forum/#!topic/symfony-devs/WXHy-rsfqSA)
  * [DoctrineCache](https://groups.google.com/forum/#!topic/symfony-devs/F1EeutjYA0A)

Symfony2 開発ハイライト
-----------------------

[2.0 ブランチ](http://github.com/symfony/symfony/commits/2.0):

  * [e5c44e2](http://github.com/symfony/symfony/commit/e5c44e261e06d97068fee0fd961ad4994e000dfd "e5c44e261e06d97068fee0fd961ad4994e000dfd commit on github"), [6aee905](http://github.com/symfony/symfony/commit/6aee905588d1df0743dfee6025fddc30de970014 "6aee905588d1df0743dfee6025fddc30de970014 commit on github"), [5b4e619](http://github.com/symfony/symfony/commit/5b4e6190c4420524e4dcaf51213c4ad78f646528 "5b4e6190c4420524e4dcaf51213c4ad78f646528 commit on github"): released 2.0.8 version
  * [eb2d6e6](http://github.com/symfony/symfony/commit/eb2d6e6f2fb90d8c5b276a79617f197758e37e62 "eb2d6e6f2fb90d8c5b276a79617f197758e37e62 commit on github"): \[FrameworkBundle\] updated Spanish translations for validators
  * [c92d75f](http://github.com/symfony/symfony/commit/c92d75f6ddfa09db50cac8018ddb7e8041a5a0a5 "c92d75f6ddfa09db50cac8018ddb7e8041a5a0a5 commit on github"), [f458e96](http://github.com/symfony/symfony/commit/f458e96f934c9d8c57040d3f55448d207c7bc21b "f458e96f934c9d8c57040d3f55448d207c7bc21b commit on github"): \[TwigBridge\] changed composer.json max version for Twig
  * [85ca8e3](http://github.com/symfony/symfony/commit/85ca8e3615be14b784cd499c7f17f61d5594df05 "85ca8e3615be14b784cd499c7f17f61d5594df05 commit on github"), [99011ca](http://github.com/symfony/symfony/commit/99011ca9c9b0eb6f55f5a9fe679a647b158d3ed1 "99011ca9c9b0eb6f55f5a9fe679a647b158d3ed1 commit on github"): \[DependencyInjection\] ParameterBag no longer resolves parameters that have spaces (They must be strictly "%some.parameter%" or similar)
  * [ced57d8](http://github.com/symfony/symfony/commit/ced57d8ee5d6844312d7ec71760e88bf2c8b9d89 "ced57d8ee5d6844312d7ec71760e88bf2c8b9d89 commit on github"): \[Form\] reverse transform doesn't take a second argument


[master ブランチ](http://github.com/symfony/symfony/commits/master):

  * [de9d7d8](http://github.com/symfony/symfony/commit/de9d7d8c3c509c394985f923c07ffed34e7c9dd6 "de9d7d8c3c509c394985f923c07ffed34e7c9dd6 commit on github"): \[FrameworkBundle\] updated Italian translations for validators
  * [eef8a3c](http://github.com/symfony/symfony/commit/eef8a3c5135907a1f5c049c02d55462c85a5d53d "eef8a3c5135907a1f5c049c02d55462c85a5d53d commit on github"): \[FrameworkBundle\] changed the implementation of Controller::getUser() to be similar to the one from GlobalVariables::getUser()
  * [d12f5b2](http://github.com/symfony/symfony/commit/d12f5b202c38a67c800339425be2059e4fec3c75 "d12f5b202c38a67c800339425be2059e4fec3c75 commit on github"): \[Routing\] removed trailing slash support for routes that are not available for GET/HEAD methods (as the redirection will always occurs with a GET/HEAD request)
  * [0038d1b](http://github.com/symfony/symfony/commit/0038d1bac4a8d2dbe83f12b6a5236e8a2161b7d9 "0038d1bac4a8d2dbe83f12b6a5236e8a2161b7d9 commit on github"), [e44b8ba](http://github.com/symfony/symfony/commit/e44b8ba521e60f4b0c8218a65415c001090520da "e44b8ba521e60f4b0c8218a65415c001090520da commit on github"): \[HttpFoundation\] added support for streamed responses
  * [473741b](http://github.com/symfony/symfony/commit/473741b9db7a2868c19033ff62963fd1b37ea29e "473741b9db7a2868c19033ff62963fd1b37ea29e commit on github"): added the possibility to change a StreamedResponse callback after its creation
  * [887c0e9](http://github.com/symfony/symfony/commit/887c0e9c04af4219ce5d4aa536e2e797614e94d2 "887c0e9c04af4219ce5d4aa536e2e797614e94d2 commit on github"): moved EngineInterface::stream() to a new StreamingEngineInterface to keep BC with 2.0
  * [3ef0594](http://github.com/symfony/symfony/commit/3ef0594e7413c721f41b53f4b834a03cc44e9f03 "3ef0594e7413c721f41b53f4b834a03cc44e9f03 commit on github"): \[HttpKernel\] fixed missing $method argument in MongoDbProfilerStorageTest
  * [e462f7b](http://github.com/symfony/symfony/commit/e462f7b668f2af150a47ccd453767d9853884558 "e462f7b668f2af150a47ccd453767d9853884558 commit on github"): \[Templating\] simplified PhpEngine as it cannot implements the streaming interface
  * [3d5ecc0](http://github.com/symfony/symfony/commit/3d5ecc0478b89aacba655d3fbe89604e187848dd "3d5ecc0478b89aacba655d3fbe89604e187848dd commit on github"): \[HttpKernel\] added the path info in the request data collector
  * [b46114a](http://github.com/symfony/symfony/commit/b46114a0f67da3338aa6728f33d20fb11c4da59c "b46114a0f67da3338aa6728f33d20fb11c4da59c commit on github"): \[WebProfilerBundle\] moved the computation of the Router panel at runtime
  * [66a18f3](http://github.com/symfony/symfony/commit/66a18f3239f7c0679c503018efbf98c5848afdcc "66a18f3239f7c0679c503018efbf98c5848afdcc commit on github"): \[BrowserKit\] first attempt at fixing CookieJar


