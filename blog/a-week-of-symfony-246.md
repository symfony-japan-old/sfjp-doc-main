---
layout: default
title: A week of symfony #246 (12->18 September 2011)
---

A week of symfony #246 (12->18 September 2011)
==============================================

先週、[Symfony 1.4.14 がリリースされました](http://symfony.com/blog/symfony-1-4-14-released)。このリリースでは、Symfonyコミュニティから提案された複数の改善と修正が行われています。また、[Symfony2 公式リポジトリ](https://github.com/symfony/symfony/) のウォッチャーの数が 3,000 を越えました。
 
開発メーリングリスト
--------------------

  * [カスタムクラス内での Doctrine クエリー](https://groups.google.com/forum/#!topic/symfony-devs/ANhemHPnFXk)

symfony 1 開発ハイライト
------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=18%2F09%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r33021](http://trac.symfony-project.org/changeset/33021 "33021 revision on trac"): \[1.4\] fixed sfCacheSessionStorage does not serialize properly, also uses wrong option name for httponly
  * [r33022](http://trac.symfony-project.org/changeset/33022 "33022 revision on trac"): \[1.4\] fixed auto_link_text() when an email address is already linked
  * [r33025](http://trac.symfony-project.org/changeset/33025 "33025 revision on trac"): \[1.4\] fixed sfCacheSessionStorage does not always check whether HTTP_USER_AGENT is set
  * [r33026](http://trac.symfony-project.org/changeset/33026 "33026 revision on trac"): \[1.4\] made sfCacheSessionStorage class code faster
  * [Milestone 1.4.14 completed](http://trac.symfony-project.org/milestone/1.4.14)

Symfony2 開発ハイライト
-----------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [aecfd0a](http://github.com/symfony/symfony/commit/aecfd0a8917370edd237120352749141ffa85362 "aecfd0a8917370edd237120352749141ffa85362 commit on github"): \[HttpFoundation\] support user and password in url
  * [e6e5146](http://github.com/symfony/symfony/commit/e6e5146ccba6ac80f6a3823ff6ce89bb3667aa39 "e6e5146ccba6ac80f6a3823ff6ce89bb3667aa39 commit on github"): \[Translation\] now support ResourceBundle
  * [cfc202b](http://github.com/symfony/symfony/commit/cfc202be93f98a0addf0e907b45b73566265c897 "cfc202be93f98a0addf0e907b45b73566265c897 commit on github"), [27dcc18](http://github.com/symfony/symfony/commit/27dcc187f6f4eacfefee4fad908212d31c75153b "27dcc187f6f4eacfefee4fad908212d31c75153b commit on github"): bumped versions of Twig and Swiftmailer
  * [73c8d2b](http://github.com/symfony/symfony/commit/73c8d2ba744d8a74df512f730a67e8c9f8a123c6 "73c8d2ba744d8a74df512f730a67e8c9f8a123c6 commit on github"): \[Form\] fixed error bubbling for Date and Time types when rendering as multiple choices
  * [53b4cd8](http://github.com/symfony/symfony/commit/53b4cd8c9c963c9f6cea41a1fd68a118dd0f7870 "53b4cd8c9c963c9f6cea41a1fd68a118dd0f7870 commit on github"): \[FrameworkBundle\] made code more robust
  * [400159d](http://github.com/symfony/symfony/commit/400159de4f1d2ace9eefa77962e7cb1f95d3ea37 "400159de4f1d2ace9eefa77962e7cb1f95d3ea37 commit on github"), [fabec37](http://github.com/symfony/symfony/commit/fabec37edcc8f34eeff82fbf84ef0fdf9ea4f2d9 "fabec37edcc8f34eeff82fbf84ef0fdf9ea4f2d9 commit on github"): \[FrameworkBundle\] made DIC placeholders replacement in route defaults only when the parameter exists in the container
  * [f9ecdfe](http://github.com/symfony/symfony/commit/f9ecdfeb0559448c598294b5740fdb3b4213ca13 "f9ecdfeb0559448c598294b5740fdb3b4213ca13 commit on github"): \[FrameworkBundle\] added sc parameters replacement in route requirements
  * [c5e0c80](http://github.com/symfony/symfony/commit/c5e0c80a76e78994e0d6e6fed07091c01349a04c "c5e0c80a76e78994e0d6e6fed07091c01349a04c commit on github"): \[HttpFoundation\] made FileBinaryMimeTypeGuesser command configurable
  * [c985ffa](http://github.com/symfony/symfony/commit/c985ffaa99fcdc6baa6eb94a2dd059cf2428aac4 "c985ffaa99fcdc6baa6eb94a2dd059cf2428aac4 commit on github"): \[Translation\] fixed message selector when the message is empty
  * [c50a3a1](http://github.com/symfony/symfony/commit/c50a3a194d5d2d1108aa32df830b9107039b4416 "c50a3a194d5d2d1108aa32df830b9107039b4416 commit on github"): \[Translation\] fixed transchoice when used with a fallback
  * [79710ed](http://github.com/symfony/symfony/commit/79710edb8abeda71b0991669cbd5059385aaf241 "79710edb8abeda71b0991669cbd5059385aaf241 commit on github"), [9ffd8ca](http://github.com/symfony/symfony/commit/9ffd8ca99c32cb0d463ea56a59bf61ecce7e0e22 "9ffd8ca99c32cb0d463ea56a59bf61ecce7e0e22 commit on github"): \[Translation\] added a MessageCatalogue::defines() method to check if a string has a translation (but without taking into account the fallback mechanism)
  * [5526072](http://github.com/symfony/symfony/commit/5526072dba59602d4eb11a2695fa925dc975ecde "5526072dba59602d4eb11a2695fa925dc975ecde commit on github"): \[Translation\] added support for more than one fallback locale
  * [9fb15c7](http://github.com/symfony/symfony/commit/9fb15c7cb2a48588cec40d78b9d6c6482bc9f1e3 "9fb15c7cb2a48588cec40d78b9d6c6482bc9f1e3 commit on github"): \[Process\] workaround a faulty implementation of is_executable on Windows
  * [43b55ef](http://github.com/symfony/symfony/commit/43b55efd04d26396043cab0b3525a4051e219dee "43b55efd04d26396043cab0b3525a4051e219dee commit on github"): \[Locale\] added support for yy format in StubIntlDateFormatter
  * [bede420](http://github.com/symfony/symfony/commit/bede42065eb528eaeab52dc509e34da0df1d0823 "bede42065eb528eaeab52dc509e34da0df1d0823 commit on github"): \[Config\] fixed FileResource usage of is_file (we must use file_exists here as the resource can be a file or a directory)
  * [046a125](http://github.com/symfony/symfony/commit/046a125ef763bb909103c1506b48692cde175e78 "046a125ef763bb909103c1506b48692cde175e78 commit on github"): \[FrameworkBundle\] set the file storage as default storage for Symfony2
  * [0826d1c](http://github.com/symfony/symfony/commit/0826d1c717c5e35ee9840ae5b38844ab727c6a1c "0826d1c717c5e35ee9840ae5b38844ab727c6a1c commit on github"): \[WebProfilerBundle\] added a way to filter logs by priority

