A week of symfony #254 (7->13 November 2011)
============================================

先週、Symfony コミュニティでは、ゲーミフィケーションを採用した新しい [開発コミュニティプラットフォームを発表](http://symfony.com/blog/developing-the-symfony-community) され、Symfony コミュニティの今後の発展に大きな期待が集まりました。
SensioLabs Connectと名付けられたこのプラットフォームに参加すると、コミュニティでのさまざまな活動に対して小さな賞が贈られるようになります。
また、初めての [Symfony コミュニティアワード](http://awards.symfony.com/) の開催もアナウンスされ、コミュニティで活躍したメンバーが投票により選ばれることになりました。
 
開発メーリングリスト
--------------------

  * [HttpCache issue](https://groups.google.com/forum/#!topic/symfony-devs/2qKekaBJfV4)
  * [Interface with supports method](https://groups.google.com/forum/#!topic/symfony-devs/cxWDUG5jo9Y)
  * [\[Symfony2\] brain storming master/slave setups](https://groups.google.com/forum/#!topic/symfony-devs/W865kY4rSUc)


Symfony2 開発ハイライト
-----------------------

[2.0 ブランチ](http://github.com/symfony/symfony/commits/2.0):

  * [380c67e](http://github.com/symfony/symfony/commit/380c67efc8bb5cc26d15269c145a2379d77729af "380c67efc8bb5cc26d15269c145a2379d77729af commit on github"): \[FrameworkBundle\] fixed HttpKernel when the app is stateless
  * [c31c512](http://github.com/symfony/symfony/commit/c31c512466c92faa59ec6f5db83df88fce870340 "c31c512466c92faa59ec6f5db83df88fce870340 commit on github"): \[FrameworkBundle\] fixed output buffering when an error occurs in a sub-request
  * [9e6ba9a](http://github.com/symfony/symfony/commit/9e6ba9ae893f5c16a42b36c10ac9dfb5b63f41df "9e6ba9ae893f5c16a42b36c10ac9dfb5b63f41df commit on github"), [d789f94](http://github.com/symfony/symfony/commit/d789f9424e0c93f7d98ae74817ccacb23555b754 "d789f9424e0c93f7d98ae74817ccacb23555b754 commit on github"), [7346896](http://github.com/symfony/symfony/commit/7346896129b7e1c466c160abf484ea8624fa8bec "7346896129b7e1c466c160abf484ea8624fa8bec commit on github"): \[Serializer\] added a supportsNormalization method
  * [414d4be](http://github.com/symfony/symfony/commit/414d4be7e81fecefa30f7f1c338f412565475c45 "414d4be7e81fecefa30f7f1c338f412565475c45 commit on github"): \[Doctrine\] refactored unit tests
  * [9d2ab9c](http://github.com/symfony/symfony/commit/9d2ab9ca9c1762c529e053cefd39a5e626102133 "9d2ab9ca9c1762c529e053cefd39a5e626102133 commit on github"): \[Doctrine\] fixed security user reloading when the user has been changed via a form with validation errors
  * [a245e15](http://github.com/symfony/symfony/commit/a245e154344c5860ba9847839afbd37326a44c35 "a245e154344c5860ba9847839afbd37326a44c35 commit on github"): \[DomCrawler\] trim URI in getURI
  * [45b218e](http://github.com/symfony/symfony/commit/45b218e7c4cb6f1d8280c6cd09b262395f8f24a4 "45b218e7c4cb6f1d8280c6cd09b262395f8f24a4 commit on github"): \[Translation\] added detection for circular references when adding a fallback catalogue
  * [6b0e7c8](http://github.com/symfony/symfony/commit/6b0e7c8c410bdc646e29b7af24d6664e5dd1d3ac "6b0e7c8c410bdc646e29b7af24d6664e5dd1d3ac commit on github"): \[Translation\] removed unneeded methods
  * [8351a11](http://github.com/symfony/symfony/commit/8351a112861cd1cc71fbe35d69455c504d2f6acf "8351a112861cd1cc71fbe35d69455c504d2f6acf commit on github"): added check for array fields to be integers in reverseTransform method
  * [e83e00a](http://github.com/symfony/symfony/commit/e83e00a7b881e6d1eccdd8c3213ca78c7add2d37 "e83e00a7b881e6d1eccdd8c3213ca78c7add2d37 commit on github"): fixed rendering of FileType (value is not a valid attribute for input[type=file])
  * [ed1a6c2](http://github.com/symfony/symfony/commit/ed1a6c2e453025ceff40193a1ac53aeb1f72647a "ed1a6c2e453025ceff40193a1ac53aeb1f72647a commit on github"), [29e12af](http://github.com/symfony/symfony/commit/29e12affb064882d5599f16a8e13f8975148520c "29e12affb064882d5599f16a8e13f8975148520c commit on github"): \[TwigBundle\] do not clean output buffering below initial level (this resulted in issues with PHPUnit 3.6, which will buffer all output and clean them in the end)
  * [7cba0a0](http://github.com/symfony/symfony/commit/7cba0a07b6e34ca4721e7be12d610a5dc3f3a5d4 "7cba0a07b6e34ca4721e7be12d610a5dc3f3a5d4 commit on github"): \[Bridge/Monolog\] also identify FirePHP by the X-FirePHP-Version header
  * [bb5fb79](http://github.com/symfony/symfony/commit/bb5fb79c3d86d86f286ac44a3ef77ccc7c1b9307 "bb5fb79c3d86d86f286ac44a3ef77ccc7c1b9307 commit on github"): changed the way we store the current ob level
  * [4858fbe](http://github.com/symfony/symfony/commit/4858fbe7e0f991dd3e8f0a3846eb0634b76fdd07 "4858fbe7e0f991dd3e8f0a3846eb0634b76fdd07 commit on github"): \[TwigBundle\] fixed trace to not show 'in at line' when file/line are empty

[master ブランチ](http://github.com/symfony/symfony/commits/master):

  * [6f05544](http://github.com/symfony/symfony/commit/6f05544424480f1ccd008cf773dc573d47586019 "6f05544424480f1ccd008cf773dc573d47586019 commit on github"): \[Console\] added an exception when overriding an existing argument (added some unit tests for option and arguments overriding)
  * [47b888a](http://github.com/symfony/symfony/commit/47b888a9579f65d10f568b90fa4820fb8c1c0208 "47b888a9579f65d10f568b90fa4820fb8c1c0208 commit on github"): added the real template name when an error occurs in a Twig template
  * [47fca8e](http://github.com/symfony/symfony/commit/47fca8e0a0ab74f88d2c37838d62344e28bb37a2 "47fca8e0a0ab74f88d2c37838d62344e28bb37a2 commit on github"): \[HttpKernel\] fixed file storage for the profiler
  * [a7296e7](http://github.com/symfony/symfony/commit/a7296e7c84df28201276648757b04b2da2526018 "a7296e7c84df28201276648757b04b2da2526018 commit on github"): \[Security\] made exceptions thrown by the user checker and the checkAuthentication() method use the hideUserNotFoundExceptions flag
  * [e1822e7](http://github.com/symfony/symfony/commit/e1822e78076040a64755b31f22e0d46f801d9bb0 "e1822e78076040a64755b31f22e0d46f801d9bb0 commit on github"): enable dynamic set of validation groups by a callback or Closure
  * [d08ec5e](http://github.com/symfony/symfony/commit/d08ec5e55f7e90a44589a50fdbc5c86f7278ff7f "d08ec5e55f7e90a44589a50fdbc5c86f7278ff7f commit on github"): added DelegatingValidator tests
  * [796c6b2](http://github.com/symfony/symfony/commit/796c6b2f8de8b3fc653542d2eb8f3b22501f2a1e "796c6b2f8de8b3fc653542d2eb8f3b22501f2a1e commit on github"): \[Locale\] added getIcuVersion and getIcuDataVersion to Locale
  * [9c2a26d](http://github.com/symfony/symfony/commit/9c2a26db12d6f5a488c4e22e2cb134e4039d30d5 "9c2a26db12d6f5a488c4e22e2cb134e4039d30d5 commit on github"): \[Translation\] added Mo loader tests
  * [56cb7a5](http://github.com/symfony/symfony/commit/56cb7a515bfb028e00767c3c73ed15d66a44fb6b "56cb7a515bfb028e00767c3c73ed15d66a44fb6b commit on github"): \[Translation\] added gettext PO and MO Dumper
  * [4d80ebd](http://github.com/symfony/symfony/commit/4d80ebd5c85743812a4859d26b2e5d204dfa59d7 "4d80ebd5c85743812a4859d26b2e5d204dfa59d7 commit on github"): \[Security\] remove security token if user was deleted, is disabled or locked to prevent infinite redirect loops to the login path

