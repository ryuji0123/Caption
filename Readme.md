# VIM (Varying Icon and Message)

### Installation
まずこのレポジトリをcloneします

```sh
$ git clone https://github.com/ryuji0123/Caption.git
```
次に自分のGoogle Drive上で以下のディレクトリ構成を作ります。
```sh
MyDrive/Colab Notebooks/Caption
```
Colab Notebooksは(無ければ)新規で作成してください。  過去にColabを使った場合は既にディレクトリが存在するのでそれを流用してください。

Captionについては先ほどcloneしたものをそのままuploadしてください。

最後に必要なmodelファイルをネット上からdownloadし、手動でuploadします(githubのファイルサイズ制限に引っかかってしまったのでレポジトリには含められなかったです、面倒ですみません)。

linkから3種類のmodelファイルをdownloadし、以下のディレクトリ構成になるようuploadしてください。

| Link | Directory |
----|----
| [model.vec][model] | Caption/model.vec |
| [encoder-2-1000.ckpt][encoder] | Caption/pytorch-tutorial/tutorials/03-advanced/image_captioning/models/encoder-2-1000.ckpt |
| [decoder-2-1000.ckpt][decoder] | Caption/pytorch-tutorial/tutorials/03-advanced/image_captioning/models/decoder-2-1000.ckpt |

# Execution
以下のファイルをcolab上で開いてください。
```sh
Caption/caption.ipynb
```
以降はこのファイル内について説明をします。  
まず、以下の部分を書き換えてください。
```sh
#自由に書き換える部分
USER_TOKEN = 'slack の user token'
USER_ID = 'slack の user id'
IMG_PATH = '/content/drive/My Drive/Colab Notebooks/Caption/pytorch-tutorial/tutorials/03-advanced/image_captioning/img/画像のファイル名'
```
slackのuser token, user idについては以下のサイトを参考に確認してください。user tokenは過去に発行したことがない場合は新規で発行する必要があることに注意してください。

[API トークンの生成と再生成][slack-api]  

[SlackのIDとは何ですか？][slack-id]

画像については該当するディレクトリに好きな画像を入れ、そのファイル名をIMG_PATHに設定してください。なお、絶対PATHとして正しければ任意のディレクトリを指定して良いです。


あとは実際に全てのセルを実行するだけです。コメントアウトはcleanな状態からの実行を想定して念の為残してありますが、無視してください。

   [model]: <https://drive.google.com/file/d/11rwXicN6-0ttpM0LOHcLQGZTx4wMQ5pT/view?usp=sharing>
   [encoder]: <https://drive.google.com/file/d/1Ld8MKb4glgsNiqml-OcB1auquViCnwOq/view?usp=sharing>
   [decoder]: <https://drive.google.com/file/d/1a8qUUTq8m8IsFBNRSLWUMC3qQv_znIFx/view?usp=sharing>
   [slack-api]: <https://slack.com/intl/ja-jp/help/articles/215770388-Create-and-regenerate-API-tokens>
   [slack-id]: <http://help.receptionist.jp/?p=1100>
   
