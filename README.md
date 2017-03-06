# SimpleMyToDoApp
・version 1.0

##概要
PHPの練習用に書きました。自分用に作ったTODOリストです。タスクの〆切やメモについての簡単な確認ができます。新規登録時に設定する優先度や、〆切が近くなると現れる警告などを表示させることでやるべき順番なども考えやすいように組みました。
![一覧](http://imgur.com/a/CfEXA "一覧画像")

##機能
一覧・編集・週表・タスク追加を1画面で一括確認・操作できます。
* 一覧 : 通常は登録順に並べられていますが、「▲」「▼」で優先度順、〆切順に昇順降順にソートできます。警告では、優先度「高」で2日以内のタスクと優先度「中」または「低」で1日以内のタスクには旗と残り時間を表示します。〆切を過ぎたものにはボムを表示します。
* 編集 : [+開く]を押すと入力フォームがでるので変更後、更新を押すと編集できます。エラーメッセージ、成功のメッセ―ジがでるのでそれに従って操作します。
* 週表(今日から一週間の予定) : 本日から一週間以内のタスクを簡易的に確認できます。
* 追加(新規タスク追加) : タスク名・優先度・〆切・メモ(任意)を入力し送信を押すと追加できます。編集同様エラーメッセージ、成功のメッセ―ジがでるのでそれに従って操作します。

(HTML5のdatetime-localの関係でブラウザによって機能しない場合があります。機能しなかった場合の対策もしていますが、開発した環境でもあるのでChromeを使うことを推奨します。)

##開発環境
* XAMPP v3.2.2
* MySQL
* Google Chrome バージョン 56.0.2924.87

##ファイル構成
一画面で操作できるようになっていますがphpは部品ごとに分けて作成しています。
* all.php : 一覧・週表
* update.php : 編集
* add.php : 追加  
* index.css : アプリ全般のレイアウト
* index.js : 一覧の時計、編集のボタンの制御  
アイコンはfont-awesome-4.7.0を使用しています。

##DB
データベース名:DB_NAME  
テーブル名:todo  
ユーザー名:DB_USERNAME  
パスワード:DB_PASSWORD  

* 自分で設定したtodoの定義  
id int(11) NULLなし AUTO_INCREMENT  
checkbox varchar(1)	NULLなし  
taskname varchar(100)	NULLなし  
memo varchar(100)  
deadline datetime	NULLなし  
priority varchar(1)	NULLなし  
