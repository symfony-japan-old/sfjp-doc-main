---
layout: default
title: A week of symfony #250 (10->16 October 2011)
---

A week of symfony #250 (10->16 October 2011)
============================================

先週、すべての Symfony2 コンポーネントが Composer のパブリックリポジトリである [packagist.org](http://packagist.org/) に登録されました。Composer はパッケージマネージャで、もうすぐ Symfony2 で使えるようになります。
また、Symfony2 リポジトリの master ブランチで、[HttpKernel のイベントリスナーが EventSubscriberInterface を実装するように修正され](https://github.com/symfony/symfony/commit/beda03ba96b847fb6bcf2d7aed2893c978ec2565)ました。
公式リポジトリは、フォーク数が 800 を超えました。
 
開発メーリングリスト
--------------------

  * [Doctrine のエンティティを JSON にシリアライズする標準的な方法](https://groups.google.com/forum/#!topic/symfony-devs/GIOXA3GFspQ)
  * [\[Security\] トークンを永続化する ContextListener のロジック](https://groups.google.com/forum/#!topic/symfony-devs/ojLvh0WUbfo)

Symfony2 開発ハイライト
-----------------------

[Master branch changelog](http://github.com/symfony/symfony/commits/master):

  * [8f15794](http://github.com/symfony/symfony/commit/8f157942740b61a140997c3e2bfcb8326606e3b7 "8f157942740b61a140997c3e2bfcb8326606e3b7 commit on github"): moved LocaleListener and RouterListener to the HttpKernel component
  * [4539e5c](http://github.com/symfony/symfony/commit/4539e5c554e71d53ae6d4b3b48681fea60d0fd90 "4539e5c554e71d53ae6d4b3b48681fea60d0fd90 commit on github"): moved configuration of the default HTTP and HTTPS ports from RouterListener to RequestContext
  * [beda03b](http://github.com/symfony/symfony/commit/beda03ba96b847fb6bcf2d7aed2893c978ec2565 "beda03ba96b847fb6bcf2d7aed2893c978ec2565 commit on github"), [7a89d34](http://github.com/symfony/symfony/commit/7a89d34872e82fcc67efef7a709e8501351d6bac "7a89d34872e82fcc67efef7a709e8501351d6bac commit on github"): \[HttpKernel\] updated all HttpKernel event listeners to implement EventSubscriberInterface
  * [6e4269f](http://github.com/symfony/symfony/commit/6e4269f9eb944c879c563b701cbf203ac3a48056 "6e4269f9eb944c879c563b701cbf203ac3a48056 commit on github"), [3aa7582](http://github.com/symfony/symfony/commit/3aa75828b01149a8ea6fbe18f27d1fd27f96bd35 "3aa75828b01149a8ea6fbe18f27d1fd27f96bd35 commit on github"), [a2cf023](http://github.com/symfony/symfony/commit/a2cf023da1e3bc58cd1f3acae9d186cba0aea1dc "a2cf023da1e3bc58cd1f3acae9d186cba0aea1dc commit on github"): \[Form, TwigBridge, FrameworkBundle\] added the ability to specify the translation domain
  * [73312ab](http://github.com/symfony/symfony/commit/73312ab5e9321bb586fd2e7f7503b01554875969 "73312ab5e9321bb586fd2e7f7503b01554875969 commit on github"): \[Validator\] the Type constraint now accepts the Boolean type instead of boolean
  * [cc76da1](http://github.com/symfony/symfony/commit/cc76da1144bbeb57db6faafcfd2242e055276275 "cc76da1144bbeb57db6faafcfd2242e055276275 commit on github"): \[HttpKernel\] fixed file profile storage when trying to read an empty token
  * [5b69dae](http://github.com/symfony/symfony/commit/5b69dae9c8384a3e8c0cbc1a2ec5dc4fa44d05d3 "5b69dae9c8384a3e8c0cbc1a2ec5dc4fa44d05d3 commit on github"): \[HttpKernel\] fixed profiler file storage for children
  * [3ca1ccb](http://github.com/symfony/symfony/commit/3ca1ccbf6764de5e2d48b2ddabdd2f1eb7075459 "3ca1ccbf6764de5e2d48b2ddabdd2f1eb7075459 commit on github"): \[DoctrineBridge\] removed the Xml and Yaml driver as they are now part of Doctrine
  * [976f8b1](http://github.com/symfony/symfony/commit/976f8b10fa6bf4505cab6fcec07ff1d73a281994 "976f8b10fa6bf4505cab6fcec07ff1d73a281994 commit on github"): \[HttpKernel\] moved the Timer data collector to HttpKernel
  * [08285ed](http://github.com/symfony/symfony/commit/08285edef973a0c2392503ba499d761e086c49d2 "08285edef973a0c2392503ba499d761e086c49d2 commit on github"): \[SwiftmailerBundle\] fixed email display in the web profiler when the message is not in UTF-8

[2.0 branch changelog](http://github.com/symfony/symfony/commits/2.0):

  * [2270a4d](http://github.com/symfony/symfony/commit/2270a4da5ad24fec70142301ee01935efa2e78c9 "2270a4da5ad24fec70142301ee01935efa2e78c9 commit on github"): \[Bridge, Doctrine\] added a catch for when a developer uses the EntityType with multiple=false but on a hasMany relationship
  * [00cbd39](http://github.com/symfony/symfony/commit/00cbd398135b865478fa63278e667421368525c5 "00cbd398135b865478fa63278e667421368525c5 commit on github"), [d8dfca2](http://github.com/symfony/symfony/commit/d8dfca21f2a61861f3b00114d876210171be446c "d8dfca21f2a61861f3b00114d876210171be446c commit on github"): \[BrowserKit\] fixed cookie expiry discard when attribute contains capitals
  * [9d8046e](http://github.com/symfony/symfony/commit/9d8046e40739d275de3049283fe934f5de4ae98c "9d8046e40739d275de3049283fe934f5de4ae98c commit on github"): \[Doctrine\] UniqueValidator now works with associations


