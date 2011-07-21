A week of symfony #236 (4->10 July 2011)
========================================

今週Symfony2は[4番目のリリース候補バージョン](http://symfony.com/blog/symfony2-2-0-rc4-released)を公開しました。 ファイナルリリースの前の最新バージョンとなります。さらに、Symfony2はDoctrineをバージョン2.1、Monologを1.0へ更新しました。最後に例外メッセージの一部が改善され、[検証エラーメッセージ](http://twitter.com/#!/fabpot/status/90032233515196416)が多くの言語に更新/翻訳された。

 
開発メーリングリスト
------------------------

  * [どのようにCSSファイルにAssetイメージファイルに埋め込む？](https://groups.google.com/forum/#!topic/symfony-devs/5JOZCBrtW4w)
  * [ESIを使用するときに、なぜmax-ageに代わりs-maxageのディレクティブを使用する必要がある？](https://groups.google.com/forum/#!topic/symfony-devs/rP6IdpnM2Ck)
  * [単一変数のレンダリング](https://groups.google.com/forum/#!topic/symfony-devs/3Wr6yJ9K2Sk)

symfony 1 開発ハイライト
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=10%2F07%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r32729](http://trac.symfony-project.org/changeset/32729 "32729 revision on trac"): [1.3, 1.4] getHost()を転送されたホストのチェインを考慮するように更新
  * [r32741](http://trac.symfony-project.org/changeset/32741 "32741 revision on trac"): [1.4] sfCultureInfo::getCountries()からデータの無い場合を削除

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [06c3712](http://github.com/symfony/symfony/commit/06c371278f01dbc1a3145d07fb55bd636300f3c7 "06c371278f01dbc1a3145d07fb55bd636300f3c7 commit on github"): [Form] FileTypeCsrdExtensionは不要となりました。(FileTypeはFieldTypeを拡張)
  * [756ea8d](http://github.com/symfony/symfony/commit/756ea8db39421cdbec07b2a6fd457540b4cedb47 "756ea8db39421cdbec07b2a6fd457540b4cedb47 commit on github"), [311a9bd](http://github.com/symfony/symfony/commit/311a9bd02bd9b0304f8b3e72e6f4f290d2b1e53b "311a9bd02bd9b0304f8b3e72e6f4f290d2b1e53b commit on github"): ユーザーが新しいクッキー名を指定した時のみsession_name()を呼ぶ
  * [bd89cc7](http://github.com/symfony/symfony/commit/bd89cc7b372826ab4fc98ac618605f0de70e47c7 "bd89cc7b372826ab4fc98ac618605f0de70e47c7 commit on github"): [FrameworkBundle] テンプレートパーサがテンプレートにドットを受け入れるよう修正
  * [e6da824](http://github.com/symfony/symfony/commit/e6da824aa10dffecc3ccdaf95ca1f0ae906add94 "e6da824aa10dffecc3ccdaf95ca1f0ae906add94 commit on github"): [MonologBundle] コアプロセッサのためのサービスを追加
  * [b9656e6](http://github.com/symfony/symfony/commit/b9656e62ec441c010fc205e8533de42f3e3d925e "b9656e62ec441c010fc205e8533de42f3e3d925e commit on github"): Doctrineのバージョンを2.1.0に更新
  * [4f8a980](http://github.com/symfony/symfony/commit/4f8a98033a949630cc6bd2a6f37c401b25ac0383 "4f8a98033a949630cc6bd2a6f37c401b25ac0383 commit on github"): [Security] URLの生成に関連するハックを削除
  * [431460f](http://github.com/symfony/symfony/commit/431460f6ff23ef3a27800d917d3989924ea84574 "431460f6ff23ef3a27800d917d3989924ea84574 commit on github"): [Form] 十分にチェックされており空の選択フォームを防止する条件のchoiceまたはchoice_listの必要要件を削除(AJAXなどによる移植)
  * [4c6e177](http://github.com/symfony/symfony/commit/4c6e177a6305567b337e09bd2560422a26b97e39 "4c6e177a6305567b337e09bd2560422a26b97e39 commit on github"): [Form] デフォルトのバリデータの修正
  * [932cd10](http://github.com/symfony/symfony/commit/932cd10477a5fa507df4171ebc97323f8715c5a6 "932cd10477a5fa507df4171ebc97323f8715c5a6 commit on github"), [722ad12](http://github.com/symfony/symfony/commit/722ad12a2d2e5ff1b52d969a2af512cf7f8fc704 "722ad12a2d2e5ff1b52d969a2af512cf7f8fc704 commit on github"): プロキシからの作成されたHTTPヘッダは、デフォルトでは信頼しない
  * [d58ba34](http://github.com/symfony/symfony/commit/d58ba342460fe5c4410e3d94f3b11f2ace0bc2c9 "d58ba342460fe5c4410e3d94f3b11f2ace0bc2c9 commit on github"): [Validator] アップロードされたファイルを検証する際にupload_max_filesize iniディレクティブを考慮
  * [3df5ec3](http://github.com/symfony/symfony/commit/3df5ec3de5faa9eb0c7d1355f50c4841d9957872 "3df5ec3de5faa9eb0c7d1355f50c4841d9957872 commit on github"): [HttpKernel] クライアントでupload_max_filesize iniディレクティブのサポートの追加
  * [133169f](http://github.com/symfony/symfony/commit/133169f6683f82283281e974f66921a0a8cfaa5e "133169f6683f82283281e974f66921a0a8cfaa5e commit on github"): XmlFileLoaderのエクステンションのためのより良い例外メッセージ
  * [d3b7807](http://github.com/symfony/symfony/commit/d3b78075f077fff5cb591735641ea22f2c2e7565 "d3b78075f077fff5cb591735641ea22f2c2e7565 commit on github"): [Doctrine] オブジェクトがプロキシかつオリジナルのエンティティのインスタンスでない時のDoctrine guesserを修正
  * [090a51a](http://github.com/symfony/symfony/commit/090a51a0fe076b0667018d333cb307cd73cdfe5d "090a51a0fe076b0667018d333cb307cd73cdfe5d commit on github"), [f21dc42](http://github.com/symfony/symfony/commit/f21dc423584e3a25bd62bdcb93056435d2fc6b4c "f21dc423584e3a25bd62bdcb93056435d2fc6b4c commit on github"): 特定のエンティティに関連付けられたエンティティマネージャを取得するRegistry::getEntityManagerForObject()を追加
  * [0824736](http://github.com/symfony/symfony/commit/082473659e22ea85e67956818e702cfae6701c9d "082473659e22ea85e67956818e702cfae6701c9d commit on github"): Doctrineプロキシオブジェクトのバリデーションの修正
  * [ef022c0](http://github.com/symfony/symfony/commit/ef022c0c6c6f8635d73862aaf58cdb9416f038cb "ef022c0c6c6f8635d73862aaf58cdb9416f038cb commit on github"): WTFの問題を回避するために型の名前の推測を削除
  * [47da6cf](http://github.com/symfony/symfony/commit/47da6cf39eeda97ec46e899704115b222e66a151 "47da6cf39eeda97ec46e899704115b222e66a151 commit on github"): [Form] 選択肢の制約の推測を削除
  * [fa20b51](http://github.com/symfony/symfony/commit/fa20b514a23e33a067184ca65493c029ab83a6bb "fa20b514a23e33a067184ca65493c029ab83a6bb commit on github"): [Console] 設定プリンタのリファクタリング
  * [874fb95](http://github.com/symfony/symfony/commit/874fb9540a89f5cbae3b503fc1aad540ffbcc8b0 "874fb9540a89f5cbae3b503fc1aad540ffbcc8b0 commit on github"): [MonologBundle] コンフィグレーションプロセッサのリファクタリング
  * [f8b5f35](http://github.com/symfony/symfony/commit/f8b5f350dc4a502aa4b51497d0a8c889103387f4 "f8b5f350dc4a502aa4b51497d0a8c889103387f4 commit on github"): [MonologBundle] swiftmailerに電子メールプロトタイプを設定するための方法をリファクタリング
  * [c12676b](http://github.com/symfony/symfony/commit/c12676b0a18f26732d5f01503f83ba63d1b9216b "c12676b0a18f26732d5f01503f83ba63d1b9216b commit on github"): [Doctrine] エンティティに__toStringメソッドが定義されていない時のより良いエラーメッセージを追加
  * [bb5075d](http://github.com/symfony/symfony/commit/bb5075d8200cdb0a285fb366e58924e787edf231 "bb5075d8200cdb0a285fb366e58924e787edf231 commit on github"): [HttpFoundation] レスポンスヘッダが2回送信される事を防止。この変更により、開発者が早期にレスポンスコンテンツをフラッシュしようとする場合、より柔軟性が生まれる。
  * [7eec2ca](http://github.com/symfony/symfony/commit/7eec2ca7b3c7bc5b9018e0d549344c21776857aa "7eec2ca7b3c7bc5b9018e0d549344c21776857aa commit on github"): [Form] フォームタイプ名のバリデータを追加
  * [6039569](http://github.com/symfony/symfony/commit/603956979c5e413bd96fca1cb6ed38bdf185e321 "603956979c5e413bd96fca1cb6ed38bdf185e321 commit on github"), [ac1448f](http://github.com/symfony/symfony/commit/ac1448f573c7918b01b13bdc57bcbf0377d5907a "ac1448f573c7918b01b13bdc57bcbf0377d5907a commit on github"), [4f9060c](http://github.com/symfony/symfony/commit/4f9060c929ec679fd43380726d4f86d2bdfe987b "4f9060c929ec679fd43380726d4f86d2bdfe987b commit on github"): [Routing] 「#」と「?」のエスケープ文字を追加
  * [6786e81](http://github.com/symfony/symfony/commit/6786e81f6111139f8e11bae25f0810f6c0b6408f "6786e81f6111139f8e11bae25f0810f6c0b6408f commit on github"): [HttpFoundation] UploadedFileにコードをまとめる
  * [76a5816](http://github.com/symfony/symfony/commit/76a5816d609133c33f8f9085525f4afeed11a5aa "76a5816d609133c33f8f9085525f4afeed11a5aa commit on github"): [HttpKernel] 例外のスタックトレースのフラット化の再帰処理の修正
  * [bb1b480](http://github.com/symfony/symfony/commit/bb1b48046ddf5b100443ce307e32337a5a0a8314 "bb1b48046ddf5b100443ce307e32337a5a0a8314 commit on github"): [Translation] CsvFileLoaderのためのCSVのコントロールの追加
  * [df57e0f](http://github.com/symfony/symfony/commit/df57e0fe9aed32dbed94e418f3738284857c85fb "df57e0fe9aed32dbed94e418f3738284857c85fb commit on github"): [Validator] ChoiceConstraintにstrictオプションの追加
  * [28be194](http://github.com/symfony/symfony/commit/28be19461b92d65642b79c87cf97b90406b2b0e8 "28be19461b92d65642b79c87cf97b90406b2b0e8 commit on github"): Monologを1.0.0に更新
  * [8cba490](http://github.com/symfony/symfony/commit/8cba4903d8c64372476dabdbc74cc73db90b958d "8cba4903d8c64372476dabdbc74cc73db90b958d commit on github"): [Process] 最近の変更後に動作しなくなっているようなので回避策を削除
  * [08b4219](http://github.com/symfony/symfony/commit/08b42193471e40682fc04b28a6cf8b77ef455fc9 "08b42193471e40682fc04b28a6cf8b77ef455fc9 commit on github"): [DoctrineBridge] ユニークバリデータは、NULL値では動作しないように修正
  * [9714cfc](http://github.com/symfony/symfony/commit/9714cfc4f9645b68773ddcbb1e82aa3d6f0b8615 "9714cfc4f9645b68773ddcbb1e82aa3d6f0b8615 commit on github"): 国際モジュールがインストールされていない時の致命的なエラーを修正



