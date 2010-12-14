A week of symfony #206 (6->12 December 2010)
============================================

今週、<a href="http://www.symfony-live.com/">Symfony Live 2011 カンファレンス</a>の最終的なスケジュールが発表されました。一方で、Symfony2の開発はちょっとした微調整やコードのリファクタリングに焦点を当てました。
 
開発メーリングリスト
------------------------

  * [積極的なResponseの生成](https://groups.google.com/forum/#topic/symfony-devs/DR4FVYvL4nU)
  * [[Symfony2] セキュリティレイヤの問題](https://groups.google.com/forum/#topic/symfony-devs/EievadAUlRs)
  * [PR4にアップデートした後、不思議な引用符が挿入される](https://groups.google.com/forum/#topic/symfony-devs/Wq-kbj2PysI)
  * [[Symfony2] 複数のフロントエンドコントローラ](https://groups.google.com/forum/#topic/symfony-devs/rt3BI5JqDiw)
  * [[Symfony2] Twigでifroleを無効にする方法とは？](https://groups.google.com/forum/#topic/symfony-devs/QyhaCRp60Us)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [978a14c](http://github.com/symfony/symfony/commit/978a14c5688258f174b7f844c8a0164624ac8186 "978a14c5688258f174b7f844c8a0164624ac8186 commit on github"): \[FrameworkBundle\]ファイアウォール認証リスナを設定可能に修正
  * [db0ddb6](http://github.com/symfony/symfony/commit/db0ddb6e307de79e7f3755e796285e735593aac6 "db0ddb6e307de79e7f3755e796285e735593aac6 commit on github"): \[FrameworkBundle\] テンプレートを提供するためにセキュリティ認証リスナを許可するよう新しいテンプレートタグを追加
  * [7c47fd7](http://github.com/symfony/symfony/commit/7c47fd77ccc4cfd43111fc0ae944c7a98d761df7 "7c47fd77ccc4cfd43111fc0ae944c7a98d761df7 commit on github"): 最近のDoctrine MongoDB ODMの変更でも動作するようにDoctrineMongoDBBundleを修正
  * [714c294](http://github.com/symfony/symfony/commit/714c294f477fef94f6aa0f1447cad7c0f93eee90 "714c294f477fef94f6aa0f1447cad7c0f93eee90 commit on github"), [87aeb0e](http://github.com/symfony/symfony/commit/87aeb0e6033da31dc759046148b2e3cc24cfabf0 "87aeb0e6033da31dc759046148b2e3cc24cfabf0 commit on github"): \[DoctrineBundle\] エンティティとドキュメントマネージャサービスにタグを追加
  * [0b26be1](http://github.com/symfony/symfony/commit/0b26be1765d546bb0b0bd0e29e774aef58ac87df "0b26be1765d546bb0b0bd0e29e774aef58ac87df commit on github"), [53c1f1f](http://github.com/symfony/symfony/commit/53c1f1f509d520f66261abaf38706ff6bd2b4857 "53c1f1f509d520f66261abaf38706ff6bd2b4857 commit on github"): \[DoctrineBundle\] Memcacheの問題を修正
  * [3e02eaf](http://github.com/symfony/symfony/commit/3e02eafc70c4dfe73d9003f36a0e9aa299138d4e "3e02eafc70c4dfe73d9003f36a0e9aa299138d4e commit on github"): PHPUnitのsetUpとtearDownメソッドのアクセス権を修正
  * [a832885](http://github.com/symfony/symfony/commit/a832885960e6f12270af57afe9258ea8e21be7b2 "a832885960e6f12270af57afe9258ea8e21be7b2 commit on github"): \[HttpFoundation\] 単一のIPに限定するよう標準のネットマスクを修正
  * [e867274](http://github.com/symfony/symfony/commit/e8672740c75600835778150df7d467503b84fe6b "e8672740c75600835778150df7d467503b84fe6b commit on github"): \[HttpFoundation\] Requestクラスへの全てのHTTPメソッドを許可
  * [beecd1f](http://github.com/symfony/symfony/commit/beecd1fef8fc2f5d0fd39abee82c3b3b759b4575 "beecd1fef8fc2f5d0fd39abee82c3b3b759b4575 commit on github"): \[HttpKernel\] Cacheクラスのデバッガヘッダ内で、パスと同じようにクエリ文字列もログを取るよう変更
  * [fb41389](http://github.com/symfony/symfony/commit/fb41389999e06f5e912ae7053e996594c645136e "fb41389999e06f5e912ae7053e996594c645136e commit on github"): \[HttpFoundation\] Request::createのフルURIの取り扱いを修正
  * [70a793b](http://github.com/symfony/symfony/commit/70a793b33d3081b178bc6473e1d1d6bc9f654cf6 "70a793b33d3081b178bc6473e1d1d6bc9f654cf6 commit on github"): \[DoctrineBundle\] プロキシのディレクトリを設定可能に修正
  * [50cfd4a](http://github.com/symfony/symfony/commit/50cfd4a7bf7a69512968b752a3b50d38143d5b98 "50cfd4a7bf7a69512968b752a3b50d38143d5b98 commit on github"): \[FrameworkBundle\] シンボリックリンクを張る際にエラーを発生させるのではなくbundlesディレクトリを作成するように修正
  * [eef6578](http://github.com/symfony/symfony/commit/eef6578c15b0dd6de804fd6f46c26029375b4131 "eef6578c15b0dd6de804fd6f46c26029375b4131 commit on github"): 切断されないリスナによるバグを修正
  * [b171ab9](http://github.com/symfony/symfony/commit/b171ab9b7d1994221325936f6b7e50b625055c4e "b171ab9b7d1994221325936f6b7e50b625055c4e commit on github"): PasswordFieldのレンダラを追加
  * [d94420f](http://github.com/symfony/symfony/commit/d94420f3a5e1d2699a7cccabca451b1cc02b4222 "d94420f3a5e1d2699a7cccabca451b1cc02b4222 commit on github"): ログアウトのリファクタリング
  * [2ff474f](http://github.com/symfony/symfony/commit/2ff474fc3a2a49090f4636d6a13620920d702b93 "2ff474fc3a2a49090f4636d6a13620920d702b93 commit on github"), [7eea488](http://github.com/symfony/symfony/commit/7eea4882db8c8876131533ad61791e6d96d7a0d1 "7eea4882db8c8876131533ad61791e6d96d7a0d1 commit on github"): \[HttpKernel, FrameworkBundle\] BaseHttpKernelをHttpKernelに改名。オリジナルのHttpKernelクラスは削除され、そのリクエストスタッシングはKernelクラスに移動
  * [5da423b](http://github.com/symfony/symfony/commit/5da423be204c144554feb053baf482cf91a2e485 "5da423be204c144554feb053baf482cf91a2e485 commit on github"): \[HttpKernel\] HttpKernelInterfaceにgetRequest()を追加
  * [be94dab](http://github.com/symfony/symfony/commit/be94daba6688fe4134dd1ff305e3dd43454d033b "be94daba6688fe4134dd1ff305e3dd43454d033b commit on github"): \[HttpKernel\] 標準のOOクラスとより一貫性があるように、HttpExceptionクラスのコンストラクタを改良
  * [1317760](http://github.com/symfony/symfony/commit/131776001f054ecb4ddf0c161ba4dd22cdb8370f "131776001f054ecb4ddf0c161ba4dd22cdb8370f commit on github"): ForbiddenHttpExceptionを削除 (HttpKernelとSecurityの両方が403エラーを定義しているため)
  * [55bed30](http://github.com/symfony/symfony/commit/55bed307f1e67eda91c50819a00ec3ee42b83db5 "55bed307f1e67eda91c50819a00ec3ee42b83db5 commit on github"): HttpExceptionベースクラスを削除し、FlattenExceptionクラスをリファクタリング
  * [c8c9fba](http://github.com/symfony/symfony/commit/c8c9fba7d92eb6a75b2f90e697bd3f5393325a97 "c8c9fba7d92eb6a75b2f90e697bd3f5393325a97 commit on github"): \[Routing\] リソースの文字列が複数の意味を持つ時のローダのヒントのために、選択可能なtypeパラメータを追加

ドキュメンテーション
-------------

  * <a href="http://trac.symfony-project.org/wiki/IRCLogs20101209">IRC ログ 2010-12-09</a> ページ
