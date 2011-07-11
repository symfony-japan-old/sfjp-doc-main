A week of symfony #235 (27 June -> 3 July 2011)
===============================================

今週のSymfony2は2つのリリース候補バージョンを公開しました。いくつかの小さなバグと回帰バグを修正しました。Symfony 1.4 ブランチも新しいメンテナンスバージョンをリリースしました。
 
開発ML
------------------------

  * [Doctrineと非公開属性](https://groups.google.com/forum/#!topic/symfony-devs/tDmPMR-RHiw)
  * [Symfony2アプリケーションのパッケージング](https://groups.google.com/forum/#!topic/symfony-devs/7obkjZo-0Kw)
  * [アノテーションの問題](https://groups.google.com/forum/#!topic/symfony-devs/iGmw0ply2Wc)

Symfony2開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [c3bb214](http://github.com/symfony/symfony/commit/c3bb214e94c1a76a796ff05cb3b001f373ce3116 "c3bb214e94c1a76a796ff05cb3b001f373ce3116 commit on github"): \[DependencyInjection\] protected と private プロパティの挿入を削除
  * [761724a](http://github.com/symfony/symfony/commit/761724ae57d07cee2368bee86a2f1fe22cf188fc "761724ae57d07cee2368bee86a2f1fe22cf188fc commit on github"): \[Routing\] URLエスケープのルールを調整し、 + と % だけは生成されたルート(route)ではエンコードされるように修正
  * [2b5e22d](http://github.com/symfony/symfony/commit/2b5e22d961f4c9e1d8f225da2bac856a0ba299c2 "2b5e22d961f4c9e1d8f225da2bac856a0ba299c2 commit on github"): \[Routing\] デフォルト値に空白文字が現れたときの ApacheDumper を修正
  * [418d6a0](http://github.com/symfony/symfony/commit/418d6a0ead41b5b27cb6dfa6e1e32edc688ce7ed "418d6a0ead41b5b27cb6dfa6e1e32edc688ce7ed commit on github"): \[Routing\] requirementやpatterの中でシングルクォートを含むルート(route)をダンプするときの文法エラーを修正
  * [4e7b16f](http://github.com/symfony/symfony/commit/4e7b16f7692748164c3fe656248337d06ec68019 "4e7b16f7692748164c3fe656248337d06ec68019 commit on github"): widget_choice_optionsブロックの中のラベルに'trans' Twig フィルタを追加
  * [339ad86](http://github.com/symfony/symfony/commit/339ad861bb80f8191c4e0957e91a2d61f07e017e "339ad861bb80f8191c4e0957e91a2d61f07e017e commit on github"): フォームテンプレート内で存在しないトランスレータの呼び出しを追加
  * [a724774](http://github.com/symfony/symfony/commit/a724774fc003cc5df8e23f88812f25042088344b "a724774fc003cc5df8e23f88812f25042088344b commit on github"): \[Form\] コールバックによってchoice constraintが定義されたときの推測アルゴリズム(guesser)を修正
  * [fb4dea6](http://github.com/symfony/symfony/commit/fb4dea6015561206f8c9e87a1e7a27caa915d4a1 "fb4dea6015561206f8c9e87a1e7a27caa915d4a1 commit on github"): \[Config\] リソースが読み込めないときの例外メッセージを微調整
