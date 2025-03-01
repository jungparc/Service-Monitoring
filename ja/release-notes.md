## Management > Service Monitoring > リリースノート

### 2021. 12. 28.

#### バグ修正
* シナリオ名が31文字を超える場合、2つ以上のシナリオのヒストリーExcelをダウンロードできない問題を修正

### 2021. 07. 27.

#### 機能改善
* 新規ローディングバーの適用
* セキュリティ改善事項の適用

### 2021. 04. 27.

#### バグ修正
* 特定のユーザーが含まれるプロジェクトで、配信対象者が照会できない問題を修正

### 2021. 03. 23.

#### バグ修正
* 障害通知ページ検索条件に基づいて照会できない問題を修正
* 障害通知ページでリストを選択した時、満了案内が表示される問題を修正
* Webフックを編集した時、既存のHTTPヘッダが継続して表示される問題を修正
* ヒストリー検索を行った時、開始時間が含まれていない問題を修正

### 2020. 12. 29.

#### バグ修正
* シナリオ管理オープンAPIのメソッド(POST、GET、PUT、DELETE)で、API呼び出しのresultCodeとresultMessageの表示が異なる問題を修正
* CloudTrailイベントが常にUSER_CONSOLEとして適用される問題を修正
* CloudTrail PM変更イベントがPM登録イベントとして登録される問題を修正

### 2020. 11. 24.

#### 機能追加
* シナリオを管理するための[修正](/Management/Service%20Monitoring/ja/api-guide/#_15)オープンApi機能を追加
* Webフックリクエストパラメータをサポート
* **LINE**のメッセージ送信Webフックテンプレートを追加

### 2020. 10. 27.

#### バグ修正
* openAPIを活用してシナリオを作成する際、requestBodyのurlフィールドにハイフン(-)が含まれている場合に、シナリオが作成できない問題を修正
* バッチモニタリングシナリオを作成する時、検証情報を入力しなくても作成できた問題を修正
* Webフック情報を修正する時、リクエストデータの編集項目の内容が正常に表示されない問題を修正

### 2020. 09. 22.

#### 機能追加
* シナリオ管理用の[作成](/Management/Service%20Monitoring/ja/api-guide/#_8)、[照会](/Management/Service%20Monitoring/ja/api-guide/#_11)、[削除](/Management/Service%20Monitoring/ja/api-guide/#_13) Open API機能を追加

### 2020. 08. 25.

#### バグ修正
* バッチモニタリングシナリオを登録した後、すぐにAPIを呼び出した時、呼び出し結果が正常に反映されない問題を修正

### 2020. 07. 28.

#### 機能改善
* Webモニタリングの動作最小単位を変更
  * APIモニタリング：60秒 ---> 30秒
  * 仮想ブラウザ、モジュールモニタリング：120秒 ---> 60秒

#### バグ修正
* バッチモニタリング内容検証時、大文字/小文字を区別しない問題を修正

### 2020. 05. 26.

#### 機能改善
* Webモニタリングテストが30秒以上かかる場合、失敗する問題を修正
* Webモニタリングテキスト検証時、シナリオタイプ、レスポンスコンテンツタイプに応じて使用できる演算子を追加
  * API
    * レスポンスが_HTML_、_XML_の場合、contain、!containのみ使用可能
    * レスポンスが_JSON_の場合、_JsonPath_を活用して(==, !=, >, >=, <, <=)使用可能
  * Browser, Module
    * レスポンスが_HTML_、_XML_の場合、contain、!contain、_xPath_を活用して(==, !=, >, >=, <, <=)使用可能
    * レスポンスが_JSON_の場合、_JsonPath_を活用して(==, !=, >, >=, <, <=)使用可能
* TOAST CloudTrailサービス連携
  * Service Monitoringコンソールで発生したユーザーイベントをTOAST CloudTrailで確認可能
  
### 2020. 01. 21.

#### 機能改善
* Web/TCPモニタリングUSリージョンをサポート
* モニタリングヒストリー検索時、モニタリングリージョンオプションを追加

### 2019. 12. 24.

#### 機能改善
* 障害の配信に失敗した時、ヒストリー詳細履歴メッセージを改善
* Webページ性能が向上

#### バグ修正
* サービス配信担当者ではないユーザーに配信状況ページで配信履歴が表示されない問題を修正

### 2019. 11. 26.

#### 機能改善
* 配信状況ページで、配信状態情報を分離表示。
* ユーザー言語が英語の場合、一部のUIが崩れる現象を修正。
* Webモニタリングシナリオ編集機能を改善
  * テキスト検証時、演算子に応じてplaceholderが表示されるように改善。
  * [シナリオ検証タイプ]によってテキスト検証演算子表示を制限。
  * [シナリオ検証タイプ]がモジュールの場合にも**スクリプトエラー無視**、**イメージダウンロード除外**、**CSS有効化**オプションを使用できるように改善。

#### バグ修正
* [障害配信キャンセル案内]メールの送信時、各メール内のキャンセルしたユーザー名ではなく受信者名が伝達される問題を修正。


### 2019. 08. 27.

#### 機能改善
* 日本語のフォントをTOAST共通のフォントに変更しました。
* TCPモニタリングシナリオ編集画面で、IP、PORT入力ラベルを分離して可読性を向上させました。

#### バグの修正
* 配信詳細表示画面で、時間が正常に表示されない問題を修正しました。
* モニタリング障害登録の際、配信タイトルがシナリオ保存時に設定された言語で登録されるように修正しました。
* 障害配信メッセージ内の障害通知ページ接続時に、有効期限切れではないのにかかわらず、有効期限切れと表示される現象を修正しました。
* 日本語の障害配信メッセージのタイトルが誤って追加される問題を修正しました。

### 2019. 07. 23.


#### 新規サービスリリース
Service Monitoringは、安定的にサービスを運営するためのサービス障害管理プラットフォームです。 
	* サービスごとに配信担当者、配信チャンネルを管理
	* 多様なモニタリング方式をサポート。Webモニタリング、TCPモニタリング、バッチモニタリング 
