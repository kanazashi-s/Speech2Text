Speech2Text
====

音声ファイルを指定すると、そのスクリプトを返す関数です。  
ほぼ[Google-Cloud-Speech-APIのサンプルコード transcribe.py](https://github.com/GoogleCloudPlatform/python-docs-samples/tree/master/speech/cloud-client)を使用しています。  
GitHubの練習のようなものです。  

<div align="center">
<img src=https://cloud.google.com/images/products/speech/speech-api-lead.png "Google-Speech-API">
</div>

## Description
[Cloud Speech-to-Text ドキュメント](https://cloud.google.com/speech-to-text/docs/?hl=ja)

## Demo
かなり見にくくなっておりますが、普通に実行しているだけです。  
![result](https://github.com/zacceydesuyo/Speech2Text/blob/development/Speech2TextDemo.gif)

## Requirement
- Python3.6.6  
- Jupyterで実行する場合、Anaconda3

## Usage
### 認証について  
ソースコード中の、
`os.environ["GOOGLE_APPLICATION_CREDENTIALS"]= "C:***/***/***.json"`  
を、訂正する必要があります。  
認証用jsonファイルを入手するには、Google Cloudにて、サービスアカウントの登録を行う必要があります。  
そののち、[認証の概要](https://cloud.google.com/docs/authentication/getting-started)によって、認証用jsonファイルを入手してください。  
このjsonファイルは、他のプロジェクトでも使うことができます。  
`os.environ["GOOGLE_APPLICATION_CREDENTIALS"]= "C:***/***/***.json"`  
は、環境変数に書き込んでおくのが最もスマートではありますが、このようにソースコード中で指定することもできます。  
  
### .ipynbを使う場合
- コンソールを開き、任意の場所で以下を実行し、ファイルをダウンロードしてください。  
`git clone https://github.com/zacceydesuyo/Speech2Text.git`  
- Speech2Textフォルダ内の以下を実行し、必要なライブラリをインストールしてください。  
`pip install -r requirements.txt`   
- 任意の環境(デモGifではJupyterLab)で"Speech2Text_note.ipynb"を開き、  
`os.environ["GOOGLE_APPLICATION_CREDENTIALS"]= "C:***/***/***.json"`  
を訂正したのち、上から実行してください。  
  
### .pyを使う場合
- コンソールを開き、任意の場所で以下を実行し、ファイルをダウンロードしてください。  
`git clone https://github.com/zacceydesuyo/Speech2Text.git`  
- コマンドライン上で以下を実行し、必要なライブラリをインストールしてください。  
`pip install -r requirements.txt`   
- 任意のエディタで"Speech2Text.py"を開き、以下を訂正してください。  
`os.environ["GOOGLE_APPLICATION_CREDENTIALS"]= "C:***/***/***.json"`  
- コマンドライン上で、以下を実行してください。
`python Speech2Text.py minami.wav`
  
### .mp3のファイルや、ステレオ音声を用いる場合  
- "Suit_Encoding.ipynb"に、.mp3→.wavへの変換、ステレオからモノラルの変換を行うソースが記載されています。  
- 実行するためには、[ffmpeg](https://ffmpeg.zeranoe.com/builds/)が必要です。ダウンロード・解凍ののち、binディレクトリ内の.exeファイルを全て、カレントディレクトリへ移動してください。  
- (2019/1/23現在)binディレクトリにパスを通すことにより、.exeファイルを移動することなく実行したいと思っていますが、私の環境ではできませんでした。でき次第、ソースを更新します。  
  
## Install
必要なライブラリは、'requirements.txt'に記述してあります。  
そのため、以下のコマンドを任意の場所で実行していただくことにより、必要なライブラリがすべてインストールされます。  
`pip install -r requirements.txt` 

## Contribution  
お待ちしております。
フォークして、新しいブランチを作ってそこに変更点をプッシュしておいてください。
プルリクエストもお願いします。

## Licence  
This source is licensed under the Apache License, Version2.0

## Author
zashio
