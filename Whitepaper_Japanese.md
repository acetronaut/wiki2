この文章はhttps://blockchain.aeternity.com/%C3%A6ternity-blockchain-whitepaper.pdf
を翻訳しているものです。2017/5/21現在翻訳中です。

### æternity blockchain

トラストレスで、分散化された、 そして純真で機能的なオラクルマシーン

2017/2/6

Ver.0.1

- Zackary Hess zack@aeternity.com
- Yanislav Malahov yani@aeternity.com
- Jack Pettersson jack@aeternity.com

## 概要

Ethereumが2014年に始まって以来、分散型でトラストレスなアプリケーション（スマートコントラクト）に大きな関心が集まってます。
その結果、多くの人々がブロックチェーン上に現実の世界のデータを使ったアプリケーションを実装しようとしています。

私たちは、アプリケーションの状態とコードをブロックチェーン上に保存することはいくつかの理由で間違っていると考えてます。
私たちはオラクルシステムを使ってチェックするコンセンサスメカニズムを使用した、非常にスケーラブルなブロックチェーンアーキテクチャを提案します。
この仕組みはオラクルを非常に効率的にします。なぜならそれは一つのコンセンサスメカニズムを積み重ねるレイヤー構造を避けるからです。
ステートチャネルはプライバシーとスケーラビリティを高めるために統合されています。
チャネルにおけるトークンは、純真で機能的なスマートコントラクトを使用し、オラクルの結果にアクセスして、送信することができます。
コントラクトコードを保存したりオンチェーンを使用せずに、私たちは大幅なロスもない、機能性のあるスマートコントラクトを簡単に分析でき処理も高速です。

総合的な資産と予測市場的なアプリケーションは、世界規模で市場をもっと効率的に動かすことができます。

いくつかの分野のProof of
Concept(PoC)はErlangという言語を使い実装しています。開発用ツールとアプリケーションや必需のウォレット、身元確認システムも提供されます。


## 目次

I [はじめに](#はじめに)

I-A [以前](#以前)

II [æternity](#æternity)

II-A [トークン、アカウント、そしてブロック](#トークン、アカウント、そしてブロック)

II-A.1 [Aeonトークンへのアクセス](#Aeonトークンへのアクセス)

II-A.2 [アカウント](#アカウント)

II-A.3 [ネームシステム](#ネームシステム)

II-A.4 [ブロックの内容](#ブロックの内容)

II-B [ステートチャネル](#ステートチャネル)

II-B.1 [スマートコントラクト](#スマートコントラクト)

II-B.2 [例](#例)

II-C [コンセンサスメカニズム](#コンセンサスメカニズム)

II-C.1 [オラクル](#オラクル)

II-D [ガバナンス](#ガバナンス)

II-E [スケーラビリティ](#スケーラビリティ)

II-E.1 [Sharding-trees](#sharding-trees)

II-E.2 [軽量クライアント](#軽量クライアント)

II-E.3 [ステートチャネルと比較](#ステートチャネルと比較)

II-E.4 [Transactions/secとメモリ要件](#Transactions/secとメモリ要件)

III [アプリケーション](#アプリケーション)

III-A [ブロックチェーンに必要なこと](#ブロックチェーンに必要なこと)

III-A.1 [アイデンティティ](#アイデンティティ)

III-A.2 [ウォレット](#ウォレット)

III-A.3 [PoE](#PoE)

III-B [ステートチャネルアプリケーション](#ステートチャネルアプリケーション)

III-B.1 [APIを叩く](#APIを叩く)

III-B.2 [保険付きクラウドファンディング](#保険付きクラウドファンディング)

III-B.3 [クロスチェーンとアトミックスワップ](#クロスチェーンとアトミックスワップ)

III-B.4
[安定した価値の資産と、ポートフォリオの複製](#安定した価値の資産と、ポートフォリオの複製)

III-B.5 [イベントコントラクト](#イベントコントラクト)

III-B.6 [予測市場](#予測市場)

III-B.7
[単一の価格で行われるバッチ取引によるマーケット](#単一の価格で行われるバッチ取引によるマーケット)

IV [実装](#実装)

IV-A [VMとコントラクト言語](#VMとコントラクト言語)

IV-B [ウェブ統合による採用](#ウェブ統合による採用)

IV-C [オープンソースモジュール](#オープンソースモジュール)

IV-D [ユーザビリティとUXデザイン](#ユーザビリティとUXデザイン)

V [ディスカッション](#ディスカッション)

V-A [制限とトレードオフ](#制限とトレードオフ)

V-A.1 [オンチェーンステート](#オンチェーンステート)

V-A.2 [無料化の問題](#無料化の問題)

V-A.3
[流動性の低下とステートチャネルトポロジー](#流動性の低下とステートチャネルトポロジー)

V-B [今後の活動](#今後の活動)

V-B.1 [機能的なコントラクト言語](#機能的なコントラクト言語)

V-B.2 [マルチパーティチャネル](#マルチパーティチャネル)

# I はじめに

この論文の目的はæternityのブロックチェーンアーキテクチャとその上に構築可能なアプリケーションの概要を示すことです。より詳細な論文は将来リリースされる予定であり、特にコンセンサスとガバナンスのメカニズムを示すためのものである。
しかし、我々の構造は全体論的であることに留意する必要がある。すべてのコンポーネントが連携して、モジュール方式を使用し、相乗効果を発揮します。
この論文は4つのパートで構成されています。
一つ目に、我々は私たちのアーキテクチャに関して、基本的かつ論理的なアイデアを紹介し論じます。
二つ目に、私たちは、あらかじめ含まれている必需のアプリケーションについて論じ、他のユースケースや、開発者がどのようにこのプラットフォームを使うのかに関する例をあげます。
三つ目にErlangで書かれたProof of
Conceptの実装を提示します。私たちは将来の方向性と他の技術の可能性に関する議論で話を締めくくります。

# I-A 以前

Bitcoinから始まったブロックチェーンは、新しいインターネット上での価値交換の方法を示しています。[1]
またそれに続いて多くの有望な進歩が続きました。Ethereumはブロックチェーンアーキテクチャ上で安全に動くチューリング完全なスマートコントラクトを書く方法を示しました。Truthcoinは
オラクルをブロックチェーン上に作るためのツールを発明しました。[3]
GnosisとAugurはどのようにしてより効率的にオラクルを作るのかを示しました[4]。Casey
Detrioはブロックチェーン上にマーケットを作る方法を示しました[5]。Namecoinは同様に分散化されるDNS（ドメインネームサーバー）の作り方を示しました[6]。Factomはハッシュを記録することができるブロックチェーンを、あらゆるデジタルデータの存在証明（Proof
of existence）にどのようにして使えるかを示しました[7]。

これらの技術は誰にでもファーストクラスの金融サービス、正当で適法のサービスを提供します。しかしこれまでのところ、完全に約束を果たすことはできませんでした。
具体的に言えば、これまでの解決方法はガバナンス、スケーラビリティ、スクリプトの安全性の確保、実世界のデータへの安価なアクセスに欠けていました。æternityはこれらすべての問題点について、解決することが目標であり目的です。

# II æternity

我々はスケーラビリティ、スクリプトの安全性、実世界のデータへの安価なアクセスの欠如は「スマートコントラクトプラットフォーム」における3つの重要な問題点となります。
