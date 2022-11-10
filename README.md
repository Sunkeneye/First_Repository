# First_Repository

# Repo를 생성하면서 Nest.js폴더와 React.js폴더를 연결하던 중에 문제가 발생
# 원래는 First-Repository와 연결을 하려고 하였으나 아예 새로운 Repo를 만들어 연결하기 위해 Second_Repository를 생성하여
# 이 Repo와 연결하려고 GitHub의 공식 매뉴얼(...or push an existing repository from the command line)대로 하였으나

git remote add origin https://github.com/Sunkeneye/Second_Repository.git\n
git branch -M main
git push -u origin main
# 을  Git Bash에 입력하였으나

error: remote origin already exists.
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/Sunkeneye/First-Repository.git'
# 라는 에러가 발생

# 구글링을 통해 해결방법을 찾아 아래대로 입력하였으나
git remote remove origin
git remote add origin https://github.com/Sunkeneye/Second_Repository.git
git remote -v
  'Git Bash의 반응': origin https://github.com/Sunkeneye/Second_Repository.git (fetch)
  'Git Bash의 반응': origin https://github.com/Sunkeneye/Second_Repository.git (push)
git push origin master
  'Git Bash의 반응': error: src refspec main does not match any
  'Git Bash의 반응': error: failed to push some refs to 'https://github.com/Sunkeneye/Second_Repository.git'
# 라는 에러가 또 발생

# 다시 구글링을 하여 해결을 하려고 아래의 코드를 넣으려고 하였으나
git init
git add .
git commit -m "message"
git remote add origin "https://github.com/Sunkeneye/Second_Repository.git"
git push -u origin master
# git add . 에서 waring: ~ 같은 스크립트가 끝도 없이 작성되어 중단한 상황
    
Help...

