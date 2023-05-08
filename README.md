# nurse-robo（編集中）

https://user-images.githubusercontent.com/127037666/236716336-17b5f97c-dcf0-4fd7-ab14-5dcb66938d62.mp4

## ダウンロード方法
<!-- 
![Fs60KHuaAAE7mtP](https://user-images.githubusercontent.com/127037666/236717163-23b2fd4c-0ac2-47d8-be41-55f2be2d7bc5.png)
-->

1. このページの一番上にある緑色の「<>Code」ボタンをクリックし、Download ZIPをクリックしてダウンロードしてください。

<!-- 
![Fs61B9GaMAMr73E](https://user-images.githubusercontent.com/127037666/236717220-2fcdcfa8-d95c-4248-aba1-72704dc5827e.png)
-->

2. ダウンロードしたZipフォルダを展開してください。

3. ![nurse-robo-v.1.1.0](nurse-robo-v1.1.0/nurse-robo-v1.1.0.exe)をクリックし、ページの右の方にあるDownloadボタンをクリックしてください。
<!--
<img src="https://user-images.githubusercontent.com/127037666/236718356-e58cba07-6744-4905-bf3d-66036992cd4e.jpg" width="75%" style="border: 10px solid #hhh;">
![Fs654HkaIAE3sna](https://user-images.githubusercontent.com/127037666/236718356-e58cba07-6744-4905-bf3d-66036992cd4e.jpg)
<img src="画像のURL" alt="画像の説明" style="border: 1px solid #ccc;">
![Fs654HkaIAE3sna](https://user-images.githubusercontent.com/127037666/236718356-e58cba07-6744-4905-bf3d-66036992cd4e.jpg)
-->

4. 展開したフォルダのnurse-robo-v1.1.0.exeに上書き保存してください。
<!-- 
<img src="https://user-images.githubusercontent.com/127037666/236718257-b310d404-3e63-4fc4-bb52-2620e1f59674.png" width="75%" style="border: 10px solid #hhh;">
-->

## セッティング方法

1. <a href="https://voicevox.hiroshiba.jp" target="_blank" rel="noopener noreferrer">新規タブで開く</a>

[VOICEVOX](https://voicevox.hiroshiba.jp){:target="_blank"}をダウンロード・起動。GPUがある方は「GPUモードに切り替える」まで、そうでない方は「初回起動時の確認」まで、
この[サイト](https://sosakubiyori.com/voicevox-introduction/)に沿って設定して下さい。

2. OpenAIのAPIキーを用意してください。まだ持ってない方はこの[サイト](https://laboratory.kazuuu.net/how-to-get-an-openai-api-key/)を参考に取得できます。

3. nurse-robo-v1.1.0.exeをダブルクリック。警告が出ますが実行して、数十秒待つとアプリが立ち上がります。

（初回だけ起動に時間がかかります）

4. 右下の入力BOXにAPIキーをコピペしてEnterを押すとキーが有効か否かを認証します。
<!--
<img src="https://user-images.githubusercontent.com/127037666/236718488-7b00bb12-765b-41af-b72e-aaa4cb103a07.jpg" width="75%" style="border: 10px solid #hhh;">
-->

5. 認証が完了すると会話できるようになります。

## 音声入力方法

<img src="https://user-images.githubusercontent.com/127037666/236718700-0ad4d45c-c28d-4ff5-8405-aa491a2f4b0b.jpg" width="75%" style="border: 10px solid #hhh;">

会話の方法は右下の入力ボックスにテキストを書いてEnterキーを押すか、空欄のままEnterキーを押して声で話しかけるかです。
別のウィンドウで「話してください...」と表示されている間は聞いています。話し始めてから１秒以上の沈黙があると聞くのをやめて応答を考えます。
応答が考え終わると口パクしながら返答を話し始めます。

<img src="https://user-images.githubusercontent.com/127037666/236718746-ed861d8b-2453-4aec-82d1-eb09f20167ae.jpg" width="75%" style="border: 10px solid #hhh;">
<!-- 
![Fs7Id9yaMAYn4TB](https://user-images.githubusercontent.com/127037666/236718746-ed861d8b-2453-4aec-82d1-eb09f20167ae.jpg)
-->

## 設定方法
### 設定モード起動
```/setting```

> 設定モードを開始します。その状態で以下のコマンドを入力すると各種設定を変更できます。

### 人格設定変更
```change_persona:女の子として、好きな相手に対する返答をため口で２０文字でしてください。```

> キャラクターの人格設定や２０文字以内等の字数制限、口調の指定ができます。上記の書式でコマンドと設定文を一回で入力するように、メモからコピペするなどしてください。

### 履歴参照開始
```log_on```

> 返答する際に会話履歴を取り始め、参照するようにします。この場合、１ラリーの対話で人格設定文とその回の入力文と返答文に加えて、履歴を取り始めてからの入力文と返答文の文字数分トークンを消費します。つまり、このモードを開始するとより自然な会話ができますが、消費するトークン数が対話するごとに増加するので注意してください。

### 履歴参照終了
```log_off```

> 返答する際に会話履歴を参照せずに、人格設定のみに基づいて入力文に返答します。この場合、１ラリーの対話で人格設定文と入力文、返答文の文字数分トークンを消費します。

> デフォルトのモードは会話履歴を取らないモード（log_off）で、モードを切り替えるたびに会話履歴はリセットされます。

### 声変更
```speaker_id:10```

> キャラクターの声を指定した番号に変更します。指定できる声の一覧はリプライかgithubのREADMEに書いてます。最新の声の一覧はVOICEVOXのアプリを起動した状態でhttp://localhost:50021/speakersにアクセスすると確認できます。

## ルール
- このアプリを利用た上で「発信する」場合、利用規約 krnr.top/rulesを遵守してください。
- ソースコードを利用・編集・再配布する際に、私への連絡・クレジット表記は不要です。
- 入力ボックスにEscキーを入力してもアプリを終了できます。
