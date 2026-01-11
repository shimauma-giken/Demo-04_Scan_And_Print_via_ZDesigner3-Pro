#### Demo-04_Scan_And_Print_via_ZDesigner3-Pro
# Zebra Designer 3 Proを用いたスキャン＆プリントデモ

オートIDの仕事していると、スキャンデータを基に印刷をするというシーンをよく見かけます。しかしながら、まだまだ浸透していません。導入が高価のためソリューションを導入できないや、導入企画・検討できるITエンジニアがいないため導入に躊躇している、などという現場のお声を多く聞きます。ゼブラ社のソリューションを活用することで、汎用的なプロセスであれば、以外とシンプル・安価に構築できます。

本頁では汎用的なスキャン＋印刷プロセスをしたいユーザの参考になるように、基礎的なデモ手順をご紹介します。


### デモの想定シーン

製造業などで個品に様々な情報が格納されたQRが添付されていることがあります。各プロセスにおいて、QRから必要な情報を抽出し、専用ラベルを印刷するタスクがあります。本頁では上記運用をイメージしたデモ環境を構築し、実際に体験する手順を提供します。

</br>


</br>

## 0. 本手順で必要なマテリアル
</br>

#### 構成イメージ
   <img width="500" src="./connected.png"> 


1. Zebra Link-OS プリンタ</br>

1. Zebra DSスキャナ (本頁ではUSBを前提に説明)</br>

1. 印刷用のラベル・リボン
   添付のサンプルは、2x1 inchラベル向けに作成されています。</br>

2. Window 11 以上のPC 
   - 要: Zebra Designer v10 ドライバ
   - 要: Zebra Designer 3 Professional
   - 要: Zebra 123Scan
  
3. PC <--> プリンタ接続用のUSBケーブル
</br>


## 1. 123Scan操作：スキャナの設定
</br>

1. （**重要**）スキャナの初期化

   <img src="./factory-reset.png">

</br>

1. DSスキャナで下記の設定バーコードを読み取り。
   
   <img src="./barcode-config-00ms.png">

    #### ワンポイント解説

    123Scanを用いて、マニュアルで設定をする場合は下記設定内容か、添付の[123Scan設定ファイル](./Barcode-DS9308_delay-00ms.scncfg)を参考に設定をすること。</br>
   <img src="./config-01.png">
</br>

## 2. 個品ラベルの印刷

1. 本頁に添付されている下記ファイルをダウンロードする。
    - [input_QR.nlbl](./input_QR.nlbl)
    - [input_QR.xlsx](./input_QR.xlsx) 
    </br>

2. 本ページに添付されている**input_QR.nlbl**をZDesigner 3 Proで起動する。</br>
   ![alt text](image-6.png) 
   </br>

2. **ファイル** → **印刷**を選択し、印刷画面に遷移する。
   ![alt text](image-7.png) 
   </br>

3. 印刷先プリンタの設定をする。
    ![alt text](image-5.png) 
    </br>

1. 印刷ボタンを押下し、印刷する。
    * サンプルではラベルが3枚印刷される。</br>

</br></br>

## 3. デモ印刷
</br>

1. PCにプリンタとスキャナを接続する。</br>
   <img width="500" src="./connected.png"> 
   </br>

2. 本ページに添付されている下記ファイルをZDesigner 3 Proで起動する。</br>
   [サンプルプログラム：output_QR.nlbl](./output_QR.nlbl)
   </br>

3. **ファイル** → **印刷**を選択し、印刷画面に遷移する。
   ![alt text](image-1.png)</br>

1. 印刷先プリンタの設定をする。
    ![alt text](image-5.png) 
    </br>

2. **変数キーボード** > **バーコード**が選択された状態にする。
   ![alt text](image-4.png) </br>

    **※（重要）この時、Windows PCの入力が半角英数になっていることを確認すること！！全角入力となっている場合は、半角英数に変更すること。**
    </br>

    ![alt text](image-3.png)

    </br>

3. 個品ラベルのQRコードを（連続）スキャンし、QRに応じたパーツラベルが印刷されることを確認する。
    ![alt text](image-8.png)
</br>

-- End: Enjoy Zebra!
