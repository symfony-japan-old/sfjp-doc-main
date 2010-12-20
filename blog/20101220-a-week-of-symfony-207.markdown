A week of symfony #207 (13->19 December 2010)
=============================================

今週のSymfony2では、セキュリティに関わる2つの大きな変更がコミットされました:[アンシリアライズ後のユーザリフレッシュの修正](https://github.com/symfony/symfony/commit/3c692bd1608eb2bef30f74343f476a5e045ab38b)と[トラストリゾルバー認証の追加](https://github.com/symfony/symfony/commit/abe804726279148cdebae017550308c7fc21114b)。また、2つの重要な微調整がコミットされました: Twigテンプレートでのハッシュ構文の追加と、XML属性の新しいフォーマットです。


開発メーリングリスト
------------------------

  * ["[Symfony2] パスワードのハッシュ化"](https://groups.google.com/forum/?pli=1#!topic/symfony-devs/6xLFKlasiMw)
  * ["[Symfony2] RFC: 複数のフィールドグループを1つのフォームにマージ"](https://groups.google.com/forum/?pli=1#!topic/symfony-devs/2PRlTxIOKb8)
  * ["Symfony2: 新しくプロジェクトを始める際のオススメ"](https://groups.google.com/forum/?pli=1#!topic/symfony-devs/zFvPZ9C4WPU)
  * ["[Symfony2] パスワードフィールドの初期値"](https://groups.google.com/forum/?pli=1#!topic/symfony-devs/IFhlASNJiJY)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [984a857](http://github.com/symfony/symfony/commit/984a857a96252ce3c355554e2ab133649f743b70 "984a857a96252ce3c355554e2ab133649f743b70 commit on github"): \[Validator\] 親クラスにスタティックメソッドがある際に子クラスでその同じスタティックメソッドをロードしないようにするスタティックメソッドローダーの追加
  * [131b3fe](http://github.com/symfony/symfony/commit/131b3fe3730ba979eb57d4e3d7d683be472da09c "131b3fe3730ba979eb57d4e3d7d683be472da09c commit on github"): \[Form\] サブクラスでの変更を容易するための、FiledとFieldGroupのリファクタリング
  * [e80aa9a](http://github.com/symfony/symfony/commit/e80aa9a5ab9643ad7dbf85727cf4188e58cda6ed "e80aa9a5ab9643ad7dbf85727cf4188e58cda6ed commit on github"): \[Form\] フィールドが削除されている際に、それに伴うCollectionFieldのデータの修正
  * [f73b6b4](http://github.com/symfony/symfony/commit/f73b6b4e1c5c563d31176c9de1fdeb962a94d0e3 "f73b6b4e1c5c563d31176c9de1fdeb962a94d0e3 commit on github"): \[PropertyPath\] publicでないオブジェクトがプロパティにアクセスする際の __get() と __set() の使用方法を修正
  * [1b2ca25](http://github.com/symfony/symfony/commit/1b2ca259f12cf7de86626c78d2d8b1573e8ddf85 "1b2ca259f12cf7de86626c78d2d8b1573e8ddf85 commit on github"), [af291bb](http://github.com/symfony/symfony/commit/af291bb0f1c9032adaa96790829cbe04077a8234 "af291bb0f1c9032adaa96790829cbe04077a8234 commit on github"): \[Validator\] 文字列の制約バリデターに、空の値を受け付けることができるように修正
  * [e49cc36](http://github.com/symfony/symfony/commit/e49cc363395ef02f7dc68ced1726f69e08429492 "e49cc363395ef02f7dc68ced1726f69e08429492 commit on github"): \[DependencyInjection\] インターフェースがExtensionで組み込まれたコンテナにおいて定義できるように。そして、インタフェースインジェクションがコンストラクタの引数が必要なクラスで使えるように修正
  * [48e3053](http://github.com/symfony/symfony/commit/48e30537c407db8a645a3e18c854a13b9d9b1873 "48e30537c407db8a645a3e18c854a13b9d9b1873 commit on github"): YAMLリソースが配列でないときの例外を追加
  * [504463c](http://github.com/symfony/symfony/commit/504463c30769264e4cefc32f99018d9000e7c51c "504463c30769264e4cefc32f99018d9000e7c51c commit on github"): \[Routing\] PHPジェネレーターのダンプコードのリファクタリング
  * [7cb8dca](http://github.com/symfony/symfony/commit/7cb8dca04dad72679e3615e3b45ab067c34494bf "7cb8dca04dad72679e3615e3b45ab067c34494bf commit on github"), [5857576](http://github.com/symfony/symfony/commit/5857576024739919dd03dd9f204bb3446cacfc01 "5857576024739919dd03dd9f204bb3446cacfc01 commit on github"): \[Routing\] ルート名に有効な文字として、 .（ドット）を追加
  * [a7c8157](http://github.com/symfony/symfony/commit/a7c81577c7f26cbbf34df49d200d496c91f825e2 "a7c81577c7f26cbbf34df49d200d496c91f825e2 commit on github"): \[HttpFoundation\] リクエストから生の内容を取り出す方法を追加
  * [abe8047](http://github.com/symfony/symfony/commit/abe804726279148cdebae017550308c7fc21114b "abe804726279148cdebae017550308c7fc21114b commit on github"): トラストリゾルバ認証を追加
  * [30f231d](http://github.com/symfony/symfony/commit/30f231deaf5208b2f4854b3f550259a15f8fbebd "30f231deaf5208b2f4854b3f550259a15f8fbebd commit on github"): フォームテンプレートのデフォルトをDICコンフィグに移動
  * [e6d0385](http://github.com/symfony/symfony/commit/e6d03857780abf17d02ae2b76e90d76d370ba302 "e6d03857780abf17d02ae2b76e90d76d370ba302 commit on github"): \[HttpFoundation\] スクリプト名が削除されるべき際に、HTTPSで getUri() もしくは getPathForUri() を使用した際の Request::create()を修正
  * [02a92ec](http://github.com/symfony/symfony/commit/02a92ec297cc1bbc19cabc6103f4b708bfe3771c "02a92ec297cc1bbc19cabc6103f4b708bfe3771c commit on github"): \[TwigBundle\] Twigの設定で自動エスケープの機能のオプションを追加
  * [84c7496](http://github.com/symfony/symfony/commit/84c749656543265d966d105cdefa2aea2583f0ae "84c749656543265d966d105cdefa2aea2583f0ae commit on github"): \[DoctrineBundle\] createOrmProxyDirectoryメソッドを修正
  * [6970a46](http://github.com/symfony/symfony/commit/6970a46b84072b835a90612e19fb8109f1f78738 "6970a46b84072b835a90612e19fb8109f1f78738 commit on github"): 新しいハッシュ構文をTwigテンプレートに追加
  * [c9f08c0](http://github.com/symfony/symfony/commit/c9f08c0a68446ef27e5ec089c9ec5b85ba78b35a "c9f08c0a68446ef27e5ec089c9ec5b85ba78b35a commit on github"): XMLの属性名に _(アンダースコア) を使用せずに -（ハイフン）を使用するように変更（これで全て表記が統一されました）
  * [3c692bd](http://github.com/symfony/symfony/commit/3c692bd1608eb2bef30f74343f476a5e045ab38b "3c692bd1608eb2bef30f74343f476a5e045ab38b commit on github"): アンシリアライズの後にユーザをリフレッシュするように修正

