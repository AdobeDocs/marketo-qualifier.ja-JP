---
title: CRM プラグインの設定
description: SalesforceまたはMicrosoft Dynamics 365にMarketo Qualifier CRM プラグインをインストールする方法について説明します。 ワークフローとMarketo キャンペーンに対するSalesforce アクションを設定します。
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: da701e37-3227-4187-b68a-914277252a79
    internal-label: Integrations
  - id: f8f8b877-7295-5853-989f-e21f73bc94c4
    internal-label: Administration
subfeature_v2:
  - id: d2fe5f36-5653-5902-937c-9d3026104284
    internal-label: CRM integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: df256cf271296b82fab2ed10725a0d6bd165e05b
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%
---

# CRM プラグインの設定

[!DNL Adobe Marketo Qualifier] CRM プラグインをインストールして、担当者が[!DNL Marketo Sales Insights]とAIによって生成されたインサイトをSalesforceやMicrosoft Dynamics 365から離れることなく、リード、取引先責任者、アカウントのレコードページで使用できるようにします。 このプラグインは、CRMでリードを[優先順位付けするためのホームビューも提供します](admin-settings.md#prioritize-leads-in-the-crm-plugin)。

Salesforceでは、リードや連絡先のリストビューや個々のレコードページから、アウトバウンドワークフローやMarketoキャンペーンに見込み客を追加することもできます。

## 始める前に

プラグインをインストールして使用するユーザーが必要なアクセス権を持っていることを確認します。

* **Salesforce管理者**: パッケージのインストールとページレイアウトの編集を行う権限。
* **Microsoft Dynamics 365 administrator**: Power Appsでソリューションをターゲット環境にインポートする権限。
* **代表者**: Marketo Qualifierおよび関連するCRM レコードへのアクセス。

プラグインのインストールは、[CRMをMarketo Qualifierに接続することとは別です](getting-started.md#connect-your-crm)。

## Salesforceへのインストール

パッケージをインストールしてから、担当者が使用するレコードページにそのコンポーネントを追加します。

1. [Salesforce インストールページ ](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce)を開き、Salesforceに管理者としてログインします。
1. パッケージのインストールページで、「**[!UICONTROL すべてのユーザーにインストール]**」を選択し、「**[!UICONTROL インストール]**」を選択します。

   Salesforce権限を使用して、個々のユーザーのアクセスを引き続き制御できます。

1. サードパーティアクセスの承認を求めるメッセージが表示されたら、「承認」チェックボックスを選択し、**[!UICONTROL 続行]**&#x200B;を選択します。
1. インストールが完了したら、**[!UICONTROL 完了]**&#x200B;を選択します。

   インストールには数分かかります。 パッケージが&#x200B;**[!UICONTROL インストール済みパッケージ]** ページに表示されていることを確認します。

1. Lightning App Builderで、リード、取引先責任者、アカウントのレコードページを編集し、Marketo Qualifier コンポーネントを追加します。

### リストビューへのアクションの追加

リードと連絡先のリスト表示については、**[!UICONTROL アウトバウンドワークフローに追加]**&#x200B;と&#x200B;**[!UICONTROL Marketo Campaignに追加]**&#x200B;を個別に設定します。 パッケージに含まれているボタンを使用して、重複を避けます。

1. **[!UICONTROL Setup]** > **[!UICONTROL Object Manager]**&#x200B;に移動し、**[!UICONTROL Lead]**&#x200B;または&#x200B;**[!UICONTROL Contact]**&#x200B;を選択します。
1. **[!UICONTROL ボタン、リンク、およびアクション]**&#x200B;を開き、リストボタン **[!UICONTROL AMQ Add to Outbound Workflow]**&#x200B;および&#x200B;**[!UICONTROL AMQ Add to Marketo Campaign]**&#x200B;を見つけます。
1. オブジェクトの&#x200B;**[!UICONTROL リスト表示ボタン レイアウト]**&#x200B;を開き、**[!UICONTROL 編集]**&#x200B;を選択します。

   Salesforceの設定によっては、リストビューレイアウトが&#x200B;**[!UICONTROL 検索レイアウト]**/**[!UICONTROL リストビュー]**&#x200B;の下にある場合があります。

1. 両方のリストボタンを&#x200B;**[!UICONTROL 選択したボタン]**&#x200B;に移動して保存します。
1. 他のオブジェクトに対してこれを繰り返します。

担当者は、リストビューで1つ以上のレコードを選択してから、アクションを選択します。

### レコードページへのアクションの追加

レコードページのアクションは、リストビューボタンとは別に設定する必要があります。 使用中のリードと連絡先のページレイアウトごとに両方のアクションを追加します。

1. **[!UICONTROL Setup]** > **[!UICONTROL Object Manager]**&#x200B;に移動し、**[!UICONTROL Lead]**&#x200B;または&#x200B;**[!UICONTROL Contact]**&#x200B;を選択します。
1. **[!UICONTROL ボタン、リンク、アクション]**&#x200B;を開き、詳細ボタン **[!UICONTROL AMQ Add to Outbound Workflow]**&#x200B;および&#x200B;**[!UICONTROL AMQ Add to Marketo Campaign]**&#x200B;を見つけます。
1. **[!UICONTROL ページレイアウト]**&#x200B;を開き、担当者に割り当てられたレイアウトを編集します。
1. **[!UICONTROL Salesforce MobileとLightning Experience Actions]**&#x200B;の両方の詳細ボタンを追加して保存します。
1. 該当する各レイアウトと他のオブジェクトに対してこれを繰り返します。

アクションは、レコードのアクションバーまたはそのメニューに表示され、表示中のレコードに適用されます。

>[!NOTE]
>
>これらのアクションは、Salesforce モバイルアプリではなく、デスクトップ Salesforce Lightning Experienceで機能します。 **[!UICONTROL Salesforce Mobile and Lightning Experience Actions]**&#x200B;という名前のレイアウトセクションは、デスクトップアクションにも使用されます。

### 見つからないボタンを置き換える

パッケージ化されたボタンが見つからない場合は、オブジェクトの&#x200B;**[!UICONTROL ボタン、リンク、アクション]**&#x200B;の下に置き換えを作成します。

1. **[!UICONTROL 新規ボタンまたはリンク]**&#x200B;を選択します。
1. アクションのラベル（`Add to Outbound Workflow`や`Add to Marketo Campaign`など）を入力します。
1. リスト表示には&#x200B;**[!UICONTROL リストボタン]**、レコードページには&#x200B;**[!UICONTROL 詳細ページボタン]**&#x200B;を選択します。
1. **[!UICONTROL Content Source]**&#x200B;を&#x200B;**[!UICONTROL Visualforce Page]**&#x200B;に設定し、アクション、オブジェクト、配置に一致するパッケージのアクションページを選択します。

   リードリスト、リード詳細、コンタクトリスト、コンタクト詳細の配置では、異なるページを使用します。 選択したページが、設定しているプレースメントと一致することを確認します。

1. リストボタンの場合は、**[!UICONTROL 行選択を要求]**&#x200B;を選択します。
1. ボタンを保存し、上記のように、適切なリスト表示ボタンのレイアウトまたはレコードページのアクションに追加します。

### Salesforceのアクションの確認

レイアウトを保存した後、両方のアクションがリードビューと連絡先リストビューおよびレコードページに表示されることを確認します。 選択したレコードと、個々のレコードの各レコードページのアクションを使用して、各リストアクションをテストします。

アクションが使用できない場合や開かない場合は、次のチェックを使用します。

| 問題 | 確認すべきこと |
| --- | --- |
| リスト表示にボタンが表示されない | リスト ボタンが正しいオブジェクトの&#x200B;**[!UICONTROL リスト表示ボタン レイアウト]**&#x200B;の&#x200B;**[!UICONTROL 選択ボタン]**&#x200B;にあることを確認し、レイアウトを保存します。 |
| レコードページにボタンがありません | 詳細ボタンが、ユーザーに割り当てられたレイアウトの&#x200B;**[!UICONTROL Salesforce Mobile and Lightning Experience Actions]**&#x200B;にあることを確認します。 組織で動的アクションを使用している場合は、レコードページのアクションの表示も確認します。 |
| ボタンの作成時に想定されるページオプションが使用できない | 表示タイプがリスト表示の場合は&#x200B;**[!UICONTROL リストボタン]**、レコードページの場合は&#x200B;**[!UICONTROL 詳細ページボタン]**&#x200B;であることを確認してください。 |
| アクションが開かない、またはアクセスエラーが表示される | ユーザーがMarketo Qualifierおよび選択したレコードにアクセスできることを確認します。 |

## Microsoft Dynamics 365へのインストール

プラグインパッケージを、担当者が作業する環境に読み込みます。

1. [Microsoft Dynamics 365 インストールページ ](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics)を開き、パッケージ ZIP ファイルをダウンロードします。
1. 管理者として[Power Apps](https://make.powerapps.com/)にログインし、ターゲット環境を選択します。
1. **[!UICONTROL ソリューション]**&#x200B;を開き、**[!UICONTROL ソリューションの読み込み]**&#x200B;を選択します。
1. **[!UICONTROL 参照]**&#x200B;を選択し、ダウンロードしたZIP ファイルを選択して、**[!UICONTROL 次へ]**&#x200B;を選択します。
1. パッケージの詳細を確認し、**[!UICONTROL 次へ]**&#x200B;を選択します。
1. 事前入力された環境変数の値を保持し、**[!UICONTROL 読み込み]**&#x200B;を選択します。
1. ソリューションが正常に読み込まれたという確認メッセージがページの上部に表示されるまで待ちます。

読み込みには数分かかります。

>[!MORELIKETHIS]
>
>* [CRM プラグインでリードに優先順位を付ける](admin-settings.md#prioritize-leads-in-the-crm-plugin)
>* [統合](integrations.md)
>* [基本を学ぶ](getting-started.md)
