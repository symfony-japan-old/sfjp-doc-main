---
layout: default
title: A week of symfony #234 (20->26 June 2011)
---

A week of symfony #234 (20->26 June 2011)
=========================================

Symfony2は今週新しい[対話型ジェネレータ](http://symfony.com/blog/symfony2-getting-easier-interactive-generators)を導入しました。このツールによって開発効率が大いに向上するでしょう。加えて、[Symfony2のための新しいML](https://groups.google.com/forum/#!forum/symfony2)が発表されました。最後に、[最初のリリース候補バージョン](http://symfony.com/blog/symfony2-2-0-rc1-released)がリリースされ、Symfony2コンポーネントは[新しいSymfony2 PEARチャンネル](http://symfony.com/blog/symfony2-pear-channel)で利用可能になりました。
 
開発ML
------------------------

  * [\[Sf2\] フォーム描画のRFC](https://groups.google.com/forum/#!topic/symfony-devs/F3VBKLpIBUU)
  * [\[Sf2\]\[Form\] PHPテーマ](https://groups.google.com/forum/#!topic/symfony-devs/mz8TH-EWtRE)
  * [Symfony2と複数のアプリケーション](https://groups.google.com/forum/#!topic/symfony-devs/yneojUuFiqw)
  * [サービスとしてのコントローラの再考](https://groups.google.com/forum/#!topic/symfony-devs/oqWdklH1j3E)

Symfony2開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [01ecaa4](http://github.com/symfony/symfony/commit/01ecaa45031ce83c80f75873f8e2374bf437567c "01ecaa45031ce83c80f75873f8e2374bf437567c commit on github"): \[Config\] FileLoaderImportExceptionをFileLoaderLoadExceptionにリネームし、いくつかの\InvalidArgumentExceptionを新しい例外クラスで置換
  * [2e1747b](http://github.com/symfony/symfony/commit/2e1747bf760e01673db5493ae20f240e5a18b05d "2e1747bf760e01673db5493ae20f240e5a18b05d commit on github"): エラー時やデバッグメッセージのリソースについての情報を追加
  * [8b168a1](http://github.com/symfony/symfony/commit/8b168a142b07992e8261d66bfb0e732fc5824ee1 "8b168a142b07992e8261d66bfb0e732fc5824ee1 commit on github"): \[HttpKernel\] HttpKernel::varToString()を更新
  * [e43fb98](http://github.com/symfony/symfony/commit/e43fb989e320e29045e1a8a1c9b2dfa33d0e4d28 "e43fb989e320e29045e1a8a1c9b2dfa33d0e4d28 commit on github"): \[Form, TwigBridge\] FormExtension::render()を再帰的に呼び出せるように変更
  * [e09ae3f](http://github.com/symfony/symfony/commit/e09ae3f6a2ddf0b1b0ae24cf104902acf6a278c8 "e09ae3f6a2ddf0b1b0ae24cf104902acf6a278c8 commit on github"): \[Form, FrameworkBundle\] FormHelper::renderSection()を再帰的に呼び出せるように変更し、FormHelper::renderBlock()を導入
  * [f729c6b](http://github.com/symfony/symfony/commit/f729c6ba93397f918dc1b0661fca5f268782be53 "f729c6ba93397f918dc1b0661fca5f268782be53 commit on github"), [2c1108c](http://github.com/symfony/symfony/commit/2c1108ce6b987d804aaeeab30932340fc90b5841 "2c1108ce6b987d804aaeeab30932340fc90b5841 commit on github"): \[Form\] 列を描画するときにラベルとウィジェットオプションを上書きできるように修正 (reverted)
  * [8670995](http://github.com/symfony/symfony/commit/867099557465236fe18abcc3ce128897af339067 "867099557465236fe18abcc3ce128897af339067 commit on github"): \[Form\] 描画するブロックが既出の場合の描画を改善
  * [cdd39ac](http://github.com/symfony/symfony/commit/cdd39ac3e2d593dd36da498da601c9a625c317f8 "cdd39ac3e2d593dd36da498da601c9a625c317f8 commit on github"), [7783a05](http://github.com/symfony/symfony/commit/7783a050c21fddd188d111e216d87d8d1a6cff61 "7783a050c21fddd188d111e216d87d8d1a6cff61 commit on github"): DateTimeType、DateType、TimeTypeに'empty_value'がセット出来るように修正
  * [c827faf](http://github.com/symfony/symfony/commit/c827faf694041edabbf94c510e2c32c23e20c770 "c827faf694041edabbf94c510e2c32c23e20c770 commit on github"), [159fc0e](http://github.com/symfony/symfony/commit/159fc0edf0dfd9d76c27cb65fbd0934863f7e8e5 "159fc0edf0dfd9d76c27cb65fbd0934863f7e8e5 commit on github"): \[Validator\] IDNとカスタムTLDのサポートを追加
  * [25e99e8](http://github.com/symfony/symfony/commit/25e99e894b84958026f3da4dc9766130d49f1f88 "25e99e894b84958026f3da4dc9766130d49f1f88 commit on github"): CommandをContainerAwareCommandにリネーム
  * [6ab11eb](http://github.com/symfony/symfony/commit/6ab11eb1cec767509e37cc50d240169307643db0 "6ab11eb1cec767509e37cc50d240169307643db0 commit on github"): \[Console\] ApplicationからCommandを分離
  * [406c8d8](http://github.com/symfony/symfony/commit/406c8d81efb13de8c83de7f473ee0ecf9bbe3d44 "406c8d81efb13de8c83de7f473ee0ecf9bbe3d44 commit on github"), [abd60ac](http://github.com/symfony/symfony/commit/abd60ac3454b6f03504370c8ff89242dfd56f608 "abd60ac3454b6f03504370c8ff89242dfd56f608 commit on github"), [f315ad9](http://github.com/symfony/symfony/commit/f315ad950e8216c19491917db5c549d8994aa558 "f315ad950e8216c19491917db5c549d8994aa558 commit on github"), [e272d56](http://github.com/symfony/symfony/commit/e272d569130d0a7237faceb6ab461741ed36ed0c "e272d569130d0a7237faceb6ab461741ed36ed0c commit on github"): \[WebProfilerBundle\] プロファイラツールバーを微修正
  * [7af003b](http://github.com/symfony/symfony/commit/7af003b753fd367248112cdbe4c6572ed45bc51e "7af003b753fd367248112cdbe4c6572ed45bc51e commit on github"), [37521b6](http://github.com/symfony/symfony/commit/37521b6fd71b3d12d8e5d035075e3e71982a3f30 "37521b6fd71b3d12d8e5d035075e3e71982a3f30 commit on github"), [84e87c6](http://github.com/symfony/symfony/commit/84e87c65cccadef5ec117c8c24d0e7b18c1c2b95 "84e87c65cccadef5ec117c8c24d0e7b18c1c2b95 commit on github"): \[HttpFoundation\] レスポンス本文に文字列化可能なオブジェクトや数値を許可するように修正し、テストを追加
  * [edbdf7b](http://github.com/symfony/symfony/commit/edbdf7b154d0ed9ff5b34794f66fa89c59ed290e "edbdf7b154d0ed9ff5b34794f66fa89c59ed290e commit on github"): kernel.listenerをkernel.event_listenerにリネーム (doctrine.event_listenerとより一貫性を保つために)
  * [7350109](http://github.com/symfony/symfony/commit/7350109f6e0a486d13e49f9e1ba2efcd5f54bc1f "7350109f6e0a486d13e49f9e1ba2efcd5f54bc1f commit on github"): core.* eventsをkernel.*に、CoreEventsをKernelEventsにリネーム
  * [4620700](http://github.com/symfony/symfony/commit/462070058a8b9fd1bc355505c05a0f530baad3a4 "462070058a8b9fd1bc355505c05a0f530baad3a4 commit on github"), [1c36d5a](http://github.com/symfony/symfony/commit/1c36d5a5298b3c311f08f4348d9c4675733bb342 "1c36d5a5298b3c311f08f4348d9c4675733bb342 commit on github"): \[Validator\] アノテーションでのconstraintsの認識方法を変更
  * [2d13129](http://github.com/symfony/symfony/commit/2d13129e41b5b8ba0df8edecf5b24caadd4e9bc0 "2d13129e41b5b8ba0df8edecf5b24caadd4e9bc0 commit on github"): \[DoctrineBundle\] Doctrineプロキシのためのオートローダを追加
  * [f39ce67](http://github.com/symfony/symfony/commit/f39ce6709dbbafd116c661d67fc03ca214da07f2 "f39ce6709dbbafd116c661d67fc03ca214da07f2 commit on github"): \[Form, FrameworkBundle\] PHPテーマ
  * [1cb2129](http://github.com/symfony/symfony/commit/1cb212977226befd0cd543f18ecfe60050373022 "1cb212977226befd0cd543f18ecfe60050373022 commit on github"): \[FrameworkBundle, Form\] FormHelper::lookupTemplate()のキャッシュを追加
  * [a43fad4](http://github.com/symfony/symfony/commit/a43fad409b58e4d6e67252354499d0a5c6fcf52b "a43fad409b58e4d6e67252354499d0a5c6fcf52b commit on github"): \[Form\] 描画のユニットテストを改善
  * [5d46e63](http://github.com/symfony/symfony/commit/5d46e630892034d09788d81574fc3b94e954511d "5d46e630892034d09788d81574fc3b94e954511d commit on github"): \[Form\] FormHelper設定を追加
  * [7117f41](http://github.com/symfony/symfony/commit/7117f41b387f7c93b30e56b4684f34f930bd3ab6 "7117f41b387f7c93b30e56b4684f34f930bd3ab6 commit on github"): \[FrameworkBundle\] init:bundleを削除し (replaced by the generator bundle in Symfony SE)
  * [b91bd78](http://github.com/symfony/symfony/commit/b91bd78ddb495d4dcf5f3d843af3b8a079aba76c "b91bd78ddb495d4dcf5f3d843af3b8a079aba76c commit on github"): \[DoctrineBundle\] generate:doctrine:entityを削除
  * [1436d8d](http://github.com/symfony/symfony/commit/1436d8dab76ba8c16da0328d05af78fd31ac40b8 "1436d8dab76ba8c16da0328d05af78fd31ac40b8 commit on github"): \[Security\] HttpUtilsクラスをリクエストとレスポンスに関連するロジックの管理のために追加。この変更で{_locale}ハックする必要がなくなった。
  * [bda4129](http://github.com/symfony/symfony/commit/bda412932be85728fb96635f80343e509f6a1bca "bda412932be85728fb96635f80343e509f6a1bca commit on github"): run()が完全にノンブロッキングになるように修正し、潜在的な他の問題も修正
  * [d49e306](http://github.com/symfony/symfony/commit/d49e306b9b4fe0f26db8775fd29da650b89e4f85 "d49e306b9b4fe0f26db8775fd29da650b89e4f85 commit on github"): \[DomCrawler\] リンクに関連するクエリ文字列の扱いを修正
  * [6de97c5](http://github.com/symfony/symfony/commit/6de97c56e18f2c53b43b18a12006db7c72aa714c "6de97c56e18f2c53b43b18a12006db7c72aa714c commit on github"): \[Form\] からの値が選択肢に追加されたときに男泥するためのアルゴリズムを必要とするように修正 
  * [8ccebc4](http://github.com/symfony/symfony/commit/8ccebc463114a850e08d634098aeaf49ad5c3eee "8ccebc463114a850e08d634098aeaf49ad5c3eee commit on github"): \[DomCrawler\] アンカーのためのLink::getUri()メソッドを修正
  * [4824926](http://github.com/symfony/symfony/commit/482492625dea0752fef82650138dffe237e90966 "482492625dea0752fef82650138dffe237e90966 commit on github"): \[Validator\] True と False の validator が 複数の値を許可するように制限
  * [05c9906](http://github.com/symfony/symfony/commit/05c990628b4487114fee5f2955ae27193a29de97 "05c990628b4487114fee5f2955ae27193a29de97 commit on github"): \[HttpKernel\] 304レスポンスの内容ががキャッシュに入らないように抑制
  * [ad5d2c1](http://github.com/symfony/symfony/commit/ad5d2c13e11abba361267ed78df7182e5597354a "ad5d2c13e11abba361267ed78df7182e5597354a commit on github"), [17b41b2](http://github.com/symfony/symfony/commit/17b41b2c510a7e9d47c53c77920252cd16e976a2 "17b41b2c510a7e9d47c53c77920252cd16e976a2 commit on github"), [7bc19f9](http://github.com/symfony/symfony/commit/7bc19f96755e9ad70b8a8946fd648132c6edeff7 "7bc19f96755e9ad70b8a8946fd648132c6edeff7 commit on github"): TimeType と DateTimeType 拡張が single_text のようなフォーム描画できるように修正
  * [2cf7136](http://github.com/symfony/symfony/commit/2cf7136e537d3c60d32bbe72f48730cf610c597d "2cf7136e537d3c60d32bbe72f48730cf610c597d commit on github"): \[FrameworkBundle, Form\] PHP テンプレートの選択ウィジェットを微修正
  * [46680d4](http://github.com/symfony/symfony/commit/46680d4565b4b675dc73aa5dca1ec3dddbda6b97 "46680d4565b4b675dc73aa5dca1ec3dddbda6b97 commit on github"): \[FrameworkBundle\] Doctrine Common 2.1に切り戻し
  * [e80ce57](http://github.com/symfony/symfony/commit/e80ce57935290f412c787725d06d8e1cae94da65 "e80ce57935290f412c787725d06d8e1cae94da65 commit on github"): \[HttpFoundation\] デフォルトでREQUEST_TIMEを追加
  * [920a209](http://github.com/symfony/symfony/commit/920a209bbc305c9addd01908b972b2b70bb7c10f "920a209bbc305c9addd01908b972b2b70bb7c10f commit on github"), [1dfb637](http://github.com/symfony/symfony/commit/1dfb637858639fa225daa8332b33c390717035f5 "1dfb637858639fa225daa8332b33c390717035f5 commit on github"), [cb3ad8b](http://github.com/symfony/symfony/commit/cb3ad8bb79a01fefbfab3cebd29eb7b655efcb28 "cb3ad8bb79a01fefbfab3cebd29eb7b655efcb28 commit on github"), [e43cd20](http://github.com/symfony/symfony/commit/e43cd206b061447ea7e1381216a11bc49f3e3c44 "e43cd206b061447ea7e1381216a11bc49f3e3c44 commit on github"): \[Security\] http basicの修正 (reverted)
  * [600cd41](http://github.com/symfony/symfony/commit/600cd415e6f413e983a71cc3bcd6241b0105a7ee "600cd415e6f413e983a71cc3bcd6241b0105a7ee commit on github"), [9cd1590](http://github.com/symfony/symfony/commit/9cd15908f374d274c671157289d2f5086a5c236e "9cd15908f374d274c671157289d2f5086a5c236e commit on github"): \[FrameworkBundle\] cache:clearコマンドの修正
  * [a19c336](http://github.com/symfony/symfony/commit/a19c336c180ab05f309bee0630a70f68d48e1183 "a19c336c180ab05f309bee0630a70f68d48e1183 commit on github"): \[WebProfilerBundle\] WDTが無効の時のプロファイラを修正
