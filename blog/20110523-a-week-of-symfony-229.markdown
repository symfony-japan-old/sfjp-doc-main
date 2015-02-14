---
layout: default
title: A week of symfony #229 (16->22 May 2011)
---

A week of symfony #229 (16->22 May 2011)
========================================

今週の Symfony2 の開発は注目に値するマイルストーンを達成しました: [公式リポジトリ](https://github.com/symfony/symfony) は1,000回目のプルリクエストを受け付けました。そして、 Doctrine ブリッジに便利なユニークかどうかを確認するバリデーターが追加されたり、フォームコンポーネントの名前が変更されたり、プロパティーやメソッドをより単純化したり削除されたり、多くの例外が別のコンポーネントに移動し名前が変更されました。

開発ML
------------------------

  * [レガシーなフォームフレームワーク](https://groups.google.com/forum/#!topic/symfony-devs/eqB_lxCAGao)
  * [Web デバッグツールバーの無効化](https://groups.google.com/forum/#!topic/symfony-devs/0FdwdUMOYIk)
  * [entity_managers でエンティティのアノテーションマッピングができません](https://groups.google.com/forum/#!topic/symfony-devs/Z3laiY5vtJM)
  * [\[Symfony2\] スタンダードエディションに含まれるバンドルは何?](https://groups.google.com/forum/#!topic/symfony-devs/1hfNaN_rXxM)
  * [泡のようなバンドルのリソース配置 (Bundles Resources location bubbling)](https://groups.google.com/forum/#!topic/symfony-devs/XyPP2wAgkug)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [39efc49](http://github.com/symfony/symfony/commit/39efc49da0c7658de9dc1c669586a5cba0d682aa "39efc49da0c7658de9dc1c669586a5cba0d682aa commit on github"): \[Form\] FormView にメソッドチェーンの実装
  * [336c57d](http://github.com/symfony/symfony/commit/336c57d56f31cdab4668c7e2c62925867f167d6c "336c57d56f31cdab4668c7e2c62925867f167d6c commit on github"): \[DoctrineBundle\] doctrine:schema:* コマンドの説明のリファクタリング
  * [e7e5304](http://github.com/symfony/symfony/commit/e7e53048763edce79f1e21ab1898ada65318883c "e7e53048763edce79f1e21ab1898ada65318883c commit on github"): 全てのレスポンスに Date ヘッダー(RFC2616 - 14.18)を強制
  * [663f8a0](http://github.com/symfony/symfony/commit/663f8a052edfcd33373868ad1a5c9d6feff68fd2 "663f8a052edfcd33373868ad1a5c9d6feff68fd2 commit on github"): \[AsseticBundle\] cssembed　フィルターのための設定追加
  * [914620f](http://github.com/symfony/symfony/commit/914620f9484c22a7fed95ef9c405e6ae907c1880 "914620f9484c22a7fed95ef9c405e6ae907c1880 commit on github"), [b645278](http://github.com/symfony/symfony/commit/b645278f8b59ad9bffd13ccfdbb86d828264f737 "b645278f8b59ad9bffd13ccfdbb86d828264f737 commit on github"): \[Form, Security\] CSRF の page_id を intention に変更
  * [02e77ec](http://github.com/symfony/symfony/commit/02e77ec4e373ae3e6b5d15b3b3e05deb0bf6d698 "02e77ec4e373ae3e6b5d15b3b3e05deb0bf6d698 commit on github"): \[Routing\] Matcher 例外を移動
  * [b7c417f](http://github.com/symfony/symfony/commit/b7c417feaa7439567b4cdcea3546f8662a11e299 "b7c417feaa7439567b4cdcea3546f8662a11e299 commit on github"): \[Bridge/Twig\] transchoice タグにメッセージを渡せるように移動
  * [0168241](http://github.com/symfony/symfony/commit/0168241014a042a6ac676da95f5257205c652088 "0168241014a042a6ac676da95f5257205c652088 commit on github"): \[DependencyInjection\] NonExistentParameterException と NonExistentServiceException を ParameterNotFoundException と ServiceNotFoundException に名前を変更
  * [2cd0454](http://github.com/symfony/symfony/commit/2cd04547fdb99cdaf19d882a381cb71e3e33655e "2cd04547fdb99cdaf19d882a381cb71e3e33655e commit on github"): \[Routing\] 一部の例外の名前を変更
  * [1a49296](http://github.com/symfony/symfony/commit/1a49296b59c60e8bfba2a193a141f0d0fce5498a "1a49296b59c60e8bfba2a193a141f0d0fce5498a commit on github"): \[FrameworkBundle\] パラメーターではなく replaceArgument() を使うようにエクステンションを更新
  * [84d5cbf](http://github.com/symfony/symfony/commit/84d5cbfba841de5136352282001d6aeed8a86aaa "84d5cbfba841de5136352282001d6aeed8a86aaa commit on github"): \[AsseticBundle\] --force オプションと assetic:dump --watch　を追加
  * [e65a453](http://github.com/symfony/symfony/commit/e65a4535b55725e8e5364d124b04c9cbfb8408a1 "e65a4535b55725e8e5364d124b04c9cbfb8408a1 commit on github"): \[AsseticBundle\] コマンドのオプションに --watch を追加
  * [cfc2471](http://github.com/symfony/symfony/commit/cfc2471109c56fba3678894ab0762c13ab3d1ac5 "cfc2471109c56fba3678894ab0762c13ab3d1ac5 commit on github"), [8ff1d09](http://github.com/symfony/symfony/commit/8ff1d09d3614891ffb1b309913b2eab33ad7040c "8ff1d09d3614891ffb1b309913b2eab33ad7040c commit on github"), [86f9b17](http://github.com/symfony/symfony/commit/86f9b17254253fc086769c45f4c06cd58e23226c "86f9b17254253fc086769c45f4c06cd58e23226c commit on github"), [23cf63d](http://github.com/symfony/symfony/commit/23cf63d7673eb48453ef4d8eb0e05e2d747ce7ea "23cf63d7673eb48453ef4d8eb0e05e2d747ce7ea commit on github"), [a4f1b8a](http://github.com/symfony/symfony/commit/a4f1b8a0c18cd2433d5a5834a0b9179ed8f73156 "a4f1b8a0c18cd2433d5a5834a0b9179ed8f73156 commit on github"): \[Doctrine\] Unique Validator を追加
  * [ba31b5a](http://github.com/symfony/symfony/commit/ba31b5acc5b6a2774013679930b8b0ef4e6eca5d "ba31b5acc5b6a2774013679930b8b0ef4e6eca5d commit on github"): \[Form\] CSRF のオプションをタイプから CSRF エクステンションに移動
  * [ebb0e83](http://github.com/symfony/symfony/commit/ebb0e83a7e1fdeae6d1def51a32578cea835673a "ebb0e83a7e1fdeae6d1def51a32578cea835673a commit on github"): \[Form\] CSRF のドキュメント追加とインデントの変更
  * [0687aad](http://github.com/symfony/symfony/commit/0687aadad2aecdd42990542b53eca471fe3b29bf "0687aadad2aecdd42990542b53eca471fe3b29bf commit on github"): セッションが利用できないときのフォーム設定を修正
  * [a15e846](http://github.com/symfony/symfony/commit/a15e8465682c055d1ee1a779fcbcea3aaa4d3eef "a15e8465682c055d1ee1a779fcbcea3aaa4d3eef commit on github"): フォームを無効にする方法とフォームが有効のときにバリデーションを強制する方法の追加
  * [1f0ffca](http://github.com/symfony/symfony/commit/1f0ffca68e7021b771f43e158cc705b54cac6545 "1f0ffca68e7021b771f43e158cc705b54cac6545 commit on github"): \[HttpKernel\] HTTPCacheを使っているときにリクエスト中に空のEtagが出現するのを修正
  * [b39a21f](http://github.com/symfony/symfony/commit/b39a21fbaf3cd67a229dde0d18b4a14ebbc063e7 "b39a21fbaf3cd67a229dde0d18b4a14ebbc063e7 commit on github"): \[Form\] コレクションのオプションを "type_options" から "option" に変更
  * [f467317](http://github.com/symfony/symfony/commit/f467317bab9d662b5428fca770a4dc8e03690b73 "f467317bab9d662b5428fca770a4dc8e03690b73 commit on github"): \[Form\] ビューの変数を 'name' から 'full_name' に変更. 今の 'name' はローカルで短い名前を含みます。 これは $form->getName() と同じです。
  * [520e376](http://github.com/symfony/symfony/commit/520e3761e93c39002eb52e1b431b5e73e8759c1a "520e3761e93c39002eb52e1b431b5e73e8759c1a commit on github"): \[Form\] 使用していない日付と時刻種別の 'pattern' オプションを削除
  * [a7ff4f4](http://github.com/symfony/symfony/commit/a7ff4f484a6feba4ec9a9a592e96ac33e616c5b6 "a7ff4f484a6feba4ec9a9a592e96ac33e616c5b6 commit on github"): \[Form\] PropertyPath コードをより簡素化
  * [829aa4d](http://github.com/symfony/symfony/commit/829aa4dc0b65dd68e4839619d7f19cddbfd10c35 "829aa4dc0b65dd68e4839619d7f19cddbfd10c35 commit on github"): \[Locale\] エラーレポートの改善と intl_is_failure(), intl_get_error_code() と intl_get_error_message() のためのスタブを追加
  * [13a964a](http://github.com/symfony/symfony/commit/13a964ae6d844e77fdf61d95c352f9299f6750b0 "13a964ae6d844e77fdf61d95c352f9299f6750b0 commit on github"): \[Form\] Form::isBound() と Form::isValid() が 読み込みだけのフォームでも正しく動作するための修正
  * [65ed6f7](http://github.com/symfony/symfony/commit/65ed6f7763fc7b8c13593ad113bb08bc24dccd04 "65ed6f7763fc7b8c13593ad113bb08bc24dccd04 commit on github"): X-HTTP-Method-Override を通して リクエストメソッドを上書きサポート
  * [7eeb945](http://github.com/symfony/symfony/commit/7eeb945a4c7c96f548e41ee905f3ff7f5e65acdc "7eeb945a4c7c96f548e41ee905f3ff7f5e65acdc commit on github"): \[AsseticBundle\] PHP テンプレートのバグ修正と 'combine' オプションの追加
  * [e74c6ed](http://github.com/symfony/symfony/commit/e74c6edc347aab0c9ded69728585100bb9e59abf "e74c6edc347aab0c9ded69728585100bb9e59abf commit on github"): \[AsseticBundle\] packager　フィルターの設定追加
  * [fa248e0](http://github.com/symfony/symfony/commit/fa248e00fb3902aa1571169ab4b0f917f7c17e0d "fa248e00fb3902aa1571169ab4b0f917f7c17e0d commit on github"): \[AsseticBundle\] cssimport　フィルターの設定追加
  * [e6d929a](http://github.com/symfony/symfony/commit/e6d929aa71c55e7c6800203b46ba0498344432d7 "e6d929aa71c55e7c6800203b46ba0498344432d7 commit on github"): \[HttpFoundation\] Cookie　用に __toString() メソッドを追加
  * [f9b6c8b](http://github.com/symfony/symfony/commit/f9b6c8b74a82cd4e5965d5ed8ba368a655ca1bb4 "f9b6c8b74a82cd4e5965d5ed8ba368a655ca1bb4 commit on github"): \[HttpFoundation\] クッキーのヘッダーを文字列で確認できるように追加
  * [fd6c254](http://github.com/symfony/symfony/commit/fd6c254b475c9d502b921e40efeb0ce736ac82e8 "fd6c254b475c9d502b921e40efeb0ce736ac82e8 commit on github"): \[HttpFoundation\] setcookie()　で確認される消去されたクッキーの確認方法を変更
  * [5ad2ff0](http://github.com/symfony/symfony/commit/5ad2ff05958668701799fa3142532175df829fea "5ad2ff05958668701799fa3142532175df829fea commit on github"): \[Console\] DialogHelper::askAndValidate()　に標準の値を渡せるように追加
  * [f3b92cb](http://github.com/symfony/symfony/commit/f3b92cb1ad2ffcc6044ac5e6a0e59cb67ed2373f "f3b92cb1ad2ffcc6044ac5e6a0e59cb67ed2373f commit on github"): \[FrameworkBundle\] Mustache　を Generator に名前変更し、 新しい Generator のサブ名前空間に移動
  * [e0ff7d2](http://github.com/symfony/symfony/commit/e0ff7d2613c92df8fd9585b5145814613061dc36 "e0ff7d2613c92df8fd9585b5145814613061dc36 commit on github"): \[Form\] フィールドタイプの修正
  * [eb10c66](http://github.com/symfony/symfony/commit/eb10c66a55ad38003ff1e251925bc42a98504c7c "eb10c66a55ad38003ff1e251925bc42a98504c7c commit on github"): \[Twig/Form\] フォームのレンダリングの最適化
