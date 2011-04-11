A week of symfony #223 (4->10 April 2011)
=========================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。<!-- プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク]()）-->

<br />
<br />
<hr />

今週はSymfony2にZend Loggerに変わる新しいログエンジンとして[monolog](https://github.com/symfony/symfony/commit/01ee1bfed114618e51537db14331926563eac9be)を取り入れました。また、新しく[Configuration interface](https://github.com/symfony/symfony/commit/b640fcb0f0d44f637f7468309440aea591dc17df)を追加しました。これはバンドルの設定項目のXSDやドキュメントを生成しやすくするためのもので、既存のDIコンテナ用のエクステンションはこれを用いるように書き換えられています。最後に、[メーリングリストで告知した](https://groups.google.com/forum/#!topic/symfony-devs/n7XuavSq9Zk)ように、[フォームのリファクタリング](https://github.com/symfony/symfony/pull/399)のレビューとテストが終わり次第マージができる状態になりました。

 
開発メーリングリスト
------------------------

  * [\[Symfony2\] Security ACL: EntryとFieldEntryクラスのprivatフィールド](https://groups.google.com/forum/#!topic/symfony-devs/Vue58AZefH0)
  * [POSTパラメーターバッグの名前をrequestからpostへ](https://groups.google.com/forum/#!topic/symfony-devs/WcktqVOMdfw)
  * [\[Symfony2\] FrameworkExtra/SecurityExtraとODMのアノテーションの名前空間](https://groups.google.com/forum/#!topic/symfony-devs/wdA6GTBrsCA)
  * [Formのリファクタリングが使えるレベルになりましたが大きな問題はありますか？](https://groups.google.com/forum/#!topic/symfony-devs/n7XuavSq9Zk)

Symfony2 開発ハイライト
-------------------------------

[チェンジログ](http://github.com/symfony/symfony/commits/master):

  * [424a1da](http://github.com/symfony/symfony/commit/424a1dad2784ca1b14b767f55ff522ca302e4594 "424a1dad2784ca1b14b767f55ff522ca302e4594 commit on github"), [47733d0](http://github.com/symfony/symfony/commit/47733d08a11f77d1ba104eee48c7d600a6371870 "47733d08a11f77d1ba104eee48c7d600a6371870 commit on github"), [7132f81](http://github.com/symfony/symfony/commit/7132f81d14dda4e5c8fff65b166a4829e362291f "7132f81d14dda4e5c8fff65b166a4829e362291f commit on github"): \[Serializer\] protectedで定義されていた一部をprivateに変更、finalを追加
  * [21b3ee6](http://github.com/symfony/symfony/commit/21b3ee678370eaac80339eb1971553cd6718ba8f "21b3ee678370eaac80339eb1971553cd6718ba8f commit on github"): \[WebProfilerBundle\] XHR時のリダイレクトの割り込み処理を行わないよう修正
  * [ad4a0bd](http://github.com/symfony/symfony/commit/ad4a0bda1c08652fa9006d16611335c1f0348f09 "ad4a0bda1c08652fa9006d16611335c1f0348f09 commit on github"): \[Console\] CommandTesterの返り値をコマンドの終了コードをを返すよう修正
  * [daa138f](http://github.com/symfony/symfony/commit/daa138ffc8465125c1789aa72bd871d649a31fa7 "daa138ffc8465125c1789aa72bd871d649a31fa7 commit on github"), [9b093d5](http://github.com/symfony/symfony/commit/9b093d53ae7b0a443f777578aa89cced18f4a45c "9b093d53ae7b0a443f777578aa89cced18f4a45c commit on github"), [d9b3643](http://github.com/symfony/symfony/commit/d9b3643d476e2b95446901f91686bfe37f947aa2 "d9b3643d476e2b95446901f91686bfe37f947aa2 commit on github"): \[DoctrineBundle\] コンフィギュレーションからカスタムハイドレーターをEntityManagerに追加できるよう修正
  * [8b7c857](http://github.com/symfony/symfony/commit/8b7c857ef3b8f0f88522528e19f4489dfd36cae2 "8b7c857ef3b8f0f88522528e19f4489dfd36cae2 commit on github"): リソースのパスにBundleサフィックスをつけて処理するよう修正
  * [dcd727c](http://github.com/symfony/symfony/commit/dcd727c0925bc535db0142c9d7d00fe48b01f886 "dcd727c0925bc535db0142c9d7d00fe48b01f886 commit on github"), [d0b6ed2](http://github.com/symfony/symfony/commit/d0b6ed2bb6500b4165a3570d9a2f2ee28cd29b9f "d0b6ed2bb6500b4165a3570d9a2f2ee28cd29b9f commit on github"): \[Kernel\] locateResourceメソッドのテストを復元
  * [3cd3dd3](http://github.com/symfony/symfony/commit/3cd3dd39ba727e930db0936eb7bba2dbef168143 "3cd3dd39ba727e930db0936eb7bba2dbef168143 commit on github"): \[Kernel\] リソースファイルのオーバーライドを実装
  * [7ed18bf](http://github.com/symfony/symfony/commit/7ed18bf8294fa6b40e473749890d7e36185e451c "7ed18bf8294fa6b40e473749890d7e36185e451c commit on github"): \[Kernel\] locateResource()メソッドでバンドルがリソースを隠している場合に例外を投げるよう修正
  * [1cb03b1](http://github.com/symfony/symfony/commit/1cb03b1448b04c88814b0e99a82e2fde876d53f6 "1cb03b1448b04c88814b0e99a82e2fde876d53f6 commit on github"): \[FrameworkBundle\] templating.loader.cache.pathパラメーターを削除
  * [01ee1bf](http://github.com/symfony/symfony/commit/01ee1bfed114618e51537db14331926563eac9be "01ee1bfed114618e51537db14331926563eac9be commit on github"), [5bd2b53](http://github.com/symfony/symfony/commit/5bd2b53cb8c85debebd952c7a488c551182e8d5c "5bd2b53cb8c85debebd952c7a488c551182e8d5c commit on github"): Zend Loggerをmonologに置き換え
  * [1f1ee3c](http://github.com/symfony/symfony/commit/1f1ee3cb011cd0652a30c0a0a7a8113bcdd6a3d8 "1f1ee3cb011cd0652a30c0a0a7a8113bcdd6a3d8 commit on github"), [b5f3d14](http://github.com/symfony/symfony/commit/b5f3d14714d25c96787cfc89669049b78460f48d "b5f3d14714d25c96787cfc89669049b78460f48d commit on github"): \[WebProfilerBundle\] イベントのパネルレイアウトと内容を修正
  * [4e5c0b1](http://github.com/symfony/symfony/commit/4e5c0b1da98d19db3526c3a4cafbd0fa1e6f8ff6 "4e5c0b1da98d19db3526c3a4cafbd0fa1e6f8ff6 commit on github"): \[AsseticBundle\] filter定義にfile項目を追加
  * [5a1d5e5](http://github.com/symfony/symfony/commit/5a1d5e5082b7758998ae04abe88ccd6c84055c9a "5a1d5e5082b7758998ae04abe88ccd6c84055c9a commit on github"), [747c98f](http://github.com/symfony/symfony/commit/747c98f178f08f454830174005bc998465b199e0 "747c98f178f08f454830174005bc998465b199e0 commit on github"): \[FrameworkBundle\] 独自のfile_link_formatをより簡単に追加できるように変更、debug.file_link_formatパラメーターの削除
  * [22beeb2](http://github.com/symfony/symfony/commit/22beeb2549f6801630b0243a206b554f10338643 "22beeb2549f6801630b0243a206b554f10338643 commit on github"): \[TwigBundle\] テンプレートの読み込みに失敗した際のエラーメッセージの改良
  * [b640fcb](http://github.com/symfony/symfony/commit/b640fcb0f0d44f637f7468309440aea591dc17df "b640fcb0f0d44f637f7468309440aea591dc17df commit on github"): \[Config\] ConfigurationInterfaceの実装
  * [0973d37](http://github.com/symfony/symfony/commit/0973d37202a8f43370396a6c16b85802084f5b32 "0973d37202a8f43370396a6c16b85802084f5b32 commit on github"): \[MonologBundle\] ConfigurationクラスにConfigurationInterfaceインターフェイスを実装
  * [7c0a39c](http://github.com/symfony/symfony/commit/7c0a39c353e31ccfd9ea6325e7edc7f6f54d4b3d "7c0a39c353e31ccfd9ea6325e7edc7f6f54d4b3d commit on github"): \[Routing\] PHPマッチャー/ダンパーの出力を最適化
  * [e3679ef](http://github.com/symfony/symfony/commit/e3679ef44f0f20fd3b9ec13555908e6497826950 "e3679ef44f0f20fd3b9ec13555908e6497826950 commit on github"): \[Routing\] RoutingをFrameworkBundleから分離
  * [839782b](http://github.com/symfony/symfony/commit/839782b6e4a7c22d531e065a9867cec661892d31 "839782b6e4a7c22d531e065a9867cec661892d31 commit on github"): \[FrameworkBundle\] ルーティングによるリダイレクトのサポートを追加
  * [7707c0f](http://github.com/symfony/symfony/commit/7707c0f2516f38f30a1ca8f42de7b66ad7d37b6e "7707c0f2516f38f30a1ca8f42de7b66ad7d37b6e commit on github"): \[Kernel\] バンドルの継承の修正
  * [9ff2ca7](http://github.com/symfony/symfony/commit/9ff2ca7f1dc2785c4efe791cf4d195d91f24c36f "9ff2ca7f1dc2785c4efe791cf4d195d91f24c36f commit on github"), [3ff157c](http://github.com/symfony/symfony/commit/3ff157c8a5b42de866975067d44de4726bb581bc "3ff157c8a5b42de866975067d44de4726bb581bc commit on github"), [9b3ce98](http://github.com/symfony/symfony/commit/9b3ce9843228753264e08fbc375d23b037b21b86 "9b3ce9843228753264e08fbc375d23b037b21b86 commit on github"): \[Validator\] APCを用いたキャッシュを行っている箇所の修正
  * [d0f45fd](http://github.com/symfony/symfony/commit/d0f45fd3b60632ffac3d3678afaa98e09255ca61 "d0f45fd3b60632ffac3d3678afaa98e09255ca61 commit on github"): \[FrameworkBundle\] Validatorのメタデータのキャッシュの設定項目の追加
  * [4949e0d](http://github.com/symfony/symfony/commit/4949e0d1edc23c76783909c06089c50e3bc72f7a "4949e0d1edc23c76783909c06089c50e3bc72f7a commit on github"): \[MonologBundle\] ハンドラーを追加できるよう設定を変更
  * [723f7d4](http://github.com/symfony/symfony/commit/723f7d46b70fe398993b7c1f4ff888e5f951f712 "723f7d46b70fe398993b7c1f4ff888e5f951f712 commit on github"): \[MonologBundle\] fingers_crossedとrotating_fileに項目名を変更
  * [5ecf1cd](http://github.com/symfony/symfony/commit/5ecf1cd1d1a45a299d5f61c6b96c2a50f70ffe9c "5ecf1cd1d1a45a299d5f61c6b96c2a50f70ffe9c commit on github"): \[FrameworkBundle\] 意味のあるエラー情報を表示するよう修正
  * [5a4ffcd](http://github.com/symfony/symfony/commit/5a4ffcd8b6d6b561f8fdf949822c8e259d16cb16 "5a4ffcd8b6d6b561f8fdf949822c8e259d16cb16 commit on github"): \[Security\] パラメーターの追加
  * [6c48019](http://github.com/symfony/symfony/commit/6c4801945ed7f16ebc884abf10b0dc4add9e16e0 "6c4801945ed7f16ebc884abf10b0dc4add9e16e0 commit on github"), [a230090](http://github.com/symfony/symfony/commit/a230090537b593ed27434c0cc42f5d0ab326e143 "a230090537b593ed27434c0cc42f5d0ab326e143 commit on github"): \[FrameworkBundle\] TemplateReferenceにgetLogicalName()メソッドを追加


> **NOTE**
> 翻訳者コメント<br />
> フォーム周りの大幅なリファクタリングがいよいよ取り込まれそうです。symfony 1の時はフォーム周りが鬼門でしたが、あれに比べたら柔軟なフォームの組み立てが可能になったのではないかと思われます。リリースされたら実際に使って感触を試してみたいです。
> あとはロガーがZend Loggerからmonologに変わりました。AsseticやTwigもそうですが、Pythonから輸入してきたライブラリが多いように感じます。情報があまりない場合はオリジナルのライブラリの情報を調べてみるのもよいかもしれませんね。
> [fivestar]

