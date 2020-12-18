# 1-Command-Line

UNIXのコマンドラインの Tutorialです。
新人向けのRepositoryになります。

- パスの意味と使い方
- ls
- pwd
- cat
- cd
- cp
- mv
- mkdir
- rm
- chmod
- grep
- scp
- ssh
- kill

- パスの意味と使い方
2つのパスの書類があります: AbsoluteとRelative
absoluteは今のDirectoryを認識せず、システムの中のdirectoryを指定する物です
relativeはDirectoryを認識して、入っているDirectoryからのファイルパスです

Absolute例:
/home/user/docs/Letter.txt   (システムのどこからでもLetter.txtのパス指定)
Relative例:
./Letter.txt                 (docs Directoryからのパス指定)

- LSコマンド

lsはlistという意味で
フォルダの中のファイルをlistしてくれるコマンドです

例:
ls /home/user/docs           (このコマンドを打つとdocsフォルダのファイルリストが見れます)
ls -la                       (今のDirectoryのファイルリストプラス権限)

maru@coolpc demo % ls
HELP.md         mvnw            mvnw.cmd        pom.xml         src             target

- PWDコマンド

pwdは今のDirectoryの名前をプリントするコマンドです

例:

maru@coolpc demo % pwd
/Users/maru/Desktop/demo

- CATコマンド

ファイルの中身をプリントするコマンドです
いくつかのファイルに紐づいてプリントもできます

例:
maru@coolpc demo % cat Letter.txt      (を打つとLetter.txtの中身全て表示されます)

- CDコマンド

Change Directory (directoryをチェンジするコマンドです)

例:
maru@coolpc demo %cd /Users/maru/Desktop
maru@coolpc Desktop %

- CPコマンド

ファイルかDirectoryをコピーするコマンドです
パラメターが2つ必要です: ファイルが存在するところ、コピーの場所

例:
maru@coolpc demo % cp Letter.txt ../

- MVコマンド

ファイルかDirectoryを移動するコマンドです
パラメターが2つ必要です: ファイルが存在するところ、移動の場所

例:
maru@coolpc demo % mv Letter.txt /Users/maru/Desktop


- MKDIRコマンド

Directoryを作成するためのコマンドです

例:
maru@coolpc demo % mkdir project

- RMコマンド

ファイルかDirectoryを消すコマンドです
一回消したらは永遠だから気をつけてください


例:
maru@coolpc demo % rm -rf project    (最近だからDirectoryを消したら中身も消される)
maru@coolpc demo % rm Letter.txt


- CHMODコマンド

権限をチェンジできるコマンドです
https://qiita.com/shisama/items/5f4c4fa768642aad9e06

- GREPコマンド

ファイルの中身を検索できるコマンドです

例:
maru@coolpc demo % grep 'hello' Letter.txt    (この書き方ではHelloが書いてあるラインを表示してくれます)
maru@coolpc demo % grep -R 'httpd' .          (この書き方でこのフォルダとサブフォルダーにhttpdと書いてあるファイルところを探してくれる)

- SCPコマンド

リモートシステムから/までファイルをCopyするコマンドです

例:
maru@coolpc demo % scp -i demo/coolkey.pem -r file.txt ec2-user@my.ec2.id.amazonaws.com:/home/ec2-user

- SSHコマンド

リモートシステムにアクセスするコマンドです

例:
maru@coolpc demo %　ssh -i demo/coolkey.pem ec2-user@my.ec2.id.amazonaws.com


- KILLコマンド

システムにあるプロセスをStopするコマンドです

maru@coolpc demo % kill 7　　　　　　　　　　　　(Process 7番がストップされる)


