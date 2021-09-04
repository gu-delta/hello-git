# flow
1 作業ディレクトリ  
2 ステージングエリア  
3 リポジトリ（ローカル，リモート）  


# setting
git config --global user.name "gu_delta"  
git config --global user.email "gu-delta@example.com"  
git config --global color.ui true  

git help config  
ai143ns2px test % git config --help  
<!-- warning: failed to exec 'man': No such file or directory  
fatal: no man viewer handled the request -->  


# commit
mkdir hello-git  
cd hello-git  
git init  
<!-- … このディレクトリを使用することを宣言するもの。  
Initialized empty Git repository in /usr/home/ai143ns2px/html/hello-git/.git/ -->  

git add README.md  
git commit  
<!-- 説明を入力  
 1 file changed, 26 insertions(+)  
 create mode 100644 README.md -->  
git commit -m ""  
  
# log  
git log  
git log --oneline  
1行で履歴を表示  
git log -p  
変更内容を表示  
git log --stat  
どのファイルが何か所変わったか？  

# Change

# from GitHub
…or create a new repository on the command line  
echo "# hello-git" >> README.md  
git init  
git add README.md  
git commit -m "first commit"  
git branch -M main  
git remote add origin https://github.com/gu-delta/hello-git.git  
git push -u origin main  
…or push an existing repository from the command line  
git remote add origin https://github.com/gu-delta/hello-git.git  
git branch -M main  
git push -u origin main  
…or import code from another repository  
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.  

