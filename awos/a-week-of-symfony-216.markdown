---
layout: default
title: "A week of symfony #216 (14->20 February 2011)"
---

A week of symfony #216 (14->20 February 2011)
=============================================

Symfony2 frantic development activity included this week some massive commits such as [adding support for merging security configurations](https://github.com/symfony/symfony/commit/0b8fef234724cb4cb3a4ab37466efe193a6c7708), [implementing single-pass config loading with intelligent merging](https://github.com/symfony/symfony/commit/f9138d313b83f951cf82a2f7f902a2d6dd14fbb3) and [moving common configuration classes to a new Config component](https://github.com/symfony/symfony/commit/5c905beb13624d40a768e6e9ea98cb873e149c6e).
In addition, the new [AsseticBundle was integrated](https://github.com/symfony/symfony/commit/12929257021741a9d0c0d4b0c2d05836208cb324) in Symfony2, allowing a much more powerful and flexible way to handle web assets.
Lastly, [1.3.9 and 1.4.9 maintenance versions were released](http://www.symfony-project.org/blog/2011/02/14/symfony-1-3-9-and-1-4-9).

Development mailing list
------------------------

  * [\[Symfony2\] bootstrap.php and bootstrap_cache.php](https://groups.google.com/forum/#!topic/symfony-devs/ZXthOcNpIRs)
  * [\[Symfony2\] RFC - changing the default scope from container to request](https://groups.google.com/forum/#!topic/symfony-devs/VvYiZjWLc3g)
  * [Git Development Process](https://groups.google.com/forum/#!topic/symfony-devs/EUyqKpvm_ms)
  * [\[Symfony2\] ZF dependency](https://groups.google.com/forum/#!topic/symfony-devs/ihFLt_mWpyw)
  * [\[Symfony2\] RFC: Organization of projects in the Symfony2 universe](https://groups.google.com/forum/#!topic/symfony-devs/P0rqlbHkBn0)
  * [\[Symfony2\] DoctrineMigrationBundle](https://groups.google.com/forum/#!topic/symfony-devs/sTq0h2F3DHA)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [f9138d3](http://github.com/symfony/symfony/commit/f9138d313b83f951cf82a2f7f902a2d6dd14fbb3 "f9138d313b83f951cf82a2f7f902a2d6dd14fbb3 commit on github"): \[FrameworkBundle\] implemented single-pass config loading with intelligent option merging for FrameworkExtension (restructured config format to make processing more straightforward and added important changes that might break existing configs)
  * [743f25a](http://github.com/symfony/symfony/commit/743f25a287ebcd0cc6b58e984e19544108b6ba28 "743f25a287ebcd0cc6b58e984e19544108b6ba28 commit on github"): \[DependencyInjection\] create explicit factoryClass property for Definitions
  * [523e652](http://github.com/symfony/symfony/commit/523e652d9dcae71b143928df5f5eac02c7ce225a "523e652d9dcae71b143928df5f5eac02c7ce225a commit on github"): \[FrameworkBundle\] fixed the way profiler configuration works
  * [e540349](http://github.com/symfony/symfony/commit/e5403490e7ea226d19f4fb2b57bf209858caeea9 "e5403490e7ea226d19f4fb2b57bf209858caeea9 commit on github"): removed the need to define getNamespace() and getPath() in bundles
  * [f56a6ef](http://github.com/symfony/symfony/commit/f56a6efbf5b86e9da8204ee53f07eb9f416b0916 "f56a6efbf5b86e9da8204ee53f07eb9f416b0916 commit on github"): \[HttpFoundation\] File/File full coverage
  * [bd97471](http://github.com/symfony/symfony/commit/bd97471954f18ac3843a618ccc968e2d297a3b80 "bd97471954f18ac3843a618ccc968e2d297a3b80 commit on github"): \[HttpKernel\] added test coverage for cache warming
  * [c251a36](http://github.com/symfony/symfony/commit/c251a369351582324bf1afdd13b61ae01c3163a7 "c251a369351582324bf1afdd13b61ae01c3163a7 commit on github"): \[HttpFoundation\] added tests for Cookie
  * [9ba2943](http://github.com/symfony/symfony/commit/9ba2943aff2941c283065e0f09c05a572462fa50 "9ba2943aff2941c283065e0f09c05a572462fa50 commit on github"), [c5fb96b](http://github.com/symfony/symfony/commit/c5fb96b86b65ad0aa09f5c3ad5abada4f4f9a24e "c5fb96b86b65ad0aa09f5c3ad5abada4f4f9a24e commit on github"): \[HttpKernel\] added unit tests for Kernel
  * [39ed62d](http://github.com/symfony/symfony/commit/39ed62de46718af993e06a99d5e5f1ddfd7a8cbf "39ed62de46718af993e06a99d5e5f1ddfd7a8cbf commit on github"): translated validators resources into Japanese
  * [42a3e40](http://github.com/symfony/symfony/commit/42a3e404b28def5e85a1912412a6eb2311cbaf48 "42a3e404b28def5e85a1912412a6eb2311cbaf48 commit on github"): translated validators resources into Spanish
  * [6ff4120](http://github.com/symfony/symfony/commit/6ff41207843154c1f5546de54755e56bc9d9efd5 "6ff41207843154c1f5546de54755e56bc9d9efd5 commit on github"), [09a50c3](http://github.com/symfony/symfony/commit/09a50c3c55257edb95c102cb435e353f0b118208 "09a50c3c55257edb95c102cb435e353f0b118208 commit on github"): \[Form\] added Form option by_reference so that objects received from parent forms are modified by reference when this option is true (the default)
  * [74d0ac8](http://github.com/symfony/symfony/commit/74d0ac82f7d4ef2539a7fa0114025cdfd8229c54 "74d0ac82f7d4ef2539a7fa0114025cdfd8229c54 commit on github"): \[Form\] cleaned up ValueTransformerInterface (removed CollectionToStringTransformer)
  * [0b8fef2](http://github.com/symfony/symfony/commit/0b8fef234724cb4cb3a4ab37466efe193a6c7708 "0b8fef234724cb4cb3a4ab37466efe193a6c7708 commit on github"): \[Security/DependencyInjection\] adds support for merging security configurations. All passed config arrays will be transformed into the same structure regardless of what format they come from (massive commit which adds lots of methods and a new architecture)
  * [099b9de](http://github.com/symfony/symfony/commit/099b9dee1f4ad0ef411bb16fb38ab3a1ac91d1bb "099b9dee1f4ad0ef411bb16fb38ab3a1ac91d1bb commit on github"): \[FrameworkBundle\] integrated Configuration\Builder class for config merging and normalization
  * [7ad4f99](http://github.com/symfony/symfony/commit/7ad4f99153eb496bed17bfe6f17edb18276e91b1 "7ad4f99153eb496bed17bfe6f17edb18276e91b1 commit on github"): \[HttpFoundation\] File/UploadedFile, MimeTest, Exception full coverage
  * [b9ed739](http://github.com/symfony/symfony/commit/b9ed739d75fa59f5749be6c4b5ac15784fef2d91 "b9ed739d75fa59f5749be6c4b5ac15784fef2d91 commit on github"): fixed RedirectController - removed parmanent attribute before generate new url, added tests
  * [bebdcb2](http://github.com/symfony/symfony/commit/bebdcb242df685d822b7f0c4b712f67784401879 "bebdcb242df685d822b7f0c4b712f67784401879 commit on github"): \[HttpKernel\] added response cache-control modification if page is composed of ESIs
  * [ea4ab77](http://github.com/symfony/symfony/commit/ea4ab77b6d0f6983b67aa7bd856d3873258c6913 "ea4ab77b6d0f6983b67aa7bd856d3873258c6913 commit on github"): \[HttpKernel\] HttpCache now sends maxage=0 cache-control directive in case of Esi presence
  * [41bf849](http://github.com/symfony/symfony/commit/41bf849a637d9434f859eeafd816fec4a0ab51be "41bf849a637d9434f859eeafd816fec4a0ab51be commit on github"): \[HttpFoundation\] Request coverage
  * [9f30e42](http://github.com/symfony/symfony/commit/9f30e42c16ad24f5fd4dc512d2a85ffb785e5c26 "9f30e42c16ad24f5fd4dc512d2a85ffb785e5c26 commit on github"): added --debug/-d and --env/-d to console
  * [d447d22](http://github.com/symfony/symfony/commit/d447d22809e3751c5d6c13868c77a1657a8f04bd "d447d22809e3751c5d6c13868c77a1657a8f04bd commit on github"): \[DoctrineBundle, DoctrineAbstractBundle, DoctrineMongoDBBundle\] added container aware fixture loader
  * [5b95805](http://github.com/symfony/symfony/commit/5b95805340822da53aacc59229b747d590b26037 "5b95805340822da53aacc59229b747d590b26037 commit on github"), [f51dafc](http://github.com/symfony/symfony/commit/f51dafca3f181249ef58acb18d242a037a45371f "f51dafca3f181249ef58acb18d242a037a45371f commit on github"): \[Form\] added data_constructor option to Form
  * [9f77cab](http://github.com/symfony/symfony/commit/9f77cabd2fef2bbefa83a73312f94e297d74d8e0 "9f77cabd2fef2bbefa83a73312f94e297d74d8e0 commit on github"): \[TwigBundle\] cast non-array resources argument to array in form_field() twig function
  * [5d87d83](http://github.com/symfony/symfony/commit/5d87d83a10ebf001c1609f626d27300479aba308 "5d87d83a10ebf001c1609f626d27300479aba308 commit on github"): optimized duplication of Request objects
  * <del>[a8ec9b2](http://github.com/symfony/symfony/commit/a8ec9b27f044ea513c69442778c005cba7be8b1b "a8ec9b27f044ea513c69442778c005cba7be8b1b commit on github"): moved duplicated files to a new Config component</del> (reverted)
  * [82a8a3f](http://github.com/symfony/symfony/commit/82a8a3fb4234c5f5e87ec915f2ede1ad54b52dbf "82a8a3fb4234c5f5e87ec915f2ede1ad54b52dbf commit on github"): \[WebProfilerBundle, FrameworkBundle\] fixed events panel to handle closures correctly
  * <del>[f530808](http://github.com/symfony/symfony/commit/f53080860a2de21304ded72f5e6a9b6f8894dc0d "f53080860a2de21304ded72f5e6a9b6f8894dc0d commit on github"): moved Resource to the Config component</del> (reverted)
  * [fe694de](http://github.com/symfony/symfony/commit/fe694de7464ed18d9eb2947d7bc817bddde7965b "fe694de7464ed18d9eb2947d7bc817bddde7965b commit on github"), [2ed0b97](http://github.com/symfony/symfony/commit/2ed0b975f1799bbb18231166967951e1030a1c59 "2ed0b975f1799bbb18231166967951e1030a1c59 commit on github"), [5bf5933](http://github.com/symfony/symfony/commit/5bf593353f576e703c1b672a682935f437163545 "5bf593353f576e703c1b672a682935f437163545 commit on github"): \[Routing\] made trailing slashes in urls optional
  * [8cb3a23](http://github.com/symfony/symfony/commit/8cb3a237cc76176c7c31320ae85be85bcc197ca3 "8cb3a237cc76176c7c31320ae85be85bcc197ca3 commit on github"), [e929bc5](http://github.com/symfony/symfony/commit/e929bc5d1b3d958fc5b7d04308c21a4f61dc8cd2 "e929bc5d1b3d958fc5b7d04308c21a4f61dc8cd2 commit on github"): \[FrameworkBundle, HttpKernel\] allow any 2xx response code in a subrequest
  * [d85a839](http://github.com/symfony/symfony/commit/d85a83999704ccc958c7346fe869962b5b42b328 "d85a83999704ccc958c7346fe869962b5b42b328 commit on github"): \[Routing\] avoid locating imported resources as files unless they resolve to a FileLoader
  * [beaaa6d](http://github.com/symfony/symfony/commit/beaaa6d45720a0a8517c55aebc544dc000a086be "beaaa6d45720a0a8517c55aebc544dc000a086be commit on github"): \[BrowserKit\] fixed Response::__toString() method to take care of multiple header
  * <del>[19bbafc](http://github.com/symfony/symfony/commit/19bbafc441862d1d519e504386230253fcf9fbaa "19bbafc441862d1d519e504386230253fcf9fbaa commit on github"): \[Security\] refactored security context</del> (reverted)
  * [9749da6](http://github.com/symfony/symfony/commit/9749da6e52aa4f942e7e70b359e0c266a5e130e1 "9749da6e52aa4f942e7e70b359e0c266a5e130e1 commit on github"): \[Security\] performance improvements of PermissionGrantingStrategy
  * [b3cb02a](http://github.com/symfony/symfony/commit/b3cb02adf237ff04526933259d689194070f3040 "b3cb02adf237ff04526933259d689194070f3040 commit on github"): \[FrameworkBundle/Routing\] added 'type' option for main Router resource (and expose this in FrameworkExtension config)
  * [a5cfc22](http://github.com/symfony/symfony/commit/a5cfc2207c09f6182333b3b812673202701c33f3 "a5cfc2207c09f6182333b3b812673202701c33f3 commit on github"): \[Security/DependencyInjection\] updated SecurityBundle's configuration and some bug fixes in DIC config classes
  * [8684055](http://github.com/symfony/symfony/commit/8684055bdfbd4e0579b9bd3ff51cf97c9942f629 "8684055bdfbd4e0579b9bd3ff51cf97c9942f629 commit on github"): fixed calling *_vendors.sh scripts when not in the root of the project
  * [f1633f8](http://github.com/symfony/symfony/commit/f1633f89c40e69dcef50865825ec1c1e80216eba "f1633f89c40e69dcef50865825ec1c1e80216eba commit on github"): merged install_vendors.sh and update_vendors.sh
  * [b716b70](http://github.com/symfony/symfony/commit/b716b707badcaac7858e17eff07eecb7e7d737df "b716b707badcaac7858e17eff07eecb7e7d737df commit on github"): added missing console commands, proxy cache warmer and hydrator cache warmer to DoctrineMongoDBBundle
  * [1292925](http://github.com/symfony/symfony/commit/12929257021741a9d0c0d4b0c2d05836208cb324 "12929257021741a9d0c0d4b0c2d05836208cb324 commit on github"): \[AsseticBundle\] initial entry of assetic integration
  * [5c905be](http://github.com/symfony/symfony/commit/5c905beb13624d40a768e6e9ea98cb873e149c6e "5c905beb13624d40a768e6e9ea98cb873e149c6e commit on github"), [8588d55](http://github.com/symfony/symfony/commit/8588d55c11285117ef953ff25a6636bc6b594077 "8588d55c11285117ef953ff25a6636bc6b594077 commit on github"): moved common configuration classes to a new Config component
  * [20e31cd](http://github.com/symfony/symfony/commit/20e31cd3f256b777dda0a8e880336578d8063089 "20e31cd3f256b777dda0a8e880336578d8063089 commit on github"): \[HttpKernel\] added some details for two commonly encountered errors in Kernel.php and HttpKernel.php
  * [b9f4eab](http://github.com/symfony/symfony/commit/b9f4eab5c2be8fc29d671adf2fbbf8d065292466 "b9f4eab5c2be8fc29d671adf2fbbf8d065292466 commit on github"), [d22743c](http://github.com/symfony/symfony/commit/d22743cf3ace5110a2587c279f9055ec79b19ab7 "d22743cf3ace5110a2587c279f9055ec79b19ab7 commit on github"): \[Security/Acl\] added pre-generated schemas
  * [0643dc4](http://github.com/symfony/symfony/commit/0643dc44fddf347f4ffdc5764b141bfadc54aeb8 "0643dc44fddf347f4ffdc5764b141bfadc54aeb8 commit on github"): \[Security\] added a priority attribute to security voters
  * [5c7fe8f](http://github.com/symfony/symfony/commit/5c7fe8f866decdae3c6f543405bf1e64d119844d "5c7fe8f866decdae3c6f543405bf1e64d119844d commit on github"): \[Security\] simplified encoder factory implementation
  * [bc283f1](http://github.com/symfony/symfony/commit/bc283f1a66ccbdee2655274604fa87e970ca455b "bc283f1a66ccbdee2655274604fa87e970ca455b commit on github"): \[Security\] removed security.authentication_provider tag
  * [b685b3a](http://github.com/symfony/symfony/commit/b685b3ab4d306eaa1838e14406a9e390564715bf "b685b3ab4d306eaa1838e14406a9e390564715bf commit on github"): \[Security\] added logout success handler
  * [af81bca](http://github.com/symfony/symfony/commit/af81bcabf06c389a353ffde2bb3e6158bdee3970 "af81bcabf06c389a353ffde2bb3e6158bdee3970 commit on github"), [5eee0db](http://github.com/symfony/symfony/commit/5eee0db18e158e350d4c143792a1ea1e54ddaeec "5eee0db18e158e350d4c143792a1ea1e54ddaeec commit on github"): \[Templating\] refactored the component
  * [73cd26e](http://github.com/symfony/symfony/commit/73cd26e2ca4fa3528e2ee5680fac6c82f7897724 "73cd26e2ca4fa3528e2ee5680fac6c82f7897724 commit on github"): \[Serializer\] added the ability to add attributes to nodes using an array key begining with @
  * [4972bf6](http://github.com/symfony/symfony/commit/4972bf6350c3a2b68ccbd80171072f9f466787ef "4972bf6350c3a2b68ccbd80171072f9f466787ef commit on github"): \[DependencyInjection\] made getXsdValidationBasePath() and getNamespace() methods from DIC Extension class optional
  * [81765f8](http://github.com/symfony/symfony/commit/81765f8b6a0cc341869b9f5593730b8317cdd406 "81765f8b6a0cc341869b9f5593730b8317cdd406 commit on github"): \[DependencyInjection\] fixed XML loader
  * [7dbc09e](http://github.com/symfony/symfony/commit/7dbc09ed8b08a94b34184d7146ed1bf65c17fbc1 "7dbc09ed8b08a94b34184d7146ed1bf65c17fbc1 commit on github"): \[Form\] fixed reference handling in forms. Sometimes data wasn't written into the domain object, resulting in failed validation
  * [922cb0a](http://github.com/symfony/symfony/commit/922cb0a8323f749c334f2885c1ac2e909f690295 "922cb0a8323f749c334f2885c1ac2e909f690295 commit on github"): updated vendors script to allow checkout of a specific commit
  * [b8d5740](http://github.com/symfony/symfony/commit/b8d574087f29b3637d71fadceb678859d3e608c6 "b8d574087f29b3637d71fadceb678859d3e608c6 commit on github"): \[Security\] allowed authentication tokens to hold attributes
  * [14aa95b](http://github.com/symfony/symfony/commit/14aa95ba218c9fd6d02e770e279ed854314fea75 "14aa95ba218c9fd6d02e770e279ed854314fea75 commit on github"): added the concept of a main DIC extension for bundles. This allows for better conventions and better error messages if you use the wrong configuration alias in a config file
  * [7f182bd](http://github.com/symfony/symfony/commit/7f182bd877a88f36acadb2e2e7664f96aac55261 "7f182bd877a88f36acadb2e2e7664f96aac55261 commit on github"), [62e3053](http://github.com/symfony/symfony/commit/62e305376945022e0efb91a1f3a98d6eb2538749 "62e305376945022e0efb91a1f3a98d6eb2538749 commit on github"): implicitly load all registered bundles, all loading is now handled by load(), disable loading of an extension explcitly via setting the extension config to false
  * [a29a413](http://github.com/symfony/symfony/commit/a29a413c4828332fb87038dc436326cb3c306170 "a29a413c4828332fb87038dc436326cb3c306170 commit on github"): made DIC extensions members of the Container instead of static members
  * [1230bc6](http://github.com/symfony/symfony/commit/1230bc64419539c630b218b6e5204af800a97b75 "1230bc64419539c630b218b6e5204af800a97b75 commit on github"): \[AsseticBundle\] updated config for new LESS filter
  * [cd5b603](http://github.com/symfony/symfony/commit/cd5b60359d3af704c0e051ceb0370f53731c0962 "cd5b60359d3af704c0e051ceb0370f53731c0962 commit on github"): \[AsseticBundle\] added local caching to the controller
  * [e62031a](http://github.com/symfony/symfony/commit/e62031a54e1902cf54c1d2001772fba8357a7ba6 "e62031a54e1902cf54c1d2001772fba8357a7ba6 commit on github"): \[AsseticBundle\] fixed closure .jar configuration
  * [dfd9218](http://github.com/symfony/symfony/commit/dfd921822a534dd5d88927560047c63a7595f8ac "dfd921822a534dd5d88927560047c63a7595f8ac commit on github"): \[Security/Http\] added CSRF protection to the form-login
  * [82c6844](http://github.com/symfony/symfony/commit/82c684414757af8951cef3bf0ec1b36d98f62aba "82c684414757af8951cef3bf0ec1b36d98f62aba commit on github"): \[Security\] moved Security classes out of DoctrineBundle, cleaned-up SecurityExtension accordingly
  * [53f3ff8](http://github.com/symfony/symfony/commit/53f3ff8258d4efa4082d50ca0dd01f8c731b4dad "53f3ff8258d4efa4082d50ca0dd01f8c731b4dad commit on github"): \[Security\] added a chain user provider
  * [1593d6f](http://github.com/symfony/symfony/commit/1593d6f75deab634e6e31208ac0ee89f942a01e6 "1593d6f75deab634e6e31208ac0ee89f942a01e6 commit on github"): \[Form\] added method FieldInterface::isEmpty()
  * [40acc6a](http://github.com/symfony/symfony/commit/40acc6ac79ecafb897bbf301259ac3620a312a39 "40acc6ac79ecafb897bbf301259ac3620a312a39 commit on github"): \[Form\] fixed ChoiceField::isChoiceSelected() to differentiate between zero and empty
  * [14c3518](http://github.com/symfony/symfony/commit/14c3518c6e4198db0c2d133f01614df7364ef8d8 "14c3518c6e4198db0c2d133f01614df7364ef8d8 commit on github"): \[Form\] fixed if a DateField or TimeField is displayed with select boxes, either all or no select box must have a value selected
  * [df011ed](http://github.com/symfony/symfony/commit/df011ed1efc2de81396b37094fda1688711e71c8 "df011ed1efc2de81396b37094fda1688711e71c8 commit on github"): \[Form\] fixed isXXXWithinRange() methods in TimeField and DateField to ignore empty dropdowns
  * [9569262](http://github.com/symfony/symfony/commit/9569262635344223041c3812cbc48fc2838e9b31 "9569262635344223041c3812cbc48fc2838e9b31 commit on github"): \[Form\] fixed date handling classes to use server timezone by default
  * [077d192](http://github.com/symfony/symfony/commit/077d1921b3d35d5bc8bc3aec2af579a24fa8c59b "077d1921b3d35d5bc8bc3aec2af579a24fa8c59b commit on github"): added the support of the validation in the Builder
  * [990910d](http://github.com/symfony/symfony/commit/990910d601e9a34ddf11fdf7076fda4c15994a3a "990910d601e9a34ddf11fdf7076fda4c15994a3a commit on github"): converted SwiftmailerBundle to use a Configuration class
  * [0a33cbb](http://github.com/symfony/symfony/commit/0a33cbb4033a12b6aab499352d0d580c487bcd95 "0a33cbb4033a12b6aab499352d0d580c487bcd95 commit on github"): \[Finder\] added support for relative path
  * [c5e4dfb](http://github.com/symfony/symfony/commit/c5e4dfb5a631d1144eb02ea59793a38e7335898d "c5e4dfb5a631d1144eb02ea59793a38e7335898d commit on github"): \[DependencyInjection\] added to InvalidArgumentException messages to clarify when a service is given an invalid tags value
  * [6b12c21](http://github.com/symfony/symfony/commit/6b12c212615a285a43124b70b27b476e6d5c7ccd "6b12c212615a285a43124b70b27b476e6d5c7ccd commit on github"): moved DependencyInjection\Configuration to Config\Definition
  * [76262b2](http://github.com/symfony/symfony/commit/76262b2ccc2129d967a6a5bb9e7dae6f73d35968 "76262b2ccc2129d967a6a5bb9e7dae6f73d35968 commit on github"): fixed spool handling

Documentation
-------------

  * New <a href="http://trac.symfony-project.org/wiki/IRCLogs20110217">IRC Logs 2011-02-17</a> page
  * Updated <a href="http://trac.symfony-project.org/wiki/IRCLogs20110203">IRC Logs 2011-02-03</a> page

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Symfony &amp; front-end developer at [Exercise.com](http://exercise.com/) - full-time based in Mountain View, California (USA) - Contact: jobs{at}exercise.com

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfRssPP](http://www.symfony-project.org/plugins/sfRssPPPlugin): provides an easy way to get one or more RSS feeds without PHP code.
  * [stashboardTasks](http://www.symfony-project.org/plugins/stashboardTasksPlugin): gives you tasks to update your Stashboard installation. Just put your API credentials in app.yml, and update statuses from the command line.
  * [sfWebmoneyAuth](http://www.symfony-project.org/plugins/sfWebmoneyAuthPlugin): provides authentication and authorization features above the standard security feature of symfony.
  * [xTool](http://www.symfony-project.org/plugins/xToolPlugin): (no description)
  * [sfFlashWidget](http://www.symfony-project.org/plugins/sfFlashWidgetPlugin): inspired by the sfWidgetFormInputFileEditable widget of Fabien Potencier (a symfony included class). It installs a new widget that represents an upload HTML input tag (template -able) for flash objects.

Updated plugins
---------------

  * [sfProjectAnalyser](http://www.symfony-project.org/plugins/sfProjectAnalyserPlugin):
    * fixed getLibsOutput() and some typos

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * added new override to allow keeping scroll position on grid reload
    * fixed a bug with GroupingListView that was causing groups to loose their collapsed state on store reload

  * [sdInteractiveChart](http://www.symfony-project.org/plugins/sdInteractiveChartPlugin):
    * updated the automated js include code
    * improved commenting
    * updated README

  * [ahDoctrineEasyEmbeddedRelations](http://www.symfony-project.org/plugins/ahDoctrineEasyEmbeddedRelationsPlugin):
    * use Doctrine_Core instead of Doctrine

  * [csDoctrineActAsSortable](http://www.symfony-project.org/plugins/csDoctrineActAsSortablePlugin):
    * use Doctrine_Core instead of Doctrine

  * [apostrophePeople](http://www.symfony-project.org/plugins/apostrophePeoplePlugin):
    * fixed a bug in the headshot template
    * search results link to the best engine page for the person
    * sorting people slot normal view
    * you can remove a headshot by clicking to change it, then using the trashcan and saving your selection
    * people slots link to the best people engine page for the individual
    * alphabetized the categories in the people plugin

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * made googleAnalytics into a partial

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * refactored the best-blog-post algorithm out to aEngineTools where the people plugin can benefit from it


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [Article Gold](http://www.articlegold.com): \(English\) Popular Articles Directory built on Symfony 1.4

New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [Software development and productivity](http://warambil.wordpress.com/) \([feed](http://feeds.warambil.wordpress.com/)\) \(English\)
  * [1个饼](http://www.onepie.org/category/symfony-2/) \([feed](http://www.onepie.org/category/symfony-2/feed/)\) \(Chinese\)

They talked about us
--------------------

  * [less doctrine queries in symfony admin modules](http://symfony-world.blogspot.com/2011/02/less-doctrine-queries-in-symfony-admin.html)
  * [Se publican Symfony 1.3.9 y 1.4.9](http://www.symfony.es/2011/02/14/se-publican-symfony-1-3-9-y-1-4-9/)
  * [Rilasciato symfony 1.4.9](http://www.symfony.it/articoli/406/rilasciato-symfony-1-4-9/)
  * [symfony 1.4.9 wydane](http://www.fizyk.net.pl/blog/symfony-1-4-9-wydane)
  * [Decrease number of queries for admin generated module: the better way](http://www.fizyk.net.pl/blog/decrease-number-of-queries-for-admin-generated-module-the-better-way)
  * [Symfony Live 2011 San Francisco notes](http://blog.servergrove.com/2011/02/15/symfony-live-2011-san-francisco-notes/)
  * [Wurfl Symfony2 Hackday](http://blog.liip.ch/archive/2011/02/15/wurfl-symfony2-hackday.html)
  * [Symfohub](http://www.symfony.it/articoli/409/symfohub/)
  * [sfEmailPlugin](http://www.symfonylab.com/sfemailplugin-2/)
  * [Présentation du lxErrorLoggerPlugin](http://www.lexik.fr/blog/symfony/symfony/presentation-du-lxerrorloggerplugin-1433)
  * [Sort doctrine Model by default](http://www.fizyk.net.pl/blog/sort-doctrine-model-by-default)
  * [Introducing Virtual Foreign Keys](http://propel.posterous.com/introducing-virtual-foreign-keys)
  * [Symfony 1.4 und 1.3 erhalten Patches](http://www.onlinepc.ch/index.cfm?page=104029&amp;artikel_id=27197)
  * [symfttpd 1.1.1 released](http://laurent.bachelier.name/2011/02/symfttpd-1-1-1-released/)
  * [Todo list with Symfony 1.4 – Part 2 (Data Model)](http://warambil.wordpress.com/2011/02/15/todo-list-with-symfony-1-4-part-2-data-model/)
  * [Todo list with Symfony 1.4 – Part 3 (Login form)](http://warambil.wordpress.com/2011/02/15/todo-list-with-symfony-1-4-part-3-login-form/)
  * [Todo list with Symfony 1.4 – Part 4 (Show user’s lists)](http://warambil.wordpress.com/2011/02/15/todo-list-with-symfony-1-4-%E2%80%93-part-4-show-user-lists/)
  * [Todo list with Symfony 1.4 – Part 5 (Create new list)](http://warambil.wordpress.com/2011/02/16/todo-list-with-symfony-1-4-part-5-create-new-list/)
  * [Todo list with Symfony 1.4 – Part 6 (Adding and marking tasks)](http://warambil.wordpress.com/2011/02/16/todo-list-with-symfony-1-4-part-6-adding-and-marking-tasks/)
  * [Todo list with Symfony 1.4 – Part 7 (Reordering tasks)](http://warambil.wordpress.com/2011/02/16/todo-list-with-symfony-1-4-%E2%80%93-part-7-reordering-tasks/)
  * [Todo list with Symfony 1.4 – Part 8 (Editing a list)](http://warambil.wordpress.com/2011/02/16/todo-list-with-symfony-1-4-part-8-editing-a-list/)
  * [自定义Symfony filter(过滤器）](http://www.onepie.org/2011/02/17/custom-symfony-filter/)
  * [Symfony, symlinks und Cache Problem](http://www.kai-schaumann.de/blog/2011/02/20/symfony-symlinks-und-cache-problem/)
  * [Return sfView::NONE in Symfony2](http://www.metod.si/return-sfviewnone-in-symfony2/)
  * [Symfony IV. rész – egy form embedder plugin](http://blog.tlsys.hu/symfony_form_embedder_plugin/)
  * [Entrevista al creador de Symfony2](http://d2.com.es/entrevista-al-creador-de-symfony-2/19525/)
  * [Doctrine Query Cache w Symfony](http://michal.durys.pl/2011/02/doctrine-query-cache-w-symfony/)
  * [Simplifying the drawing of forms in Symfony](http://www.thewebshop.ca/blog/2011/02/simplifying-the-drawing-of-forms-in-symfony/)
  * [Getting Symfony 2 into the Cloud](http://www.webhostingwikipedia.com/getting-symfony-2-into-the-cloud/)
  * [Filtrar dados do componente sfWidgetFormDoctrineChoice](http://fabriciokerber.blogspot.com/2011/02/filtrar-dados-do-componente.html)
  * [Spunti e suggerimenti su Symfony2](http://www.sastgroup.com/feedreader/spunti-e-suggerimenti-su-symfony-2/)
  * [Entrevista con Fabien Potencier](http://desarrolla2.com/php-symfony/entrevista-con-fabien-potencier/)
  * [Symfony2: конфигурирование пакетов](http://hudson.su/2011/02/18/symfony-2-bundle-configuration/)
  * [MySQL Workbenchからschema.ymlを生成する](http://blog.loadlimits.info/2011/02/mysql-workbench%E3%81%8B%E3%82%89schema-yml%E3%82%92%E7%94%9F%E6%88%90%E3%81%99%E3%82%8B/)
  * [【PHP案件】フレームワークはSymfony](http://ameblo.jp/vacanken/entry-10803113505.html)
  * [symfonyに関する本はなぜ少ないのか](http://bontetsu.jp/?p=211)
  * [Теория кеширования](http://symfony.artsofte.ru/blog/post/id/45)
  * [Symfony2 and Drupal 8](http://alen.mobi/blog/2011/02/15/symfony2-and-drupal-8/)
  * [ネームスペースを指定してGet](http://d.hatena.ne.jp/moroto1122/20110215/1297741978)
  * [symfonyとHTMLファイルを同居させた際のリンク切れ回避方法](http://blog.asial.co.jp/802)
  * [4 etapes pour encoder les URL avec Symfony](http://www.avanim-prod.com/blog/symfony/4-etapes-pour-encoder-les-url-avec-symfony-425)
  * [OpenSky at Symfony Live, San Francisco](http://blog.shopopensky.com/2011/02/opensky-at-sflive2011/)
  * [Symfony2: Crear un bundle en PR5](http://blog.eleazan.net/2011/02/symfony-2-crear-un-bundle-en-pr5/)
