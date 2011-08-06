A week of symfony #239 (25->31 July 2011)
=========================================

Symfony 2.0.0バージョンがついに[今週リリースされました](http://symfony.com/blog/symfony-2-0), 18ヶ月前に始まった素晴らしい旅の終わりを示しています。このリリースはまた、Symfonyプロジェクトの輝かしい未来とその生態系の拡大が始まったことを示しています。 
 
開発ML
------------------------

  * [DIコンテナコンポーネントのドキュメント](https://groups.google.com/forum/#!topic/symfony-devs/I5g7lijdkWM)
  * [\[Symfony2\] ParameterBagと配列へのデータのセット](https://groups.google.com/forum/#!topic/symfony-devs/2-SWFtFKwxQ)
  * [Symfony 2.1と2.0のメンテナンスブランチ](https://groups.google.com/forum/#!topic/symfony-devs/JGYWiiUEJqw)
  * [2.0 リリースのためのバンドルのタギング](https://groups.google.com/forum/#!topic/symfony-devs/XxUz1yITBVM)

symfony 1 開発ハイライト 
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=31%2F07%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r32835](http://trac.symfony-project.org/changeset/32835 "32835 revision on trac"): \[1.4\] fixed when the renderer does not have the translate_choices option (see sfFormExtraPlugin for some examples)
  * [r32836](http://trac.symfony-project.org/changeset/32836 "32836 revision on trac"): \[1.4\] fixed guessFromFileBinary in class sfvalidatorFile does not support MIME type including dot

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [5219f81](http://github.com/symfony/symfony/commit/5219f81f3575277aab9263c3a64113ee632c8fb2 "5219f81f3575277aab9263c3a64113ee632c8fb2 commit on github"): use the $status parameter instead of fixed value when creating a RedirectResponse
  * [0b3ff39](http://github.com/symfony/symfony/commit/0b3ff39704a6978b6183a24081ce2eb2854eb8bd "0b3ff39704a6978b6183a24081ce2eb2854eb8bd commit on github"): fix supported cookie date formats
  * [c53c169](http://github.com/symfony/symfony/commit/c53c1692c29007fd6df23b9cb08560daac475642 "c53c1692c29007fd6df23b9cb08560daac475642 commit on github"): added a CONTRIBUTORS file
  * [3ea31a0](http://github.com/symfony/symfony/commit/3ea31a02630412b1c732ee1647a0724378f67665 "3ea31a02630412b1c732ee1647a0724378f67665 commit on github"), [85c0087](http://github.com/symfony/symfony/commit/85c0087825ccd9b8f4f25ab3120aca2820f5daa1 "85c0087825ccd9b8f4f25ab3120aca2820f5daa1 commit on github"): \[TwigBridge\] made the locale configurable for the trans and transchoice filters
  * [04ac1fd](http://github.com/symfony/symfony/commit/04ac1fdba2498d19977f8967d50b976898edeafe "04ac1fdba2498d19977f8967d50b976898edeafe commit on github"): \[Routing\] changed UrlGeneratorInterface::generate() signature to allow passing objects instead of arrays
  * [853935f](http://github.com/symfony/symfony/commit/853935fbabce601f38a477161fafcd535e1fe23d "853935fbabce601f38a477161fafcd535e1fe23d commit on github"): \[HttpFoundation\] made PHP_AUTH_PW optional
  * [c558b78](http://github.com/symfony/symfony/commit/c558b78bc61211977b31e5d26d5a150f6999547c "c558b78bc61211977b31e5d26d5a150f6999547c commit on github"): avoid rendering the ChoiceType separator if all choices are preferred_choices
  * [07298ac](http://github.com/symfony/symfony/commit/07298ac699a648e67095575f5fa2004359dbf7a9 "07298ac699a648e67095575f5fa2004359dbf7a9 commit on github"): \[Console\] changed back to fgets() in DialogHelper
  * [6773cd7](http://github.com/symfony/symfony/commit/6773cd7e05d3b19eb258c889ff0dcd030e6174ef "6773cd7e05d3b19eb258c889ff0dcd030e6174ef commit on github"): \[Serializer\] removed @api since its not yet part of the stable API
  * [e16ccaa](http://github.com/symfony/symfony/commit/e16ccaac711f5a98c6914203e6a197e1301217f0 "e16ccaac711f5a98c6914203e6a197e1301217f0 commit on github"): \[SecurityBundle\] added short description and help for the init:acl command
  * [ec9c0aa](http://github.com/symfony/symfony/commit/ec9c0aab64d7d7c5a70ac807bff774df1fac31dc "ec9c0aab64d7d7c5a70ac807bff774df1fac31dc commit on github"), [08072e4](http://github.com/symfony/symfony/commit/08072e4595cce1627daeb03cc3f8a5a873e8e2e2 "08072e4595cce1627daeb03cc3f8a5a873e8e2e2 commit on github"), [41fe826](http://github.com/symfony/symfony/commit/41fe82656b5648e195656e3d69ea5981ea12ae53 "41fe82656b5648e195656e3d69ea5981ea12ae53 commit on github"), [f2e4d35](http://github.com/symfony/symfony/commit/f2e4d359318d8d08072b310cb793dd2606dec593 "f2e4d359318d8d08072b310cb793dd2606dec593 commit on github"): harmonized commands documentation by changing ./app/console to php app/console
  * [c3ebdbf](http://github.com/symfony/symfony/commit/c3ebdbf9cceddb82cd2089aaef8c7b992e536363 "c3ebdbf9cceddb82cd2089aaef8c7b992e536363 commit on github"): prepared Symfony 2.0.0 release

