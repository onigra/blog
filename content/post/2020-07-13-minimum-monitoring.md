---
title: "最低限の監視"
comments: true
slug: minimum-monitoring
categories: monitoring
date: 2020-07-13T00:00:00+09:00
---

## 何を監視したいか

- ロードバランサーのレスポンスタイム
  - レスポンスタイムが悪化してないか
- ロードバランサーの5xxの数
  - 短期間に増えてないか
  - リクエスト数に対して5xxの割合
- サーバ、コンテナのCPUの利用率
- サーバ、コンテナのメモリの利用率
- サーバ、コンテナが落ちてないか
  - 希望数に対して何台起動しているか

## Dashboardに置くとそれっぽくなるもの

- ロードバランサーのリクエスト数のカウント
  - 2xx, 4xx, 5xx系のカウントも合わせて出すとそれっぽい
- ロードバランサーのレスポンスタイムのパーセンタイル
  - p99, p95, p90, p50
- ロードバランサーのレスポンスタイム
  - avg, max, min
- サーバ、コンテナごとのCPUの利用率
- サーバ、コンテナごとのメモリの利用率
- サーバ、コンテナの起動数