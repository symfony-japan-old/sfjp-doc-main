A week of symfony #233 (13->19 June 2011)
=========================================

 - [原文](http://symfony.com/blog/a-week-of-symfony-233-13-19-june-2011)
 
今週 Symfony 2.0 beta5 が公開され、ベータ期間の終わりを告げました。またもや、Form コンポーネントの開発がもっとも活発でしたが、Process、CssSelector、Yaml と Finder を含む多くのコンポーネントも調整され改善されました。ほかの重要な変更は [ClassLoader におけるパフォーマンスの大きな改善](https://github.com/symfony/symfony/commit/fb4f37856e70f2271349d057bbd147d83779f1c6) と[Session のリファクタリング](https://github.com/symfony/symfony/commit/1467a9bd9d363ba1cc33a2849b3ae97dbb936d12) です。
 
開発メーリングリスト
--------------------

  * [\[Beta4\]\[Form\] エクストラフィールド (バインドされたオブジェクトに存在しない)](https://groups.google.com/forum/#!topic/symfony-devs/qLf1T7JhkCA)
  * [DI におけるスコープ](https://groups.google.com/forum/#!topic/symfony-devs/Uq6dC09O8cg)
  * [\[Symfony2\] パーミッションをセットアップするための息切れしないソリューション](https://groups.google.com/forum/#!topic/symfony-devs/WAbUXUBdRas)
  * [\[Sf2\] フォームレンダリングにおける RFC](https://groups.google.com/forum/#!topic/symfony-devs/F3VBKLpIBUU)
  * [LoggerInterface](https://groups.google.com/forum/#!topic/symfony-devs/lQ5nVzT7G1Q)

symfony 1 の開発のハイライト
----------------------------

[チェンジログ](http://trac.symfony-project.com/trac/timeline?from=19%2F06%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r32652](http://trac.symfony-project.org/changeset/32652 "32652 revision on trac"): \[1.4\] いくつかのパラメータをシリアライズしない問題に対応するために sfRoute を修正しました。
  * [r32653](http://trac.symfony-project.org/changeset/32653 "32653 revision on trac"): \[1.4\] fixed possible PHP notice
  * [r32654](http://trac.symfony-project.org/changeset/32654 "32654 revision on trac"): \[1.4\] sfObjectRouteCollection における標準のアクションを修正しました (HEAD は GET と同等です)

Symfony2 の開発ハイライト
-------------------------

[チェンジログ](http://github.com/symfony/symfony/commits/master):

  * [1e50a55](http://github.com/symfony/symfony/commit/1e50a553d202f2daaf4b4d7286418d57660966cc "1e50a553d202f2daaf4b4d7286418d57660966cc commit on github"), [07d823c](http://github.com/symfony/symfony/commit/07d823caa8028a1bcf1fa5aa403aa977220809be "07d823caa8028a1bcf1fa5aa403aa977220809be commit on github"): \[HttpFoundation\] 文字集合の値が常に UTF-8 になるように修正しました
  * [91f4097](http://github.com/symfony/symfony/commit/91f4097a0905e2f532967a1836f57997ff6332be "91f4097a0905e2f532967a1836f57997ff6332be commit on github"): \[Routing\] ダンプされる URL マッチャクラスにおいて RouteCollections に対するネスティングの改善。この変更によって、 「/blogger」のプレフィックスがつけられたルートは「/blog」内部にネストされます
  * [5b0f1da](http://github.com/symfony/symfony/commit/5b0f1da074f22f038324cb1f2e6b97ea787167c7 "5b0f1da074f22f038324cb1f2e6b97ea787167c7 commit on github"): \[HttpKernel\] WebTestCase メソッドをスタティックに変更しました
  * [8677aa3](http://github.com/symfony/symfony/commit/8677aa3dce03e3633d272054e9c5d153aee9cf86 "8677aa3dce03e3633d272054e9c5d153aee9cf86 commit on github"): \[Form, TwigBridge\] レンダリングを修正しました
  * [9135f96](http://github.com/symfony/symfony/commit/9135f963db9d59d0785808a9cf7c22d2cfd4384d "9135f963db9d59d0785808a9cf7c22d2cfd4384d commit on github"): \[Form, TwigBridge\] テンプレートキャッシュをより効率的なものにしました
  * [b19052f](http://github.com/symfony/symfony/commit/b19052f8797d13a0ca6700c7c7f057dfb7fe0585 "b19052f8797d13a0ca6700c7c7f057dfb7fe0585 commit on github"): \[Form, TwigBridge\] テンプレートの代わりにブロックをキャッシュすることでキャッシュレイヤーを修正しました
  * [acd2cf1](http://github.com/symfony/symfony/commit/acd2cf11d8d9c45bc971fa1a85cde771dac98044 "acd2cf11d8d9c45bc971fa1a85cde771dac98044 commit on github"), [33baf9d](http://github.com/symfony/symfony/commit/33baf9d8adca979ae146e491d9876e6f3a272e66 "33baf9d8adca979ae146e491d9876e6f3a272e66 commit on github"): \[TwigBundle\] FilesystemLoader を最適化しました
  * [16e6cea](http://github.com/symfony/symfony/commit/16e6cea240dda945b593e5308bcdb8966c644d3f "16e6cea240dda945b593e5308bcdb8966c644d3f commit on github"): \[DoctrineBundle\] バンドルにおける最初のエンティティの生成を修正しました
  * [1890dab](http://github.com/symfony/symfony/commit/1890dab212e8ba56381ba2e10c2473396e139a11 "1890dab212e8ba56381ba2e10c2473396e139a11 commit on github"): \[AsseticBundle\] ロジカルテンプレートネームと連携させるためにカスタム合体ロジックを追加しました
  * [d16a708](http://github.com/symfony/symfony/commit/d16a708cc8001d768fc9937170baa0f5080d7ab1 "d16a708cc8001d768fc9937170baa0f5080d7ab1 commit on github"): \[Form\] ファイルの種類のクラスを簡略化しました
  * [c364008](http://github.com/symfony/symfony/commit/c364008a3b5e12dd0a3ac11eb1b5450be3f6fb42 "c364008a3b5e12dd0a3ac11eb1b5450be3f6fb42 commit on github"), [2ce3cfa](http://github.com/symfony/symfony/commit/2ce3cfad18691af93370be1b1d12be21a180ee19 "2ce3cfad18691af93370be1b1d12be21a180ee19 commit on github"): \[Form\] 必須項目が true の場合でもチョイスに対して空の値を表示することを許可するように修正しました
  * [4e3e276](http://github.com/symfony/symfony/commit/4e3e2768fb917f8b3798d199c9eb275e99467d39 "4e3e2768fb917f8b3798d199c9eb275e99467d39 commit on github"): \[Form\] コレクションビューのプロトタイプビューの子要素を作成しました
  * [ac0c00c](http://github.com/symfony/symfony/commit/ac0c00c6e8111e91231412b1c9d9e8a497027c29 "ac0c00c6e8111e91231412b1c9d9e8a497027c29 commit on github"), [38b3b74](http://github.com/symfony/symfony/commit/38b3b7474f52d49eab81e0f78a4634b7d84203b1 "38b3b7474f52d49eab81e0f78a4634b7d84203b1 commit on github"), [136b80a](http://github.com/symfony/symfony/commit/136b80ae63a16198071030c2147f22d3b6fffe76 "136b80ae63a16198071030c2147f22d3b6fffe76 commit on github"), [9d6357c](http://github.com/symfony/symfony/commit/9d6357c35b9e38eeab303a9b6bff045bf2ab27a7 "9d6357c35b9e38eeab303a9b6bff045bf2ab27a7 commit on github"): \[HttpFoundation\] File に \SplFileInfo を継承させました
  * [a7c1ff8](http://github.com/symfony/symfony/commit/a7c1ff85585b8afa45c6f01571e9693c345158a6 "a7c1ff85585b8afa45c6f01571e9693c345158a6 commit on github"): \[Validator\] DateTime オブジェクトを有効な Times にすることを許可しました
  * [4016dfb](http://github.com/symfony/symfony/commit/4016dfbb84abd166d9c8ef8d137bbb9f66e2d5e8 "4016dfbb84abd166d9c8ef8d137bbb9f66e2d5e8 commit on github"): \[AsseticBundle\] 必要なときだけ呼び出せるように ExecutableFinder をクロージャに戻しました
  * [1ad5bfd](http://github.com/symfony/symfony/commit/1ad5bfd723e8199435c1cf79e01f2e6bad00fea9 "1ad5bfd723e8199435c1cf79e01f2e6bad00fea9 commit on github"): \[CssSelector\] SyntaxError をリネームしました
  * [b76a1c3](http://github.com/symfony/symfony/commit/b76a1c3077d89f7e0d5efe8fa2bf95edb8b22b37 "b76a1c3077d89f7e0d5efe8fa2bf95edb8b22b37 commit on github"): \[Finder\] コンビニエンスメソッドの Finder::create() を追加しました
  * [c6cc427](http://github.com/symfony/symfony/commit/c6cc427e4b566f0899e785347710ee19f256ef04 "c6cc427e4b566f0899e785347710ee19f256ef04 commit on github"): \[EventDispatcher\] イベントのサブスクライバのための優先順位をセットする方法を追加しました
  * [ee8f34e](http://github.com/symfony/symfony/commit/ee8f34e7eda49706f83718c3544cea4e29f14f9c "ee8f34e7eda49706f83718c3544cea4e29f14f9c commit on github"): \[AsseticBundle\] cssembed コンフィグオプションを追加しました
  * [2f04bdb](http://github.com/symfony/symfony/commit/2f04bdb3c528cf079c0c652b3eb710d5a8ee04ec "2f04bdb3c528cf079c0c652b3eb710d5a8ee04ec commit on github"): \[HttpFoundation\] checkIp() を再利用可能にしました
  * [3859589](http://github.com/symfony/symfony/commit/3859589daac0a6562faa81807d2fabfa657bfead "3859589daac0a6562faa81807d2fabfa657bfead commit on github"): \[Yaml\] load() を parse() にリネームしました
  * [a9dab71](http://github.com/symfony/symfony/commit/a9dab719df340af35681b89b56319996b83f5df3 "a9dab719df340af35681b89b56319996b83f5df3 commit on github"): \[Yaml\] YAML 1.1 の仕様のサポートを削除しました
  * [06614cd](http://github.com/symfony/symfony/commit/06614cd6ca97586bc7e251ebb61ed54fe3e4ab5c "06614cd6ca97586bc7e251ebb61ed54fe3e4ab5c commit on github"): \[Yaml\] 例外をそれぞれの独自のサブネームスペースに移動させ、ダンプのための固有の例外を追加しました
  * [b552354](http://github.com/symfony/symfony/commit/b55235441475aef4964933a45275b41b11df083a "b55235441475aef4964933a45275b41b11df083a commit on github"): \[Process\] Executable Finder は open_basedir リストを通じて検索する前にファイルがこのリストに存在しているかチェックを試みるようになりました
  * [b709551](http://github.com/symfony/symfony/commit/b7095512526a85b29bf72a06c6a5a0c862e276fc "b7095512526a85b29bf72a06c6a5a0c862e276fc commit on github"): Form::types と FormView::types が同じ順番を使うように変更しました (Parent > Child)
  * [af97610](http://github.com/symfony/symfony/commit/af97610ee6965e4002729aecc2475981264e9e0d "af97610ee6965e4002729aecc2475981264e9e0d commit on github"): \[CssSelector\] Parser::cssToXPath() を CssSelector::toXPath() にリネームしました
  * [46a93c3](http://github.com/symfony/symfony/commit/46a93c376c5f8b8c481b237b24eb72a1bdc7f4d7 "46a93c376c5f8b8c481b237b24eb72a1bdc7f4d7 commit on github"): \[Routing\] 親のプレフィックスがいくつかの隣接したコレクションに対して同じである場合に PHP ダンパーを最適化しました
  * [52697ed](http://github.com/symfony/symfony/commit/52697ed3dfe0b973cc5a8d627550fa0937e6fa11 "52697ed3dfe0b973cc5a8d627550fa0937e6fa11 commit on github"): \[Swiftmailer\] プラグインの登録の順序によって disable_strategy ビヘイビアが微妙に変わるように修正しました
  * [fb24b95](http://github.com/symfony/symfony/commit/fb24b95bd556b91ac2f85f7395f6334aa1640f4b "fb24b95bd556b91ac2f85f7395f6334aa1640f4b commit on github"): エラーレベルの調整を行いました
  * [1467a9b](http://github.com/symfony/symfony/commit/1467a9bd9d363ba1cc33a2849b3ae97dbb936d12 "1467a9bd9d363ba1cc33a2849b3ae97dbb936d12 commit on github"): \[HttpFoundation\] Session をリファクタリングしました
  * [b3fa8bf](http://github.com/symfony/symfony/commit/b3fa8bf7cbca6192bb1ea43eb47a7acbecb60ff0 "b3fa8bf7cbca6192bb1ea43eb47a7acbecb60ff0 commit on github"): \[Swiftmailer\] 任意のサービスをトランスポートとして使えるようにしました
  * [524d51a](http://github.com/symfony/symfony/commit/524d51adf88b4614a9d33dfe918c63a8b3339ee6 "524d51adf88b4614a9d33dfe918c63a8b3339ee6 commit on github"): \[AsseticBundle\] バンドルを独自のリポジトリに移動させました (Symfony SE にはまだ搭載されています)
  * [f1b955b](http://github.com/symfony/symfony/commit/f1b955be8c5ab5e773403f0e56da9c0867d516f3 "f1b955be8c5ab5e773403f0e56da9c0867d516f3 commit on github"): \[Form\] 提供されたタイムゾーンの値を変更しないようにトランスフォーマを修正しました
  * [2b0c352](http://github.com/symfony/symfony/commit/2b0c3526d8f87cb83ea3fd448396dd9a1ca826d0 "2b0c3526d8f87cb83ea3fd448396dd9a1ca826d0 commit on github"): YamlParser、Validators、PhpEngine + Helpers、HttpFoundation に対するコードカバレッジを増やしました
  * [a7974ff](http://github.com/symfony/symfony/commit/a7974ff43c294e7f239ec1f76ca63cb1d037ab82 "a7974ff43c294e7f239ec1f76ca63cb1d037ab82 commit on github"): Form Twig テンプレートをより明確な名前にリネームしました
  * [fa9b920](http://github.com/symfony/symfony/commit/fa9b920051a113246893f9e9c91726c940684fa0 "fa9b920051a113246893f9e9c91726c940684fa0 commit on github"): \[Security\] UserProviderInterface::loadUser() を refreshUser() にリネームしました
  * [627a7f7](http://github.com/symfony/symfony/commit/627a7f7cd416aa647c2670ee6f4d027ad647646b "627a7f7cd416aa647c2670ee6f4d027ad647646b commit on github"): \[TwigBridge\] 衝突を避けるためにブロック名をリネームしました
  * [41347bc](http://github.com/symfony/symfony/commit/41347bc3f52a5c51689b12c6b65aaddb310756d4 "41347bc3f52a5c51689b12c6b65aaddb310756d4 commit on github"): \[DoctrineBundle\] プラットフォームのカスタムタイプのサポートを追加しました
  * [ad1b690](http://github.com/symfony/symfony/commit/ad1b6901f2a72cb9178db587f9b1ce890296d40b "ad1b6901f2a72cb9178db587f9b1ce890296d40b commit on github"): \[DoctrineBundle\] XSD スキーマをアップデートしました
  * [fb4f378](http://github.com/symfony/symfony/commit/fb4f37856e70f2271349d057bbd147d83779f1c6 "fb4f37856e70f2271349d057bbd147d83779f1c6 commit on github"), [968cc75](http://github.com/symfony/symfony/commit/968cc7532d92e45a5522b8584abc39a46c93a9ef "968cc7532d92e45a5522b8584abc39a46c93a9ef commit on github"): \[ClassLoader\] 大きなパフォーマンス改善を行いました
  * [610c1cc](http://github.com/symfony/symfony/commit/610c1cc9879061c2e5832d661b7a54b72cd142d6 "610c1cc9879061c2e5832d661b7a54b72cd142d6 commit on github"): \[Routing\] AnnotationGlobLoader を削除しました