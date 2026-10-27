---
title: プロファイル設定を指定
description: Adobe Marketo Qualifier プロファイル設定でメール接続、署名、カレンダーの利用可能設定を行う方法について説明します。
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/YsrBduYA7jKhgxttexqMBBpgDIq23s6wUb4Wp6y6h3g'
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: f8c781b4-253f-436e-b9f1-a71172814e41
    internal-label: Profile Settings
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: beb7a3c1-66ab-4786-b879-7621375b3c40
    internal-label: Email marketing
source-git-commit: ab54d20ccc80d88c3592d89c9f43feeb062ed82c
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 3%
---

# プロファイル設定

左側のナビゲーションで、**[!UICONTROL 設定]**&#x200B;を展開し、**[!UICONTROL プロファイル設定]**&#x200B;を選択します。 これらの設定を使用して、個人情報、メール接続、カレンダー、チャットの空き状況を管理します。

![ プロファイル設定](assets/profile-email-config.png)

## メールの設定

「**[!UICONTROL メール設定]**」タブで、メール接続を設定します。

* **[!UICONTROL メール接続]** — Microsoft OutlookまたはGoogleを選択し、サインインプロセスに従います。 必要に応じて、承認するアクセスと管理者の承認パスについては、[Connect Outlook](integrations.md#connect-outlook)を参照してください。
* **[!UICONTROL 電子メール署名]** – 生成された電子メールで使用される署名を追加または更新します。 見込み客が時間を予約できるように、[ ミーティング予約](outbound-workflows.md#meeting-booking)のリンクを含めます。
* **[!UICONTROL ミーティング予約リンク]** - メール内でミーティング招待状を送信します。 ミーティングのURLを取得します。

### メール作成コンテキスト

![ メールのコンテキスト ](assets/profile-email-instructions.png)

電子メールのトーン、構造、スタイルを設定するには、**[!UICONTROL 電子メール作成コンテキスト]**&#x200B;を使用して、電子メールの一貫性を保ちます。

コンテキストは、**[!UICONTROL メール作成コンテキスト]**領域のプレーンマークダウンに書きます。
これを使用して、次の項目を定義します。

* トーンとボイス
* 構造と長さ
* Personalizationと挨拶のルール
* 件名のスタイル
* エンゲージメントシグナルの使用方法
* 指標、プルーフポイント、カスタマーストーリーのフレーム化

デフォルトでは、ドラフトはハウススタイルのコンテキストを使用するため、既存のドラフトは独自のコンテキストを追加するまで変更されません。

## カレンダー設定

「**[!UICONTROL カレンダー設定]**」タブで、タイムゾーンと可用性を設定します。

* **[!UICONTROL カレンダー接続]**- **[!UICONTROL 接続]**&#x200B;を選択し、Microsoftのサインインプロセスに従います。
* **[!UICONTROL ミーティング確認メール]** – 見込客がミーティングを予約した後に受信する確認メールの件名と本文を定義します。
* **[!UICONTROL 環境設定]** - デフォルトのミーティングの長さとミーティング間のバッファーを設定します。

カレンダーの接続を解除した場合：

* アクティブな予約リンクが機能しなくなります。
* 予約ページに、一時的な利用不可メッセージが表示されます。
* 設定は、再接続したときに保持されます。

## カレンダーの可用性

Adobe Marketo Qualifierのカレンダーの空き状況は、次の2つの入力に基づいています。

* OutlookやGmailなどの接続された作業カレンダー
* **[!UICONTROL カレンダー設定]**&#x200B;の可用性とタイムスロットのルール

Marketo Qualifierは、接続されたカレンダーから、イベントの詳細ではなく、空き時間情報ステータスを読み取ります。 このステータスとルールを組み合わせることで、見込み客が予約できる時間枠を決定します。

次の項目を設定できます。

* 曜日ごとの作業時間
* 1日に複数のブロック（例：午前9:00 – 正午、午後1:00-5:00）
* 自分のタイムゾーン
* ミーティング期間
* ミーティングの前後のバッファー
* 最低限知らせ
* 予約ウィンドウ

>[!MORELIKETHIS]
>
>* [ アウトバウンドワークフロー](outbound-workflows.md)
>* [統合](integrations.md)
>* [タスク](tasks.md)
