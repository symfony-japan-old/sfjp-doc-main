---
layout: default
title: A week of symfony #231 (30 May -> 5 June 2011)
---

A week of symfony #231 (30 May -> 5 June 2011)
==============================================

Symfony2 のコードベースにおける作業はほとんど完了しましたので、今週の開発活動は、主に Routing と Event コンポーネントにおいて、コードの移動、リネーム、リファクタリングと調整に集中しました。DoctrineBundle も更新され、いくつかの新しい[便利なショートカット](https://github.com/symfony/symfony/commit/28dcb3c5815351dfc37f7e32d00353493ddc3e60)が追加され、公式マニュアルに[真新しい Doctrine の章](https://github.com/symfony/symfony-docs/pull/366)が追加されました。
 
開発 ML
-------

  * [\[Symfony2\] グローバルな {_locale} パラメータ](https://groups.google.com/forum/#!topic/symfony-devs/6oxsa7whBps)
  * [Security - 動的な login_path と check_path](https://groups.google.com/forum/#!topic/symfony-devs/y3jQyPgiPWo)
  * [キャッシュを管理する](https://groups.google.com/forum/#!topic/symfony-devs/B0D3Lsga1d8)
  * [Validation のバグの可能性](https://groups.google.com/forum/#!topic/symfony-devs/tNam9yTl0U4)
  * [Assetic javascripts: js ファイルの配列を渡す方法](https://groups.google.com/forum/#!topic/symfony-devs/QolHvmbubGg)
  * [Service Container のサービスコンフィギュレーションの種類](https://groups.google.com/forum/#!topic/symfony-devs/1J-IX2W839E)

Symfony2 の開発ハイライト
-------------------------

[チェンジログ](http://github.com/symfony/symfony/commits/master):

  * [c171142](http://github.com/symfony/symfony/commit/c171142c011d77ddf80c0bd48abef875e6304f27 "c171142c011d77ddf80c0bd48abef875e6304f27 commit on github"): イベントの定数を大文字にリネームしました
  * [9b7e14d](http://github.com/symfony/symfony/commit/9b7e14dd105a902f2a5c20ecce741084a9d14096 "9b7e14dd105a902f2a5c20ecce741084a9d14096 commit on github"), [79e709c](http://github.com/symfony/symfony/commit/79e709cdc95eda6de05853365f4462babd91256b "79e709cdc95eda6de05853365f4462babd91256b commit on github"): \[Form\] コードを新しいイベントディスパッチャに変換しました
  * [d7220f0](http://github.com/symfony/symfony/commit/d7220f0c1af323fca054394035b126afb797d36d "d7220f0c1af323fca054394035b126afb797d36d commit on github"): \[Security\] イベントの名前を修正しました
  * [9698669](http://github.com/symfony/symfony/commit/9698669baa73cbc20a8bfa3428ef3b3b1b170cfe "9698669baa73cbc20a8bfa3428ef3b3b1b170cfe commit on github"): RequestAttributeInitializingListener を RouterListener に、 SessionInitializingListener を SessionListener にリネームしました
  * [4f7484b](http://github.com/symfony/symfony/commit/4f7484b946a1e7352d0acf9642413abe114c86e0 "4f7484b946a1e7352d0acf9642413abe114c86e0 commit on github"): \[HttpFoundation\] ディレクトリ作成のタイミングをディスク書き込みの直前に移動させました
  * [a2163f3](http://github.com/symfony/symfony/commit/a2163f39ffe40d1847e3cfd3340fe24d19d2e85f "a2163f39ffe40d1847e3cfd3340fe24d19d2e85f commit on github"): \[EventDispatcher\] キャッシュレイヤーを再度追加しました
  * [b61929b](http://github.com/symfony/symfony/commit/b61929bf4ab2214bc876e60184cb9c2389a75ee5 "b61929bf4ab2214bc876e60184cb9c2389a75ee5 commit on github"): \[Form\] セクションのレンダリングの間に存続すべきではない変数のスタックを修正しました
  * [9883559](http://github.com/symfony/symfony/commit/988355993a3ed89ba761e8fc12cc88940090516a "988355993a3ed89ba761e8fc12cc88940090516a commit on github"): Profiler クラスをリファクタリングしました
  * [d1ca577](http://github.com/symfony/symfony/commit/d1ca577e3f69a752de7ca5073f70d768ac576429 "d1ca577e3f69a752de7ca5073f70d768ac576429 commit on github"): Logger::getDebugLogger() はインターフェイスの一部ではないので、このメソッドを削除しました。
  * [3ca5780](http://github.com/symfony/symfony/commit/3ca57804863e0582f06eae7e1b78b1aeb7d8e741 "3ca57804863e0582f06eae7e1b78b1aeb7d8e741 commit on github"): \[HttpKernel\] NullLogger を追加しました
  * [28527c7](http://github.com/symfony/symfony/commit/28527c7c916c2cd6536e5052106a3b4d01d39062 "28527c7c916c2cd6536e5052106a3b4d01d39062 commit on github"), [7d999ac](http://github.com/symfony/symfony/commit/7d999acd0bc3fa67c08493ba9f1a8aba9c4683b0 "7d999acd0bc3fa67c08493ba9f1a8aba9c4683b0 commit on github"): よりよい一貫性のために UniversalClassLoader をリネームしました
  * [839c332](http://github.com/symfony/symfony/commit/839c332438c77c0c82d1fac85f57ef4826be7b78 "839c332438c77c0c82d1fac85f57ef4826be7b78 commit on github"): すべてのリスナークラスを共通の EventListener サブネームスペースのもとに移動させました
  * [ed4f659](http://github.com/symfony/symfony/commit/ed4f65969334113b6d080b25fbb9e019d714b65b "ed4f65969334113b6d080b25fbb9e019d714b65b commit on github"): \[SwiftmailerBundle\] ImpersonateSenderPlugin を追加しました
  * [af84cfe](http://github.com/symfony/symfony/commit/af84cfec33e2551415e0d0a7f5e60e327016b027 "af84cfec33e2551415e0d0a7f5e60e327016b027 commit on github"): \[DoctrineBundle\] doctrine:generate:entity を修正しました
  * [2642b00](http://github.com/symfony/symfony/commit/2642b0012ffce0189fc83f598052265e1d9e4a72 "2642b0012ffce0189fc83f598052265e1d9e4a72 commit on github"), [d9f5c99](http://github.com/symfony/symfony/commit/d9f5c99fabc649b7067daf6f2f69bdd86f6f715b "d9f5c99fabc649b7067daf6f2f69bdd86f6f715b commit on github"): \[Templating\] アセットヘルパーとパッケージを作り替えました。バージョンをパスに適用するコンフィギュレーションの変更可能なフォーマット文字列のサポートを追加しました (デフォルトは '%s?%s')
  * [cb22ccc](http://github.com/symfony/symfony/commit/cb22ccc516d07069f0f588c825897ef2d3cd9982 "cb22ccc516d07069f0f588c825897ef2d3cd9982 commit on github"): \[Form\] フィールドラベルに属性を追加する機能が欠落していたので追加しました
  * [3e68eb6](http://github.com/symfony/symfony/commit/3e68eb61a50de6c279238cb4a8bc79147f34d076 "3e68eb61a50de6c279238cb4a8bc79147f34d076 commit on github"): \[AsseticBundle\] アセット入力においてパラメータのサポートを追加しました
  * [3d532f8](http://github.com/symfony/symfony/commit/3d532f806a0b5cef9c8126438e90c57713d549e0 "3d532f806a0b5cef9c8126438e90c57713d549e0 commit on github"): \[FrameworkBundle\] getProfiler() メソッドを getProfile() にリネームしました (このメソッドが Profile のインスタンスを返すようになったからです)
  * [1452164](http://github.com/symfony/symfony/commit/145216477b829505acf040aca2581c432934fb24 "145216477b829505acf040aca2581c432934fb24 commit on github"): \[AsseticBundle\] cssmin フィルタサービスのスキーマが欠落していたので追加しました
  * [d2fa6c3](http://github.com/symfony/symfony/commit/d2fa6c3e4ee958f6997d479ebe70c80dfc60ccf0 "d2fa6c3e4ee958f6997d479ebe70c80dfc60ccf0 commit on github"), [9ad3185](http://github.com/symfony/symfony/commit/9ad318546da24c25b924ced249c3163af28b7eec "9ad318546da24c25b924ced249c3163af28b7eec commit on github"): \[SecurityBundle\] remember_me の user_providers オプションを追加しました
  * [6f8871d](http://github.com/symfony/symfony/commit/6f8871d2d74b98cf6d894f1aac0e921be0111584 "6f8871d2d74b98cf6d894f1aac0e921be0111584 commit on github"): \[SecurityBundle\] チェックパスのバリデーションを追加しました
  * [597a646](http://github.com/symfony/symfony/commit/597a646347fff5bf2090fbe97096dc47ac25c6fd "597a646347fff5bf2090fbe97096dc47ac25c6fd commit on github"): ブロックをフォーマットするときに mb_detect_encoding を追加しました (mb_internal_encoding が適切にセットされていないときに役立ちます)
  * [28dcb3c](http://github.com/symfony/symfony/commit/28dcb3c5815351dfc37f7e32d00353493ddc3e60 "28dcb3c5815351dfc37f7e32d00353493ddc3e60 commit on github"), [1ac4675](http://github.com/symfony/symfony/commit/1ac4675e32d9f9ac3e595ba020ec7068a48f92c7 "1ac4675e32d9f9ac3e595ba020ec7068a48f92c7 commit on github"), [172c956](http://github.com/symfony/symfony/commit/172c956b73a1f8314f7085274f37c1bee8614047 "172c956b73a1f8314f7085274f37c1bee8614047 commit on github"): \[FrameworkBundle, DoctrineBundle\] ショートカットメソッド: Controller::getDoctrine() と Registry::getRepository() を追加しました。
  * [df81296](http://github.com/symfony/symfony/commit/df81296443d62db7d39c771253d95da25fe62e3f "df81296443d62db7d39c771253d95da25fe62e3f commit on github"): \[Routing\] デフォルトの値が null であるときの生成を修正しました
  * [611a4a2](http://github.com/symfony/symfony/commit/611a4a212caeb48d39acd3fc3622baf9e4966df1 "611a4a212caeb48d39acd3fc3622baf9e4966df1 commit on github"): \[FrameworkBundle\] サービスが任意のイベントに対してカーネルリスナーを複数回登録できるようにしました
  * [c62b230](http://github.com/symfony/symfony/commit/c62b2309cf1cc2fab448d754caf6c57c10ff84d3 "c62b2309cf1cc2fab448d754caf6c57c10ff84d3 commit on github"): \[FrameworkBundle\] Security コンポーネントによって発せられたリダイレクトに対する WDT を修正しました (注：ウォッチドッグ・タイマーはプログラムが正常に動いているか監視する機能)
  * [7780c4d](http://github.com/symfony/symfony/commit/7780c4deda80a2680586c6e3da2fd06b337bcdc6 "7780c4deda80a2680586c6e3da2fd06b337bcdc6 commit on github"): \[HttpKernel\] RFC2616 により Request メソッドが HEAD であるときの Response のコンテントを削除しました 
  * [9eae7e5](http://github.com/symfony/symfony/commit/9eae7e54caefd73ea72d0b8b88e537e629c90b4b "9eae7e54caefd73ea72d0b8b88e537e629c90b4b commit on github"): \[Routing\] ダンパーの Apache ルールにおける不要なコードを削除しました
  * [f9ffdf5](http://github.com/symfony/symfony/commit/f9ffdf5b3375ff3df5a4c9fc2236cd8b2f23b975 "f9ffdf5b3375ff3df5a4c9fc2236cd8b2f23b975 commit on github"): \[Routing\] HEAD メソッドの適切なサポートを追加しました
  * [c561f4f](http://github.com/symfony/symfony/commit/c561f4f0c0750e49ed21ed4546f2f4b6ce15f5e9 "c561f4f0c0750e49ed21ed4546f2f4b6ce15f5e9 commit on github"): \[Routing\] つねに HTTP メソッドの名前が大文字になるように変更しました (HttpFoundation/Request との一貫性を保つため)
  * [c72537d](http://github.com/symfony/symfony/commit/c72537da6b906d9d7599a0ce00aead597804d0c7 "c72537da6b906d9d7599a0ce00aead597804d0c7 commit on github"): \[Routing\] プレフィックスに変数が含まれるときにルートのマッチングを修正しました
  * [8457bfa](http://github.com/symfony/symfony/commit/8457bfa365483a589d0cc685a99bc61155395418 "8457bfa365483a589d0cc685a99bc61155395418 commit on github"): \[FrameworkBundle\] fixed _locale management in core.request において _locale の管理方法を修正しました
  * [8c0e502](http://github.com/symfony/symfony/commit/8c0e5029a0cea711453cb6da3e6bfe8b3b5d4470 "8c0e5029a0cea711453cb6da3e6bfe8b3b5d4470 commit on github"): \[DoctrineBundle\] 生成ファイルの拡張子を修正しました
  * [a98046d](http://github.com/symfony/symfony/commit/a98046dd4456042e54b73164eea4fe6e25290238 "a98046dd4456042e54b73164eea4fe6e25290238 commit on github"): \[Config\] 循環参照に対するガードを追加しました
