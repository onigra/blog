# sentry-moduleで学ぶ、Nuxt Modules入門

エラーハンドリング

https://ja.nuxtjs.org/guide/modules/

https://github.com/nuxt/nuxt.js/issues/1688


sentry
https://github.com/nuxt-community/sentry-module
https://github.com/getsentry/raven-js
https://docs.sentry.io/clients/javascript/integrations/vue/
https://github.com/getsentry/raven-node

注: JavaScriptのSentry Clientのライブラリ名

# Sentryってご存知ですか？

https://sentry.io/welcome/

アプリケーションのエラートラッキングツールで、アプリケーション内でthrowされたエラーをトラッキングし、
エラー情報を詳細に拾ってまとめてくれる便利なやつです。

類似サービスに[Rollbar](https://rollbar.com/)、[bugsnag](https://www.bugsnag.com/)、[Airbrake](https://airbrake.io/)などがあります。

# SentryをVue.jsで使用するには

公式でVueプラグインが用意されており、インストールは非常に簡単です。

https://docs.sentry.io/clients/javascript/integrations/vue/

クライアントキーを発行し、ドキュメントの通りにプラグインを追加する記述をするだけで導入ができます。
プラグインで既に `[Vue.config.errorHandler](https://jp.vuejs.org/v2/api/index.html#errorHandler)` を使ってSetnryクライアントを呼び出すようになってるので、
新たに `Vue.config.errorHandler` 内に何か書く必要も無い。

# ブラウザ側はこれで問題ないが...

Nuxt.jsでSSRを使う場合、サーバサイド側のプロセスのエラートラッキングができない。


