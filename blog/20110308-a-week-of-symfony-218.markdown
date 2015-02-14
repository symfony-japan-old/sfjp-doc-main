---
layout: default
title: A week of symfony #218 (28 February -> 6 March 2011)
---

A week of symfony #218 (28 February -> 6 March 2011)
====================================================

symfonyプロジェクトにとってなんとすばらしい週だったことでしょう！ [たくさんの開発者達](http://www.flickr.com/search/?q=sflive2011&s=rec&z=t) が [Symfony Live 2011](http://www.symfony-live.com/paris) カンファレンスのためにパリに集まりました。 [多くのテクニカルセッション](https://docs.google.com/document/pub?id=1rXrCNX25JArMq5TEHJOFiJjnmsKjRX4JpUoFxTXqob0) に参加し、 [Symfony2の未来](http://trac.symfony-project.org/wiki/SfliveParisDevMeeting) について語り合い、他のコミュニティメンバーと交流を持ちました。

[ディストリビューションベース](http://symfony.com/distributions) の、新しい Symfony2 のダウンロードとインストールの方法がカンファレンス中に発表されました。さらに、閉会のキーノートの場では、symfony プロジェクトにより、新しいビジュアルアイデンティティと [symfony.com](http://symfony.com) ドメインが公開されました。この新しいデザインは既に [Symfony2 のコードに適用](http://twitter.com/#!/fabpot/status/44353455271313408) されています。
 
開発メーリングリスト
--------------------

  * [\[Symfony2\] コンポーネントのサードパーティー依存 (再掲)](https://groups.google.com/forum/#!topic/symfony-devs/rknqUKNzFig)
  * [NotFoundHttpException の拡張](https://groups.google.com/forum/#!topic/symfony-devs/UKRV_6PcQwg)

Symfony2 開発ハイライト
-----------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [5683c6e](http://github.com/symfony/symfony/commit/5683c6e6e15d399e442826412914d15a9647e461 "5683c6e6e15d399e442826412914d15a9647e461 commit on github"): \[AsseticBundle\] カスタムストリームラッパー経由でCDNへアセットを書き込むのを促進するため、読み出しと書き込みのパスを分離
  * [0306c9a](http://github.com/symfony/symfony/commit/0306c9aa66955671d530f6ed917a34af6326fcc5 "0306c9aa66955671d530f6ed917a34af6326fcc5 commit on github"), [057e861](http://github.com/symfony/symfony/commit/057e86161e48f99fe7f23c1d50211202fefc2ca2 "057e86161e48f99fe7f23c1d50211202fefc2ca2 commit on github"): ArgvInput内の配列の引数の解析を修正
  * [d57c665](http://github.com/symfony/symfony/commit/d57c6657bda010b6864f81045744f8307b7a84d4 "d57c6657bda010b6864f81045744f8307b7a84d4 commit on github"): \[AsseticBundle\] どのバンドルのフォーミュラからロードされるかを制限する設定オプションを追加
  * [26e7470](http://github.com/symfony/symfony/commit/26e7470eb33adff42202bc20899e5645560b32b9 "26e7470eb33adff42202bc20899e5645560b32b9 commit on github"): \[ZendBundle\] コンパイルのためにクラスを追加
  * [67c886f](http://github.com/symfony/symfony/commit/67c886f3df49a236ef326478565e506002ddd4e1 "67c886f3df49a236ef326478565e506002ddd4e1 commit on github"): \[DependencyInjection/Compiler\] サービスのスコープを勝手に変更するバグを修正
  * [3a47fa6](http://github.com/symfony/symfony/commit/3a47fa6eeddfd51c64de67ec9b83c2ba39a75aaa "3a47fa6eeddfd51c64de67ec9b83c2ba39a75aaa commit on github"): \[Tests\] テストファイルのたくさんの誤字を修正
  * [9283877](http://github.com/symfony/symfony/commit/9283877828c3c11e91ee00f55eab0b3caccc3ccc "9283877828c3c11e91ee00f55eab0b3caccc3ccc commit on github"): \[AsseticBundle\] 機能テストのユニットテストへの移行の進歩
  * [f7b7288](http://github.com/symfony/symfony/commit/f7b7288892f4d2bf6c5aa1dd0f8d71f772d05ab2 "f7b7288892f4d2bf6c5aa1dd0f8d71f772d05ab2 commit on github"): \[AsseticBundle\] ファクトリワーカー向けにコンパイラパスを追加
  * [4a8f101](http://github.com/symfony/symfony/commit/4a8f10192f5bbc781e999677add6d8568335bd03 "4a8f10192f5bbc781e999677add6d8568335bd03 commit on github"): \[DependencyInjection\] phar と suhosin を使用した時のユニットテストを修正
  * [44d069a](http://github.com/symfony/symfony/commit/44d069a3fb4b02639d0b2948bcdce725b0016736 "44d069a3fb4b02639d0b2948bcdce725b0016736 commit on github"): \[HttpKernel\] 各バンドルのメインエクステンションがロードされたことを確実にするため、 MergeExtensionConfigurationPass サブクラスを追加
  * [44d069a](http://github.com/symfony/symfony/commit/44d069a3fb4b02639d0b2948bcdce725b0016736 "44d069a3fb4b02639d0b2948bcdce725b0016736 commit on github"): \[DependencyInjection\] コンフィギュレーションの中で呼び出された場合ロードのみ実行するよう修正
  * [3567fc4](http://github.com/symfony/symfony/commit/3567fc4e6cc56f17a88891b04e8c3ece1c53b35d "3567fc4e6cc56f17a88891b04e8c3ece1c53b35d commit on github"): \[HttpFoundation\] セッションテストを追加
  * [f82b89c](http://github.com/symfony/symfony/commit/f82b89cdc5f13220bf2678825ad9ffd041cafa1a "f82b89cdc5f13220bf2678825ad9ffd041cafa1a commit on github"): \[Security\] MessageDigestEncoder のデフォルト値を変更 (encode_as_base64 が真となり、イテレーションが 1 から 5000に増やされた)
  * [8d4dae9](http://github.com/symfony/symfony/commit/8d4dae9f2ace9dd389c136b4d740910303462069 "8d4dae9f2ace9dd389c136b4d740910303462069 commit on github"): \[AsseticBundle\] PHP テンプレートのサポートの完了と有効化
  * [ed338d9](http://github.com/symfony/symfony/commit/ed338d9422ae9b25d32cc03195c289a50a0edd12 "ed338d9422ae9b25d32cc03195c289a50a0edd12 commit on github"): \[Yaml\] ダブルクォートで囲まれた値のサポート向上 (YAML 1.1 と 1.2 仕様の5章にある、ダブルクォートで囲まれた文字列のエスケープ値を全てサポートするよう追加)
  * [dbde41c](http://github.com/symfony/symfony/commit/dbde41c0829ebb1408a7a522ff24de5b0ae503aa "dbde41c0829ebb1408a7a522ff24de5b0ae503aa commit on github"): \[Security\] シリアライズされた文字列がセッション内に保存されるよう、RememberMeTokenの 'key' 属性を追加
  * [3e7ccae](http://github.com/symfony/symfony/commit/3e7ccae2ba7f03cbf6bec6c26c3591b6cddd1d07 "3e7ccae2ba7f03cbf6bec6c26c3591b6cddd1d07 commit on github"): \[HttpKernel\] デバッグのためにテストを追加
  * [4c54218](http://github.com/symfony/symfony/commit/4c54218a4bf652b224c44bacd1107122571feb6f "4c54218a4bf652b224c44bacd1107122571feb6f commit on github"): \[AsseticBundle\] デバッグモードでアセットのURLを固定
  * [87e1359](http://github.com/symfony/symfony/commit/87e1359ebdcef503f357fc3c7929e6250c1d2323 "87e1359ebdcef503f357fc3c7929e6250c1d2323 commit on github"): \[HttpFoundation\] 有効期限のチェックをより洗練されたかたちに変更
  * [7900e86](http://github.com/symfony/symfony/commit/7900e8624ffaeec6be668b43186e5b37879aecf8 "7900e8624ffaeec6be668b43186e5b37879aecf8 commit on github"): \[HttpFoundation\] レスポンスにさらにいくつかのテストを追加
  * [44b0bbc](http://github.com/symfony/symfony/commit/44b0bbc0d1b64177c08f685eaf4f97e5576a228a "44b0bbc0d1b64177c08f685eaf4f97e5576a228a commit on github"): \[HttpKernel\] DataCollectors のテストを追加
  * [c2e0537](http://github.com/symfony/symfony/commit/c2e0537c31cef79943bb3d53937c7877f152f521 "c2e0537c31cef79943bb3d53937c7877f152f521 commit on github"): キャッシュウォームされたルータのサポートを RouteHelper に追加
  * [f75ec8d](http://github.com/symfony/symfony/commit/f75ec8d4ada912de982d73ef6dedba991922a619 "f75ec8d4ada912de982d73ef6dedba991922a619 commit on github"), [f0e1df2](http://github.com/symfony/symfony/commit/f0e1df26883a94f5189d719573b5c4fc8cd47ac3 "f0e1df26883a94f5189d719573b5c4fc8cd47ac3 commit on github"), [124461c](http://github.com/symfony/symfony/commit/124461cceeedfffcb200e8504f2bda826d8fe39c "124461cceeedfffcb200e8504f2bda826d8fe39c commit on github"), [be8618e](http://github.com/symfony/symfony/commit/be8618ec5661d2106fce2d3c752c30e4906016c5 "be8618ec5661d2106fce2d3c752c30e4906016c5 commit on github"): \[FrameworkBundle\] 新しい冷害のスタックとレースレイアウトを実装
  * [2d68ca4](http://github.com/symfony/symfony/commit/2d68ca4d00e473c6928268bbf46efdf8983227c1 "2d68ca4d00e473c6928268bbf46efdf8983227c1 commit on github"), [a8e882a](http://github.com/symfony/symfony/commit/a8e882ac514097e32f81e1a928fa52b9c266f44e "a8e882ac514097e32f81e1a928fa52b9c266f44e commit on github"), [1134fd1](http://github.com/symfony/symfony/commit/1134fd17ab1d70ab3490d1e66c13c0d9308de435 "1134fd17ab1d70ab3490d1e66c13c0d9308de435 commit on github"), [fcc66ad](http://github.com/symfony/symfony/commit/fcc66ad540d42e17b7955ebfc7e1b6d357703bc8 "fcc66ad540d42e17b7955ebfc7e1b6d357703bc8 commit on github"): \[WebProfilerBundle\] Web デバッグツールバーの CSS レイアウトを変更
  * [d37f52c](http://github.com/symfony/symfony/commit/d37f52c74380b49ca5bf1f4143e550de59a5ea30 "d37f52c74380b49ca5bf1f4143e550de59a5ea30 commit on github"), [e51c46b](http://github.com/symfony/symfony/commit/e51c46b21ae1f846effc0686a9eafd3df0f96ae7 "e51c46b21ae1f846effc0686a9eafd3df0f96ae7 commit on github"), [ce7fddd](http://github.com/symfony/symfony/commit/ce7fddd4ea7cb8113be8d22d73dfb4007f3c0f58 "ce7fddd4ea7cb8113be8d22d73dfb4007f3c0f58 commit on github"), [8367694](http://github.com/symfony/symfony/commit/83676943716fac60b2950178be4ab1d807450069 "83676943716fac60b2950178be4ab1d807450069 commit on github"), [f4f78d4](http://github.com/symfony/symfony/commit/f4f78d47c89ddd81b743a5364f3599af966673b4 "f4f78d47c89ddd81b743a5364f3599af966673b4 commit on github"), [91caf4b](http://github.com/symfony/symfony/commit/91caf4b6e38dd3059571266634f19cf97422f7a4 "91caf4b6e38dd3059571266634f19cf97422f7a4 commit on github"), [0b41116](http://github.com/symfony/symfony/commit/0b41116a7bb801402cc09c7c2734c005546cc7e6 "0b41116a7bb801402cc09c7c2734c005546cc7e6 commit on github"), [659bfc5](http://github.com/symfony/symfony/commit/659bfc5615503c3b140504122c54dfd686a7af76 "659bfc5615503c3b140504122c54dfd686a7af76 commit on github"), [aca2c16](http://github.com/symfony/symfony/commit/aca2c161c8d18be708abd63ec616317df6eecb19 "aca2c161c8d18be708abd63ec616317df6eecb19 commit on github"): \[WebProfilerBundle\] 新しいWebプロファイラのレイアウトを適用

ドキュメンテーション
-------------

  * Symfony Live Paris 開発者ミーティングページ

