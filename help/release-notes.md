---
title: '[!DNL Adobe Marketo Qualifier] リリースノート'
description: '[!DNL Adobe Marketo Qualifier]の新機能について説明します。'
feature: Agentic AI, Sales Insights, Account Journeys
role: User
source-git-commit: 042ebc0019d33019940ff8ad98c0635cb97235f0
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 14%
---
# [!DNL Adobe Marketo Qualifier] リリースノート

## 09-22-2026

このリリースには次のものが含まれます。

* 組み込みのCRM プラグインで[!DNL Marketo Sales Insights]とエージェント型データを表示し、見込み客を[!DNL Marketo Qualifier]に追加します。 [詳細情報](admin-settings.md#crm-mcp-and-the-embedded-plugin)。
* ベストベット、マイウォッチリスト、web アクティビティ、メールエンゲージメント、ウェビナーアクティビティにより、CRM リードに優先順位を付けることができます。 [詳細情報](admin-settings.md#prioritize-leads-in-the-crm-plugin)。
* ライブ [!DNL Marketo]のアクティビティがワークフロー条件に一致すると、見込み顧客がアウトバウンドワークフローに自動的に登録されます。 [詳細情報](home.md#automatically-enroll-prospects-from-marketing-highlights)。
* 見込み客のコンテキストを確認し、見込み客リストを書き出して、[!DNL Marketo Optimizer]件のPrimeおよびUltimate インスタンスでAI担当者の概要を表示します。 [詳細情報](prospects.md#review-prospect-context-and-export-the-list)。
* 生成された見込み客のメールをタスクキューから確認して承認し、アウトバウンドワークフロー中にエージェントの提案を返します。 [詳細情報](tasks.md)。

## 09-08-2026

このリリースには次のものが含まれます。

* プロファイル設定で独自のメール作成スタイルを一度設定すれば、生成されるあらゆるメールがそのスタイルに従います。 [詳細情報](profile-settings.md#email-drafting-context)。
* 新しい「ミーティング調査」タブで、見込み客のページから目標ベースまたはカスタムのミーティング準備を生成します。 [詳細情報](prospects.md#generate-meeting-prep)。
* 管理者は、アウトバウンドワークフローをチームメイトに割り当て、ワークフロー設定をデフォルトにリセットできます。 [詳細情報](outbound-workflows.md#create-an-outbound-workflow)。
* CSVから見込み客をインポートする際にカスタムフィールドをマッピングし、生成されたメールでそれらの値を使用します。 [詳細情報](prospects.md#build-your-prospect-list)。
* 生成されたメールは、インポートした追加の見込み客データを使用し、見込み客の言語でネイティブに作成できます。 [詳細情報](outbound-workflows.md#step-5-add-prospects-and-start-email-generation)。
* アウトバウンドパフォーマンスでは、デフォルトで開封率とクリック率が表示され、未加工の数と組織レベルでの見込客数の切り替えが表示されます。 [詳細情報](performance.md)。
* CRM同期ルールは、見込み客がアウトバウンドワークフローを通過すると、CRM ステータスを自動的に更新します。 [詳細情報](admin-settings.md#configure-crm-sync-rules)。
* [!DNL Marketo Qualifier]、CRM、[!DNL Marketo]、[!DNL Marketo Optimizer]のデータでAI チャットの質問を行います。 [詳細情報](ai-assistant.md#ask-ai-chat-across-your-connected-data)。

## 08-17-2026

[!DNL Marketo Qualifier]はスタンドアロンアプリとして利用できるようになりました。 [!DNL Marketo Engage]と[!DNL Marketo Optimizer]をサポートしています。

このリリースには次のものが含まれます。

* AIが生成したアクティビティの概要とシグナルベースのスコアリングによる、見込み顧客とアカウントの優先順位付け。 [見込み顧客に関する詳細](prospects.md#review-prospect-details)または[&#x200B; アカウント &#x200B;](accounts.md#account-insights)を確認します。
* AIが提案したケイデンスとドラフト付きメールによる、目標主導のアウトバウンドワークフロー。 [詳細情報](outbound-workflows.md)。
* 電話、LinkedInMails、メールレビュー用の統合タスクキュー。 [詳細情報](tasks.md)。
* カレンダー統合によるミーティングの自動予約。 [詳細情報](outbound-workflows.md#meeting-booking)。
* 自社のプレイブック資料でAIのアウトリーチを支援するためのナレッジセンター。 [詳細情報](admin-settings.md#knowledge-center)。
* CRM、エンゲージメント、ナレッジセンターのデータにもとづいて、自然言語での質問に対応するAI チャット。 [詳細情報](ai-assistant.md)。
* 電子メールおよびミーティング予約のパフォーマンスレポート： [詳細情報](performance.md)。
* CRMまたはOutlook内でアクセスするためのブラウザーと電子メールのプラグイン。 [詳細情報](admin-settings.md#crm-mcp-and-the-embedded-plugin)。
* SalesforceとMicrosoft Dynamics 365の統合のサポート。 [詳細情報](integrations.md)。
