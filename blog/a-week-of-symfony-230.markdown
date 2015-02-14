---
layout: default
title: A week of symfony #230 (23->29 May 2011)
---

A week of symfony #230 (23->29 May 2011)
========================================

予想よりもはるかに時間がかかりましたが、今週 Symfony2 の2つのベータバージョンがリリースされました。beta2 は[beta1 から大きな飛躍を遂げ](https://github.com/symfony/symfony/compare/v2.0.0BETA1...v2.0.0BETA2)、beta3 は[たくさんのバグを修正しました](https://github.com/symfony/symfony/compare/v2.0.0BETA2...v2.0.0BETA3)。いまだに成長を続ける [Symfony2 の貢献者のリスト](http://symfony.com/contributors)のおかげでこのすさまじい開発活動が実現されました。今週は[ドキュメントチーム](https://github.com/symfony/symfony-docs/commits/master) も Symfony2 の開発に合わせて一生懸命に作業を行いました。
開発 ML
-------

  * [Doctrine Common 3.0 Annotation Reader AnnotationException](https://groups.google.com/forum/#!topic/symfony-devs/iVFlMukBxNU)
  * [\[Symfony2\] フォームのラベル翻訳におけるカスタムドメイン](https://groups.google.com/forum/#!topic/symfony-devs/gZ0HnRP7JDM)
  * [RFC: アノテーションの改善](https://groups.google.com/forum/#!topic/symfony-devs/VRgxOyf0_-w)
  * [PHP おいてルーティングのインポートが動かない](https://groups.google.com/forum/#!topic/symfony-devs/8IFnPbIb6jc)

Symfony2 の開発ハイライト
-------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [2cecc95](http://github.com/symfony/symfony/commit/2cecc95d9e789d39921d5ca7153b52adb6aefba7 "2cecc95d9e789d39921d5ca7153b52adb6aefba7 commit on github"): \[BrowserKit\] Cookie の生の値を扱えるようにしました
  * [7ab3fde](http://github.com/symfony/symfony/commit/7ab3fdeb8325d5a72c44dc73214c97f366a11c4c "7ab3fdeb8325d5a72c44dc73214c97f366a11c4c commit on github"): \[Finder\] すべての「隠し」ファイル (訳注: バージョン管理ツールのメタデータなど) を無視する方法を追加しました
  * [e9548dc](http://github.com/symfony/symfony/commit/e9548dc80c97d90480fac4919c70eddd240ae042 "e9548dc80c97d90480fac4919c70eddd240ae042 commit on github"): \[Assetic\] assetic filter jpegtran のコンフィグの中で setOptimize メソッド呼び出しを追加しました
  * [de61474](http://github.com/symfony/symfony/commit/de61474cb73801dd7d17003cb911ea1c6439fe4f "de61474cb73801dd7d17003cb911ea1c6439fe4f commit on github"): vendors.sh の拡張子を php に変更しました
  * [15bede5](http://github.com/symfony/symfony/commit/15bede5a634c996191d1929caaacaa7e42cf18d0 "15bede5a634c996191d1929caaacaa7e42cf18d0 commit on github"): \[Console\] スタイルをマネジメントする箇所をリファクタリングしました (スタイルがインラインで定義された場合、現在のコードは壊れました)
  * [b6ce137](http://github.com/symfony/symfony/commit/b6ce137e2d3becc8919e7b6af1cecfa8d3d1333b "b6ce137e2d3becc8919e7b6af1cecfa8d3d1333b commit on github"): \[DependencyInjection\] サービスの定義からインラインのプライベートサービスを作成しました
  * [3cdf371](http://github.com/symfony/symfony/commit/3cdf371c2beb1f49aa99cb4b030097f0f8ae5d31 "3cdf371c2beb1f49aa99cb4b030097f0f8ae5d31 commit on github"): \[TwigBundle\] {% render ... %} ノードを専用のエクステンションに移動させ、サービスコンテナを削除しました
  * [73bd9c7](http://github.com/symfony/symfony/commit/73bd9c72afe95b9d8769549bfa0bedfb74645dcf "73bd9c72afe95b9d8769549bfa0bedfb74645dcf commit on github"): \[TwigBundle\] ActionsExtension の依存関係をアクションヘルパーに変更しました
  * [f83c137](http://github.com/symfony/symfony/commit/f83c1376a1796b7a08c704c97bf0186b8699c31f "f83c1376a1796b7a08c704c97bf0186b8699c31f commit on github"): \[TwigBundle\] コードフィルタを専用のエクステンションに移動させました
  * [f13798f](http://github.com/symfony/symfony/commit/f13798fa5e28b151eaa3387ad23aa60b1d63cc2f "f13798fa5e28b151eaa3387ad23aa60b1d63cc2f commit on github"): \[TwigBundle\] TemplatingExtension を AssetsExtension にリネームしました (差し戻し)
  * [dfdd26d](http://github.com/symfony/symfony/commit/dfdd26d6c45b0f45d3dce4bc61a38838e04f1b2c "dfdd26d6c45b0f45d3dce4bc61a38838e04f1b2c commit on github"): \[TwigBundle\] すべてのクラス名を DIC のパラメータに移動させました
  * [1744c86](http://github.com/symfony/symfony/commit/1744c86c18c2ffae944bb2289ae166bb4a2e49b6 "1744c86c18c2ffae944bb2289ae166bb4a2e49b6 commit on github"): assetic フィルタのコンフィグのオプションのためのメソッド呼び出しを追加しました
  * [afe6005](http://github.com/symfony/symfony/commit/afe6005f49be20b302da9f7b5398d1a58e837a86 "afe6005f49be20b302da9f7b5398d1a58e837a86 commit on github"): \[SecurityBundle\] セキュリティのファクトリを任意のコンフィグフォーマットで使えるようにするためにローダーを DelegatingLoader に変更しました
  * [aa356e7](http://github.com/symfony/symfony/commit/aa356e7288a4abb7037946ce6da9feed0162f711 "aa356e7288a4abb7037946ce6da9feed0162f711 commit on github"): \[BrowserKit\] Cookie の管理方法を修正しました (RFC 2109 をご参照ください)
  * [6c409ca](http://github.com/symfony/symfony/commit/6c409cac84da02ac2656b889891d089ffd62d41b "6c409cac84da02ac2656b889891d089ffd62d41b commit on github"): \[DependencyInjection\] パラメータバグパラメータの置き換えをリファクタリングしました (重複したコードを削除しました)
  * [456eb53](http://github.com/symfony/symfony/commit/456eb53eb8f71c837c14cd18964b0d86025507cd "456eb53eb8f71c837c14cd18964b0d86025507cd commit on github"): \[DependencyInjection\] CircularReferenceException を ServiceCircularReferenceException にリネームしました
  * [6504797](http://github.com/symfony/symfony/commit/650479735be54b403cf40cba81da4c0686eb85d9 "650479735be54b403cf40cba81da4c0686eb85d9 commit on github"), [512eb53](http://github.com/symfony/symfony/commit/512eb5378a20975b09e5c781e9a4947af71c9e0f "512eb5378a20975b09e5c781e9a4947af71c9e0f commit on github"), [946f68e](http://github.com/symfony/symfony/commit/946f68e0294812d65ee0a0b102adbc4f9e4298e7 "946f68e0294812d65ee0a0b102adbc4f9e4298e7 commit on github"): \[DoctrineBundle\] generate:entities と mapping:importing の Doctrine コマンドに 'force' と 'annotate' オプションを追加しました
  * [2438a73](http://github.com/symfony/symfony/commit/2438a73c7baf05e69edfb91e52ba1e55c422286e "2438a73c7baf05e69edfb91e52ba1e55c422286e commit on github"): \[DependencyInjection\] パラメータ定義の中の循環参照のチェックを追加しました
  * [3ea2a32](http://github.com/symfony/symfony/commit/3ea2a32c5334dbff66faf8036cec33955e7d52a0 "3ea2a32c5334dbff66faf8036cec33955e7d52a0 commit on github"): \[Validator\] バリデータの制約をリファクタリングしました: getTargets() の定義の必要性はなくし、抽象メソッドの Constraint::getTargets() を バリデータの95％が使う通常のメソッドに置き換え、Constraint\Valid の中で使われていない use 文を削除し、テストを追加しました
  * [dcd490e](http://github.com/symfony/symfony/commit/dcd490e03f5ff2e0a0ee2b5a657e6f2354e33ff9 "dcd490e03f5ff2e0a0ee2b5a657e6f2354e33ff9 commit on github"): \[Twig\] トランスメッセージの文字列の中で % を扱う方法を追加しました
  * [08e7629](http://github.com/symfony/symfony/commit/08e7629fb429e84a22bf69713fb5a78abdc58a13 "08e7629fb429e84a22bf69713fb5a78abdc58a13 commit on github"): \[DomCrawler\] 内部で使われている HTTP メソッドの名前を大文字に変更しました
  * [f019541](http://github.com/symfony/symfony/commit/f01954171636b3f2b793eb4e562fa5c99cf49e5f "f01954171636b3f2b793eb4e562fa5c99cf49e5f commit on github"): Request::getHttpHost() の中の壊れたロジックを修正しました。以前は HTTP_HOST を完全に無視していました。
  * [3c372d3](http://github.com/symfony/symfony/commit/3c372d3773ba845a3778ed77f45a9163e0a294c8 "3c372d3773ba845a3778ed77f45a9163e0a294c8 commit on github"): \[BrowserKit\] URL によって書き換えられる明示的な Cookie パラメータを修正しました
  * [3bdb7c2](http://github.com/symfony/symfony/commit/3bdb7c2b571c298f6ff4177667e8a59e7477eefe "3bdb7c2b571c298f6ff4177667e8a59e7477eefe commit on github"): \[DependencyInjection\] パラメータにエスケープされた % が含まれている場合の回帰を修正しました (注: 潜在的な問題が含まれており、完璧な対策ではありませんとコミットログにあります)
  * [a046259](http://github.com/symfony/symfony/commit/a0462593ebca5f8c3af98354d1f250ffe758be64 "a0462593ebca5f8c3af98354d1f250ffe758be64 commit on github"): \[DoctrineBundle\] Doctrine のコマンドからコードを抽出しました
  * [5ed136b](http://github.com/symfony/symfony/commit/5ed136b3f18adc2c4f43baecaf9d113d615e6a34 "5ed136b3f18adc2c4f43baecaf9d113d615e6a34 commit on github"): \[SwiftMailer\] コンフィギュレーションを最適化しました: Swift_Mailer オブジェクトを取得するときの init.php ファイルの要件を削除し、メールが送信されていない場合に Swift Mailer をロードすることを避けるようにようにデータコレクタを変更しました
  * [1ca4dca](http://github.com/symfony/symfony/commit/1ca4dcad91aae10de4e3d5114211f80329fadf2e "1ca4dcad91aae10de4e3d5114211f80329fadf2e commit on github"): \[SecurityBundle\] ファンクショナルテストスイートをブートストラップしました
  * [fb9d951](http://github.com/symfony/symfony/commit/fb9d951b1d220a3a84a0228ca2fee7c7b8883bd5 "fb9d951b1d220a3a84a0228ca2fee7c7b8883bd5 commit on github"): グループにまとめられたエンティティをサポートするように EntityChoiceList を修正しました
  * [a0397f9](http://github.com/symfony/symfony/commit/a0397f99f5a6f0ed43b23da4ea5480c83822182b "a0397f99f5a6f0ed43b23da4ea5480c83822182b commit on github"): \[DependencyInjection\] (同じベース名をもつ) 2つの異なる XML ファイルからの特定サービスが衝突する可能性があるバグを修正しました
  * [4f0214e](http://github.com/symfony/symfony/commit/4f0214eff410412204961553b2802be3acabd456 "4f0214eff410412204961553b2802be3acabd456 commit on github"): \[Routing\] PhpFileLoader クラスにおいてカレントディレクトリをセットするタイミングが遅すぎるバグを修正しました
  * [15c5d61](http://github.com/symfony/symfony/commit/15c5d61af890b597b7722248bd6bf4b2be9eb3ff "15c5d61af890b597b7722248bd6bf4b2be9eb3ff commit on github"): 定義をコピーする代わりに translator.real のエイリアスを使うように修正しました
