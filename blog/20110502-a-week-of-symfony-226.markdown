---
layout: default
title: A week of symfony #226 (25 April -> 1 May 2011)
---

A week of symfony #226 (25 April -> 1 May 2011)
===============================================

Symfony2は今週、[最初のベータ版](http://symfony.com/blog/symfony2-beta1-available)を公開しました。. Doctrineは[設定の簡略化](http://symfony.com/blog/symfony2-getting-easier)なども実装され、最も活動の多かったバンドルでした。さらに、Symfony2は2つの注目すべきマイルストーンに到達しました。１つは[レポジトリのウォッチャーが2000人](https://github.com/symfony/symfony/watchers)を超えたこと、そしてもう１つは[プルリクエストが700件](https://github.com/symfony/symfony/pulls)を超えたことです。
 
開発ML
------------------------

  * [\[Symfony2\] パスレベルのキャッシュコントロールリスナー](https://groups.google.com/forum/#!topic/symfony-devs/Np0W_hDgAoQ)
  * [\[Symfony2\] RequestとResponseのパブリックプロパティ](https://groups.google.com/forum/#!topic/symfony-devs/CiJuSno85_8)
  * [\[Symfony2\] Form Frameworkのフィードバックを考える](https://groups.google.com/forum/#!topic/symfony-devs/8eEsQZ9kyeY)
  * [Symfony2は公式のAdminジェネレータを持つだろうか？](https://groups.google.com/forum/#!topic/symfony-devs/n14GBnPy1tg)
  * [\[Symfony2\] doctrine:generate:repositoriesコマンドを消す?](https://groups.google.com/forum/#!topic/symfony-devs/E7ZtxLgW1_M)
  * [テンプレート文字列の抽出](https://groups.google.com/forum/#!topic/symfony-devs/xqKHsgMnEz0)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [7c95bda](http://github.com/symfony/symfony/commit/7c95bda751e7b54d545f4be81c09f55408bef46f "7c95bda751e7b54d545f4be81c09f55408bef46f commit on github"): \[Routing\] ルートコンパイラの簡略化
  * [d948361](http://github.com/symfony/symfony/commit/d948361ed6e5497729896688b26ccf30f9802a29 "d948361ed6e5497729896688b26ccf30f9802a29 commit on github"): \[AsseticBundle\] コンパスフィルタのための設定の追加
  * [f372874](http://github.com/symfony/symfony/commit/f3728744b497a60552aca686d58b5453a63fe031 "f3728744b497a60552aca686d58b5453a63fe031 commit on github"): \[AsseticBundle\] Twig関数のサポートを追加
  * [944a980](http://github.com/symfony/symfony/commit/944a98086ea240270e131e93034416fa17d96df2 "944a98086ea240270e131e93034416fa17d96df2 commit on github"): \[Routing\] PHPルートダンパーの最適化
  * [3bca4b7](http://github.com/symfony/symfony/commit/3bca4b73e52a849198f3681b90ec0b476cadc48e "3bca4b73e52a849198f3681b90ec0b476cadc48e commit on github"): \[MonologBundle\] 何らかのハンドラが登録されたらファイルをコンパイルするだけ
  * [f4d1196](http://github.com/symfony/symfony/commit/f4d11966665fcccaaa188af26e88f2d51460398a "f4d11966665fcccaaa188af26e88f2d51460398a commit on github"): \[MonologBundle\] FirePHPHandlerサポートの追加
  * [713e8c2](http://github.com/symfony/symfony/commit/713e8c26a6fcbb96054397d3ee6a2c3866236003 "713e8c26a6fcbb96054397d3ee6a2c3866236003 commit on github"), [f9f02a9](http://github.com/symfony/symfony/commit/f9f02a90471cc55d73ddeef9c4d4403e90ac26be "f9f02a90471cc55d73ddeef9c4d4403e90ac26be commit on github"), [05698f6](http://github.com/symfony/symfony/commit/05698f66a2ba9f83d1b3223eb12fe2bbe76296b6 "05698f66a2ba9f83d1b3223eb12fe2bbe76296b6 commit on github"), [88e78e6](http://github.com/symfony/symfony/commit/88e78e6f44636ee98c48ff3453fb3da3b9813ad3 "88e78e6f44636ee98c48ff3453fb3da3b9813ad3 commit on github"), [d506a55](http://github.com/symfony/symfony/commit/d506a55b40f53103f6759e09f645b37472e35139 "d506a55b40f53103f6759e09f645b37472e35139 commit on github"): 冗長だったり未使用だったりするパラメータや引数の削除
  * [45dd5f3](http://github.com/symfony/symfony/commit/45dd5f33ed4b6ab3a772cc8745929f243fe86383 "45dd5f33ed4b6ab3a772cc8745929f243fe86383 commit on github"): \[FrameworkBundle\] バリデーションメッセージにルクセンブルク後訳を追加
  * [246ad1b](http://github.com/symfony/symfony/commit/246ad1b03f8c10e8e072de9ba4bf37aa4b786a4c "246ad1b03f8c10e8e072de9ba4bf37aa4b786a4c commit on github"): \[FrameworkBundle\] バリデーションメッセージにドイツ語訳を追加
  * [7a7b448](http://github.com/symfony/symfony/commit/7a7b448680a0a8321f3f4ab0840b4004aea9a57d "7a7b448680a0a8321f3f4ab0840b4004aea9a57d commit on github"): \[HttpKernel\] 暗黙的に読み込まれるBundleInterface::getContainerExtension()を追加
  * [a005796](http://github.com/symfony/symfony/commit/a005796d3b55b05a59cd86d49180a9283f4093c5 "a005796d3b55b05a59cd86d49180a9283f4093c5 commit on github"): \[AsseticBundle\] 実行時にuse_controllerをチェックする実行時フィルタ関数をラップするnode visitorを追加
  * [035afc1](http://github.com/symfony/symfony/commit/035afc1f4e9dccab7d51614d3a55cfd70052e365 "035afc1f4e9dccab7d51614d3a55cfd70052e365 commit on github"): \[Routing\] Routingマッチングアルゴリズムの回帰バグを修正
  * [f9c300e](http://github.com/symfony/symfony/commit/f9c300e8db3d2edf65481884243133f1e34b5f6c "f9c300e8db3d2edf65481884243133f1e34b5f6c commit on github"): \[AsseticBundle\] use_controllerが有効時に共通イメージリクエストの書式を追加するためのリスナーを追加
  * [fefee0d](http://github.com/symfony/symfony/commit/fefee0d5e5b3d2f497b491c2b3be21f25ff77bae "fefee0d5e5b3d2f497b491c2b3be21f25ff77bae commit on github"): \[Routing\] オプション変数の値が0の時のURL生成を修正
  * [dacfa63](http://github.com/symfony/symfony/commit/dacfa633f669e1bc5a915480636df95018060dde "dacfa633f669e1bc5a915480636df95018060dde commit on github"): \[FrameworkBundle\] バリデーションメッセージにカタロニア語訳を追加
  * [e68f8f4](http://github.com/symfony/symfony/commit/e68f8f40b9d00db67c4cb8ca23fdd9b907109925 "e68f8f40b9d00db67c4cb8ca23fdd9b907109925 commit on github"): \[DoctrineBundle\] DIC クラスパラメータの名前変更 (他のバンドルの規則に従って、_classの代わりに.ckassで終わるようにした)
  * [175f944](http://github.com/symfony/symfony/commit/175f944f93c8d515627173a5fea792da956198bf "175f944f93c8d515627173a5fea792da956198bf commit on github"): \[DependencyInjection\] 存在しないパタメータが使われたことを示すNonExistentParameterExceptionを追加
  * [98e70f0](http://github.com/symfony/symfony/commit/98e70f0963b4709d89aeba64646ce328a45c7483 "98e70f0963b4709d89aeba64646ce328a45c7483 commit on github"): \[Routing\] ルートコレクションは/で始まらなければならず、一方で/で終わらなくても良い
  * [e2741ce](http://github.com/symfony/symfony/commit/e2741cefc464d3c9f17f971eb3431771849cea31 "e2741cefc464d3c9f17f971eb3431771849cea31 commit on github"): \[Process\] ExecutableFinderが実行可能なものが見つからなかったときに、例外を投げる代わりにfalseを返すよう変更
  * [97f66e9](http://github.com/symfony/symfony/commit/97f66e93ac78a2f775c67ff38bb362b1e65da1d8 "97f66e93ac78a2f775c67ff38bb362b1e65da1d8 commit on github"): \[HttpKernel\] 標準拡張のエイリアス規約のチェックを追加
  * [5dc1a9b](http://github.com/symfony/symfony/commit/5dc1a9bb587bea497ad07d76bd697b14a400525d "5dc1a9bb587bea497ad07d76bd697b14a400525d commit on github"): \[Process\] 標準で実行可能なものに対するオプション引数の追加
  * [aa3ec50](http://github.com/symfony/symfony/commit/aa3ec504ae1717d95e00b341a2597a5a006ffc53 "aa3ec504ae1717d95e00b341a2597a5a006ffc53 commit on github"): コアのどこにも使われていない機能なのでFile::getWebPath()を削除
  * [854fbd7](http://github.com/symfony/symfony/commit/854fbd7f68ce57b60c84340201ee704c707b5c34 "854fbd7f68ce57b60c84340201ee704c707b5c34 commit on github"): \[HttpFoundation\] ファイルパス内で..が使われていないことを保証するためにリアルパスを使用
  * [5bb9da4](http://github.com/symfony/symfony/commit/5bb9da4b6df5a4e7e6b72a2aeccf04955c00f7b0 "5bb9da4b6df5a4e7e6b72a2aeccf04955c00f7b0 commit on github"): \[HttpFoundation\] getDefaultExtension()をguessExtension()に名前変更 (拡張が推測できない時にnullを返す)
  * [00bfd10](http://github.com/symfony/symfony/commit/00bfd10ca95cdd4ce47473af2b52384180affb6d "00bfd10ca95cdd4ce47473af2b52384180affb6d commit on github"): \[HttpFoundation\] File管理をより安全にするためにリファクタリング
  * [35a3244](http://github.com/symfony/symfony/commit/35a32440c79ea56c270c43ccf94d1c41d3276d84 "35a32440c79ea56c270c43ccf94d1c41d3276d84 commit on github"): \[DoctrineBundle\] DBAL定義テンプレートを抽象的な定義に変換
  * [aab56fa](http://github.com/symfony/symfony/commit/aab56fa91eb06dcc489f09701d2c953be0a00a7d "aab56fa91eb06dcc489f09701d2c953be0a00a7d commit on github"): \[DoctrineBundle\] もう何個か定義を抽象的な定義に移行
  * [55f9e6f](http://github.com/symfony/symfony/commit/55f9e6fb9928b95420fd330b17145972c071a00b "55f9e6fb9928b95420fd330b17145972c071a00b commit on github"): \[DoctrineBundle\] Doctrineに関する問題をより分かりやすくするために様々な例外に手を加えた
  * [03511de](http://github.com/symfony/symfony/commit/03511dea5c28336b5bba3481eb9d1dab4b0aaa76 "03511dea5c28336b5bba3481eb9d1dab4b0aaa76 commit on github"): \[DoctrineBundle\] DBALを設定しないで定義できる可能性を排除
  * [e63c2e2](http://github.com/symfony/symfony/commit/e63c2e2315d749064712a30768f8b85c855c41b2 "e63c2e2315d749064712a30768f8b85c855c41b2 commit on github"): \[DoctrineBundle\] ほとんどのユーザーは単一のDB接続しか使わないだろうから、単一のDBAL接続を定義するのをより簡単にできるように戻した
  * [059104a](http://github.com/symfony/symfony/commit/059104a9e76b52357ec03391a1f98ba5f6a57e88 "059104a9e76b52357ec03391a1f98ba5f6a57e88 commit on github"): \[DoctrineBundle\] 短い文法で単一のエンティティマネージャを定義できるように戻した (前のコミットと同じ理由)
  * [b6a9935](http://github.com/symfony/symfony/commit/b6a9935314d4a8c2b43dfbeb729a78f41cdeac59 "b6a9935314d4a8c2b43dfbeb729a78f41cdeac59 commit on github"): \[Serializer / XmlEncoder\] ルート要素内の属性が抽出できるようにデコレータを修正
  * [dc85727](http://github.com/symfony/symfony/commit/dc85727b5aade5a5e9e817ab882226da06a4e598 "dc85727b5aade5a5e9e817ab882226da06a4e598 commit on github"), [c752429](http://github.com/symfony/symfony/commit/c752429d7cb63c74673e576b357a1069d962db3b "c752429d7cb63c74673e576b357a1069d962db3b commit on github"), [6431881](http://github.com/symfony/symfony/commit/6431881754dc5043c4c434177f97f1d4d31f1f31 "6431881754dc5043c4c434177f97f1d4d31f1f31 commit on github"), [8b85458](http://github.com/symfony/symfony/commit/8b8545895f52da456b249416c9d8677710bfeafa "8b8545895f52da456b249416c9d8677710bfeafa commit on github"): \[DoctrineBundle\] Symfonyが有効なバンドル全てを登録できるように自動マッピングオプションを追加。大抵の場合すべてのバンドルをマッピングしたいと思うが、それは手動でやるにはちょっと面倒な作業だ。
  * [4fb1035](http://github.com/symfony/symfony/commit/4fb1035578f0e475673c1d1b7ae489a1447186e7 "4fb1035578f0e475673c1d1b7ae489a1447186e7 commit on github"): 識別子が文字列の時のDoctrineのEntityTypeを修正
  * [77f9daf](http://github.com/symfony/symfony/commit/77f9daf37450af3a7cff2431fd5d2d5a5d4ab22f "77f9daf37450af3a7cff2431fd5d2d5a5d4ab22f commit on github"): \[HttpKernel\] バンドルのベース名にbundleという文字を持てるように修正
  * [2291af4](http://github.com/symfony/symfony/commit/2291af41c527af635f2b9161e16c91ff7cb08d0b "2291af41c527af635f2b9161e16c91ff7cb08d0b commit on github"): intlをインストールしていない場合にもSymfonyのユニットテストができるようにオートローダにLocaleスタブを追加
  * [e72f1a9](http://github.com/symfony/symfony/commit/e72f1a98737b8b444d0c4738b0aedab084a1a9d5 "e72f1a98737b8b444d0c4738b0aedab084a1a9d5 commit on github"): CSRF、一時ストレージやおそらくもっと他のものなどを設定するためのグローバル秘密設定を追加
  * [05f1481](http://github.com/symfony/symfony/commit/05f1481c6a22b531ddc049ef6b63b8827c4e19cd "05f1481c6a22b531ddc049ef6b63b8827c4e19cd commit on github"): \[Form\] CSRFフィールド名を設定したりCSRF機能を完全に無効化したりできるような設定を追加
  * [509f3dd](http://github.com/symfony/symfony/commit/509f3dd45424d77afddc47591e8cd149eb4a9790 "509f3dd45424d77afddc47591e8cd149eb4a9790 commit on github"): テンプレートがrender_widget()を通過してしまう可能性を排除 (Twig関数を呼びつつプレーンなHTMLを使うか、マクロを作成する)
  * [3fe385e](http://github.com/symfony/symfony/commit/3fe385e4fba4b167b0925defc062c4a0f977051d "3fe385e4fba4b167b0925defc062c4a0f977051d commit on github"): オートローダのマップ機能を削除 (この機能はフレームワークをより複雑にしていたが、coreでは使っていなかった)
  * [4cbc33a](http://github.com/symfony/symfony/commit/4cbc33a7859ca5dabc2063959a09cef22044ca96 "4cbc33a7859ca5dabc2063959a09cef22044ca96 commit on github"): コンパイル済みクラスの自動ローディングを削除 (今はエンドユーザが明示的に行うべき)
  * [12968f1](http://github.com/symfony/symfony/commit/12968f144c40bc4936079adbaeb5601265fa5713 "12968f144c40bc4936079adbaeb5601265fa5713 commit on github"): \[Locale\] ICUデータの更新 (インドルピー記号の更新、LocaleTypeTestの更新、zh_Hans_MOの削除)
  * [a204aec](http://github.com/symfony/symfony/commit/a204aec08b711cd6b39a80c6c74e19584b9e3d32 "a204aec08b711cd6b39a80c6c74e19584b9e3d32 commit on github"), [3a36c08](http://github.com/symfony/symfony/commit/3a36c08d8eb86b5aeefe60a26d50d67f42ce35ea "3a36c08d8eb86b5aeefe60a26d50d67f42ce35ea commit on github"): フォームに１つしかウィジェットがないようなテンプレートを簡単にカスタマイズ出来るように修正 (Twig と PHP)
  * [43e38c3](http://github.com/symfony/symfony/commit/43e38c3ba4505a2aa9b93f1611736bb512757a60 "43e38c3ba4505a2aa9b93f1611736bb512757a60 commit on github"): \[DoctrineBundle\] doctrine.orm.entity_managersパラメータが名前とIDを保持するように変更
  * [a607afb](http://github.com/symfony/symfony/commit/a607afb8d243953b8aeb647103430b642127cd16 "a607afb8d243953b8aeb647103430b642127cd16 commit on github"): \[DoctrineBundle\] 登録されたDBAL接続の一覧を保持するためのdoctrine.dbal.connectionsパラメータを追加
  * [01695bc](http://github.com/symfony/symfony/commit/01695bc654a8c1c8c997c87330b4c6481ea17e69 "01695bc654a8c1c8c997c87330b4c6481ea17e69 commit on github"): \[DoctrineBundle\] イベントリスナー/サブスクライバがパラメータの命名規則に依存しないようにリファクタリング
  * [f644bbc](http://github.com/symfony/symfony/commit/f644bbc0271dbef4444b84bd27bc734cbfd752db "f644bbc0271dbef4444b84bd27bc734cbfd752db commit on github"): \[translations\] アプリケーションの翻訳ディレクトリを他のバンドルと一緒になるようにResourcesの下に移動
  * [dccac19](http://github.com/symfony/symfony/commit/dccac192d6cd54ffbdcd549dbb3c08c397e367de "dccac192d6cd54ffbdcd549dbb3c08c397e367de commit on github"): \[HttpFoundation\] アップロードされたファイルの元のファイル名をサニタイズ
  * [e7c0aea](http://github.com/symfony/symfony/commit/e7c0aea5871acf405d6925660e13ec29bc875097 "e7c0aea5871acf405d6925660e13ec29bc875097 commit on github"): Templating Engineの$globalsをオプションに変更
  * [b14db26](http://github.com/symfony/symfony/commit/b14db26062f55fb3efec614cdd0c174dea0029e9 "b14db26062f55fb3efec614cdd0c174dea0029e9 commit on github"): \[Routing\] RouterInterfaceが参照して使っていたsetContextをRouterInterfacesに追加
  * [11d25f6](http://github.com/symfony/symfony/commit/11d25f61e87c12f42c1c50940136bf1461cfcd52 "11d25f61e87c12f42c1c50940136bf1461cfcd52 commit on github"): \[WebProfilerBundle\] ユニットテストを追加
  * [ee3c239](http://github.com/symfony/symfony/commit/ee3c239d123589da5f087f780c5378b1f1d3ba05 "ee3c239d123589da5f087f780c5378b1f1d3ba05 commit on github"): \[AsseticBundle\] sassとscss とcompass filterの設定をベースディレクトリが含まれるように更新
  * [a4c6243](http://github.com/symfony/symfony/commit/a4c62437437a8772e427688b063378db9c8f74c5 "a4c62437437a8772e427688b063378db9c8f74c5 commit on github"): \[DoctrineBundle\] コマンドのリファクタリング
  * [74a243b](http://github.com/symfony/symfony/commit/74a243bdd60a17a87e5f23d2f48d73439bf0b424 "74a243bdd60a17a87e5f23d2f48d73439bf0b424 commit on github"): \[DoctrineBundle\] Webプロファイラに接続とエンティティマネージャを追加
  * [03f7049](http://github.com/symfony/symfony/commit/03f7049c7eb6dd2c8c19ba2c20d40a50e5496095 "03f7049c7eb6dd2c8c19ba2c20d40a50e5496095 commit on github"): \[DoctrineBundle\] Doctrineのproxyコマンドを下位ネームスペースに移動
  * [6fec656](http://github.com/symfony/symfony/commit/6fec6562390d7fbec72f038ac9ea281e5529eadb "6fec6562390d7fbec72f038ac9ea281e5529eadb commit on github"): \[DependencyInjection\] 匿名のサービスが常にプライベートになるように修正
