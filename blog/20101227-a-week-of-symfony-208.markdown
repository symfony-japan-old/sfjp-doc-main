A week of symfony #208 (20->26 December 2010)
=============================================

今週はフォームとバリデーションのコンポーネントを大きく更新しました。
新しいロケールコンポーネント用のリファクタリングしたコードを取り込み、新しいフィールドと制約の実装を行ないました。
また、Doctrineのプロジェクトで[Doctrine 2.0の最初の安定板](http://www.doctrine-project.org/blog/doctrine2-released)
が公開されました。
 
開発メーリングリスト
------------------------

  * [\[Symfony2\](https://groups.google.com/forum/#!topic/symfony-devs/x1_Z_Zd7h7A) パラメータコンバータ]
  * [\[Symfony2\](https://groups.google.com/forum/#!topic/symfony-devs/gAxmTpsSzts) セキュリティコンポーネント: どのように自分のファイヤーウォールを実装する?]
  * [\[Symfony2\](https://groups.google.com/forum/#!topic/symfony-devs/KS4dfw9dOm4) Twigテンプレートの_view変数について]
  * [\[Symfony2\](https://groups.google.com/forum/#!topic/symfony-devs/JyCXxVMBbkE) ログインが必要な機能テスト]

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [242be93](http://github.com/symfony/symfony/commit/242be933d5cd73fed2049a29ed8c5ae069320e47 "242be933d5cd73fed2049a29ed8c5ae069320e47 commit on github"): \[Form\] FileFieldに適切なエラーハンドリングを追加
  * [b8ef7e7](http://github.com/symfony/symfony/commit/b8ef7e7332a93886b7327c32790bf185320202ab "b8ef7e7332a93886b7327c32790bf185320202ab commit on github"): \[Form\] property pathsの仕様の改善とFieldGroup::merge()の削除
  * [7c557d0](http://github.com/symfony/symfony/commit/7c557d0d6e6d174f8b9dbccc1d6f42b97d840985 "7c557d0d6e6d174f8b9dbccc1d6f42b97d840985 commit on github"): \[Form\] コンストラクタの「$data」「$validator」パラメータの指定を任意に変更
  * [78b6987](http://github.com/symfony/symfony/commit/78b69876d4524cafaaf418f23b0e391eab6eac91 "78b69876d4524cafaaf418f23b0e391eab6eac91 commit on github"): \[Form\] ロケールを変更した際にフィールドステータスの更新に多くの問題が発生するため、フォーム/フィールドを生成前にロケールを静的に設定可能にする
  * [9db7db4](http://github.com/symfony/symfony/commit/9db7db4439d4123464c6c86582a9708fa0101964 "9db7db4439d4123464c6c86582a9708fa0101964 commit on github"): \[Form\] CountryFieldの実装
  * [93d3716](http://github.com/symfony/symfony/commit/93d3716a8492aaa2590dc4f076de44f666dce26f "93d3716a8492aaa2590dc4f076de44f666dce26f commit on github"): \[Form\] LanguageFieldの実装
  * [fdb7f84](http://github.com/symfony/symfony/commit/fdb7f84c7def4f11fa66d12a2b7e57f3cb229bf9 "fdb7f84c7def4f11fa66d12a2b7e57f3cb229bf9 commit on github"): \[Locale, Form, Validator\] 新しいロケールコンポーネントコードのリファクタリングと, Countryの制約の実装
  * [993257a](http://github.com/symfony/symfony/commit/993257a83eb172310a2cdd76b3931f75cd810654 "993257a83eb172310a2cdd76b3931f75cd810654 commit on github"): \[Validator\] Languageの制約の実装
  * [a059ec8](http://github.com/symfony/symfony/commit/a059ec891dac89e9cae177c4d06ac1b60c6b5616 "a059ec891dac89e9cae177c4d06ac1b60c6b5616 commit on github"): \[Validator\] Imageの制約の実装
  * [4f46235](http://github.com/symfony/symfony/commit/4f46235ab0f93cdeb1b2a608e934df25bd19faaf "4f46235ab0f93cdeb1b2a608e934df25bd19faaf commit on github"): \[HttpFoundation\] デフォルトのtext/htmlヘッダと共に適切な文字コードを送信
  * [cd64046](http://github.com/symfony/symfony/commit/cd640468113eae70ecf2312deba40c260ba030de "cd640468113eae70ecf2312deba40c260ba030de commit on github"): \[Form\] PasswordFieldの"always_empty"オプションの意味の変更
  * [df6ffbb](http://github.com/symfony/symfony/commit/df6ffbbf070faf70f64433b9dafbafa2dbff660d "df6ffbbf070faf70f64433b9dafbafa2dbff660d commit on github"): ユーザプロパイダ名の削除
  * [b57411b](http://github.com/symfony/symfony/commit/b57411b5ec734c02451a9f7641d3b9d13bd838fb "b57411b5ec734c02451a9f7641d3b9d13bd838fb commit on github"): reloadUserByAccount()からloadUserByAccount()へ名称の変更
  * [faac8e6](http://github.com/symfony/symfony/commit/faac8e6ffdc9ce295250445d5a1eeadc6a939845 "faac8e6ffdc9ce295250445d5a1eeadc6a939845 commit on github"): \[TwigBundle\] ifroleタグをhas_role関数に置換
  * [d935df0](http://github.com/symfony/symfony/commit/d935df036cf8b592167afef7bef85b632b2a6e47 "d935df036cf8b592167afef7bef85b632b2a6e47 commit on github"): \[TwigBundle\] 未使用のタグとtwigのContentTagの削除
  * [5d65f3e](http://github.com/symfony/symfony/commit/5d65f3edbd8333cfefc16758a58a55d673b4c835 "5d65f3edbd8333cfefc16758a58a55d673b4c835 commit on github"): \[TwigBundle\] パスの変換をurlタグから関数へ変更
  * [d87c3c5](http://github.com/symfony/symfony/commit/d87c3c581cf401654d99cfc418a924e071094819 "d87c3c581cf401654d99cfc418a924e071094819 commit on github"): \[FrameworkBundle\] PdoSessionStorageのための設定値を追加
  * [5e94807](http://github.com/symfony/symfony/commit/5e948076687091b44e8f5b11ed1f3213e8211e81 "5e948076687091b44e8f5b11ed1f3213e8211e81 commit on github"): 値が指定されてないルートのurlマッチングの高速化
  * [a2105d4](http://github.com/symfony/symfony/commit/a2105d44aad351e2e1d302e7a385883428480a96 "a2105d44aad351e2e1d302e7a385883428480a96 commit on github"): わずかなコンパイラリファクタリング
  * [094d428](http://github.com/symfony/symfony/commit/094d428e68a0273b7c123999ee804755593836dc "094d428e68a0273b7c123999ee804755593836dc commit on github"), [3d9b13f](http://github.com/symfony/symfony/commit/3d9b13f240ce0ae178c0f42767c59728ecd80e71 "3d9b13f240ce0ae178c0f42767c59728ecd80e71 commit on github"): 等価比較で右側に値を置くように統一
  * [c54f6d8](http://github.com/symfony/symfony/commit/c54f6d81df02905ab7067bc44213ab39b1403c79 "c54f6d81df02905ab7067bc44213ab39b1403c79 commit on github"): DoctrineMongoDBBundleが最新版のDoctrineで動作するように修正
  * [03d25cc](http://github.com/symfony/symfony/commit/03d25cc7faf6755ae7ae737a66527d58168aaa55 "03d25cc7faf6755ae7ae737a66527d58168aaa55 commit on github"): 新しく追加されたcompiler passesを利用してaccess decision managerをリファクタリング

  * [32aef96](http://github.com/symfony/symfony/commit/32aef9644134f375f67e5685c4ffd48ea40536e3 "32aef9644134f375f67e5685c4ffd48ea40536e3 commit on github"): \[Routing\] setDefaultAnnotationNamespace()の呼び出しを削除しinjected readerで構成することができるようになります。
  * [763ef35](http://github.com/symfony/symfony/commit/763ef35d0e9c627dbf22cab8d32b79af80b288cb "763ef35d0e9c627dbf22cab8d32b79af80b288cb commit on github"): \[Routing\] annotations loaderにファイルリソースの作成を追加

