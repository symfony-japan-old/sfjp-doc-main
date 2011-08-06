A week of symfony #238 (18->24 July 2011)
=========================================

今週のSymfony2は2つのリリース候補版をリリースしました。これらのリリースには前回のバージョンから数えて数百ものコミットを含んでいます。加えて、最終的なSymfony 2.0安定版のリリース日が[7/28(木)とアナウンスされました](http://symfony.com/blog/symfony2-the-roadmap-to-final)
 
開発メーリングリスト
------------------------

  * [Entity内またはTwigエクステンションの中からどうやってEntityManagerを取得するか](https://groups.google.com/forum/#!topic/symfony-devs/37T1LP4EOqY)
  * [Symfony2のオブジェクトルート(Route)](https://groups.google.com/forum/#!topic/symfony-devs/tWhstbQDe5k)

symfony 1 開発ハイライト
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=24%2F07%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r32807](http://trac.symfony-project.org/changeset/32807 "32807 revision on trac"), [r32808](http://trac.symfony-project.org/changeset/32808 "32808 revision on trac"): \[1.4\] choice widgetsの為にparentを修正

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [872d308](http://github.com/symfony/symfony/commit/872d308e9c7f8cd60e3857ac277cbc4a898ec959 "872d308e9c7f8cd60e3857ac277cbc4a898ec959 commit on github"): \[DoctrineBundle\] allowed to configure dql functions without using the multiple entity mangers syntax
  * [bb452cd](http://github.com/symfony/symfony/commit/bb452cd7c4e45acc2267645925bb818204b3e5e3 "bb452cd7c4e45acc2267645925bb818204b3e5e3 commit on github"): \[Form\] renamed invalid_message_template to invalid_message to be consistent with other error message names
  * [8fc9547](http://github.com/symfony/symfony/commit/8fc9547da5a5607e8a1a38a2c9d100d836937062 "8fc9547da5a5607e8a1a38a2c9d100d836937062 commit on github"): \[FrameworkBundle\] fixed session support in functional tests when using several clients in the same process
  * [e2eb601](http://github.com/symfony/symfony/commit/e2eb601ebded411fa08b1990959411c3786343ea "e2eb601ebded411fa08b1990959411c3786343ea commit on github"): \[FrameworkBundle\] fixed absolute paths to the cache directory after running cache:clear
  * [f6c5ef7](http://github.com/symfony/symfony/commit/f6c5ef7b741e9d86a03a46d28ea098ca8874d45d "f6c5ef7b741e9d86a03a46d28ea098ca8874d45d commit on github"), [c3a060e](http://github.com/symfony/symfony/commit/c3a060e36874034229beb0d1115074cab326f1ec "c3a060e36874034229beb0d1115074cab326f1ec commit on github"): \[DependencyInjection\] added processConfiguration convenience method
  * [5d17b92](http://github.com/symfony/symfony/commit/5d17b9207cc53dc353b36cd1ba3520492e56483e "5d17b9207cc53dc353b36cd1ba3520492e56483e commit on github"): \[DoctrineBridge\] optimized the mapping drivers
  * [95011ce](http://github.com/symfony/symfony/commit/95011ce4b7e85bc62529277ea4dfee1d91494b96 "95011ce4b7e85bc62529277ea4dfee1d91494b96 commit on github"): \[HttpFoundation\] fixed creation of requests without a path
  * [1454d61](http://github.com/symfony/symfony/commit/1454d61ad5c1520d11ce154d143cdd3b258c27fe "1454d61ad5c1520d11ce154d143cdd3b258c27fe commit on github"), [dafa4d2](http://github.com/symfony/symfony/commit/dafa4d28d60b3d0845892f0d8c73e938d5fa6085 "dafa4d28d60b3d0845892f0d8c73e938d5fa6085 commit on github"): \[FrameworkBundle\] made a huge speed optimization for functional tests
  * [9e7cb0a](http://github.com/symfony/symfony/commit/9e7cb0a020e15564e56fa2442a8ad5a181f8456f "9e7cb0a020e15564e56fa2442a8ad5a181f8456f commit on github"): \[Routing\] fixed default value for Routes as they can be anything if they don't need to be used as default values for placeholders
  * [d3a69e3](http://github.com/symfony/symfony/commit/d3a69e353116ba0c5d4e9f413646da57eafcd346 "d3a69e353116ba0c5d4e9f413646da57eafcd346 commit on github"): \[DoctrineBundle\] renamed RegistryInterface::getEntityManagerForObject() to getEntityManagerForClass()
  * [7dcbcbe](http://github.com/symfony/symfony/commit/7dcbcbe69d7a63b425176ee4ee2681ffcb3bf7d9 "7dcbcbe69d7a63b425176ee4ee2681ffcb3bf7d9 commit on github"), [7720cb9](http://github.com/symfony/symfony/commit/7720cb9be489d615ff4f07e0657ba71e90a18d8c "7720cb9be489d615ff4f07e0657ba71e90a18d8c commit on github"), [5c06b3c](http://github.com/symfony/symfony/commit/5c06b3cfeba356d88b2a0c2d5ab436b655626af9 "5c06b3cfeba356d88b2a0c2d5ab436b655626af9 commit on github"), [b36c002](http://github.com/symfony/symfony/commit/b36c002fa489203ea8756fff754bbcfa9054bf2c "b36c002fa489203ea8756fff754bbcfa9054bf2c commit on github"), [97cb35b](http://github.com/symfony/symfony/commit/97cb35b47a4e9a5aed55937449d46f881f6f6f99 "97cb35b47a4e9a5aed55937449d46f881f6f6f99 commit on github"): tagged public @api for HttpFoundation, HttpKernel, Templating, Validator, DependencyInjection
  * [8333df6](http://github.com/symfony/symfony/commit/8333df6161094b90c622077a1e229431342d365f "8333df6161094b90c622077a1e229431342d365f commit on github"): fixed autoloader when tests are run without intl installed
  * [e5fa78a](http://github.com/symfony/symfony/commit/e5fa78af31d0e8e113f6b7e48ea41300175d3d5d "e5fa78af31d0e8e113f6b7e48ea41300175d3d5d commit on github"), [e42a2de](http://github.com/symfony/symfony/commit/e42a2dede1056aad22ace9c1f4737ab659035fa0 "e42a2dede1056aad22ace9c1f4737ab659035fa0 commit on github"): fixed Form and Validator unit tests when intl is not installed
  * [3a285c1](http://github.com/symfony/symfony/commit/3a285c15480cecbdc5d48af0e8abb96ad4646f54 "3a285c15480cecbdc5d48af0e8abb96ad4646f54 commit on github"): \[HttpKernel\] fixed handling of null-values in attribute- and query-arrays (when esi is enabled and internal uris are generated for esi-tags, an attribute-array consisting entirely of null-values isn't handled correctly)
  * [0327beb](http://github.com/symfony/symfony/commit/0327beb0b9bb1394e93845fc244c5b67c3f1b520 "0327beb0b9bb1394e93845fc244c5b67c3f1b520 commit on github"): \[Form\] added ObjectFactoryListener
  * [3749ad4](http://github.com/symfony/symfony/commit/3749ad43f48fbe718a1999ecd3e54d7803e4f11d "3749ad43f48fbe718a1999ecd3e54d7803e4f11d commit on github"): moved the Exception listener from FrameworkBundle to TwigBundle as it relies on Twig being enabled
  * [7062cc2](http://github.com/symfony/symfony/commit/7062cc2db5f1de5ab4677041fe287d5d3d4383da "7062cc2db5f1de5ab4677041fe287d5d3d4383da commit on github"), [ccda267](http://github.com/symfony/symfony/commit/ccda267c3654fbc571be5b6edbd26b05a304f99a "ccda267c3654fbc571be5b6edbd26b05a304f99a commit on github"), [e776d5d](http://github.com/symfony/symfony/commit/e776d5dbce0a333464abab7789a606867170f8b4 "e776d5dbce0a333464abab7789a606867170f8b4 commit on github"), [6b0a9ff](http://github.com/symfony/symfony/commit/6b0a9ff7842acb92767ec367d4cc750dc1cc5437 "6b0a9ff7842acb92767ec367d4cc750dc1cc5437 commit on github"): fixed compiled classes and tweaked compiled class cache
  * [cede13e](http://github.com/symfony/symfony/commit/cede13e8cc0f58a64bff70e315cf8220b09d9457 "cede13e8cc0f58a64bff70e315cf8220b09d9457 commit on github"): \[FrameworkBundle\] moved the SessionListener to the session.xml configuration file
  * [84abbbd](http://github.com/symfony/symfony/commit/84abbbd6dfd048ccc1c43a1f803148f74ea8c6ca "84abbbd6dfd048ccc1c43a1f803148f74ea8c6ca commit on github"): \[HttpKernel\] enhanced the ExceptionHandler so that it can be used in prod environment too (mainly useful for Silex)
  * [2b4cc9b](http://github.com/symfony/symfony/commit/2b4cc9bd06c100066b5402f134a65e9a840bbc81 "2b4cc9bd06c100066b5402f134a65e9a840bbc81 commit on github"): \[Form\] changed collection prototype rendering
  * [c6115ce](http://github.com/symfony/symfony/commit/c6115cee7fa4fbd56dae1b5f3a8f417a04bc3dc9 "c6115cee7fa4fbd56dae1b5f3a8f417a04bc3dc9 commit on github"): \[BrowserKit\] changed Cookie::fromString() to not take the secure setting into account if the URL is not present or is not HTTPS
  * [cc07af2](http://github.com/symfony/symfony/commit/cc07af2449ef4d976790b10b72451e7fced46108 "cc07af2449ef4d976790b10b72451e7fced46108 commit on github"): \[ClassLoader\] replaced MapFileClassLoader by MapClassLoader
  * [e16c226](http://github.com/symfony/symfony/commit/e16c226a5c4109c748fdfbac690b0fae7a1e7757 "e16c226a5c4109c748fdfbac690b0fae7a1e7757 commit on github"): \[HttpKernel\] changed the way compiled classes are managed to be sure that they are included before the Kernel is booted
  * [eb7c86b](http://github.com/symfony/symfony/commit/eb7c86b7a812f152b16b27f2abe95e9e43af1363 "eb7c86b7a812f152b16b27f2abe95e9e43af1363 commit on github"): \[HttpKernel\] removed the need to keep the compiled classes in the container


