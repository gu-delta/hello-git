# Gitとは
**Gitとはバージョン管理システムで，次の3つの状態に分けられる.**  
1. 作業ディレクトリ  
1. ステージングエリア  
1. リポジトリ (ローカル, リモート)

# 設定
**名前とメールアドレスを設定する.**  

	git config --global user.name "gu_delta"
	git config --global user.email "gu-delta@example.com"
		
		
**メッセージを色分けする.**

	git config --global color.ui true


**設定の一覧を確認する.**  

	git config -l

# リポジトリの作成からコミットまでを行う
**ディレクトリを作成して移動する.**

	mkdir hello-git  
	cd hello-git  


**現在のディレクトリをgitで使用することを宣言する.**

	git init  


**ファイルをステージングエリアへ追加する.**  

ファイル名を指定して追加する場合. (複数の場合はカンマ区切りで指定する.)

	git add README.md
	
現在のディレクトリ以下にあるファイルをまとめて追加する場合.

	git add .


**リポジトリにファイルをコミットする場合.**

オプションを指定しない場合は, エディタが立ち上がってコメントの指定を求められる. 

	git commit  

`-a` オプションを指定すれば, `git add`を省略するワークツリーで変更済みのファイルをコミットすることができるが，*ファイルの追加などは反映されない*ことに注意が必要.

	git commit -a  
  

`-m` オプションを指定すれば, エディタを立ち上げずに同時にコメントを指定できる.

	git commit -m "コメント"  
  

# コミットのログを確認する
**ログを確認する**

オプションを付けない場合は, 複数行でログが表示される。

	git log

`--oneline`オプションをつけることで, 1行表示でログを確認できる. 

	git log --oneline
	
	
**ファイルの変更内容を確認する.**

	git log -p 
	
	
**どのファイルが何カ所変わったかを確認する.**  

	git log -stat


# リモートリポジトリに反映する

**認証情報を毎回聞かれないように保存する**

	git config --global credential.helper store


**送信する.**

	git remote add origin https://github.com/gu-delta/example.git
	git branch -M main
	git push -u origin main
	
