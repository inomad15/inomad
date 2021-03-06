## 로컬서버의 파일을 깃허브에 올리기

1. git config --global user.name "이름"
2. git config --global user.email "깃허브 메일주소" // 매번 물어보는 귀찮음을 피하기 위해 설정.

3. mkdir ~/MyProject   // 로컬 디렉토리 만들고
4. cd ~/myproject      // 디렉토리로 들어가서
5. git init            // 깃 명령어를 사용할 수 있는 디렉토리로 만든다.
6. git status          // 현재 상태를 훑어보고
7. git add 화일명.확장자  // 깃 주목 리스트에 화일을 추가하고 or
8. git add 이 명령은 현재 디렉토리의 모든 화일을 추가할 수 있다.
9. git commit -m “현재형으로 설명” // 커밋해서 스냅샷을 찍는다.

10. git remote add origin https://github.com/username/myproject.git // 로컬과 원격 저장소를 연결한다.
11. git remote -v // 연결상태를 확인한다.
12. git push origin master // 깃허브로 푸시한다.

## [원격 저장소를 로컬서버로 복사하기](https://help.github.com/articles/fetching-a-remote/)

원격 저장소에서 로컬 컴퓨터로 코드를 다운로드하기 위해서 `clone`과 `fetch`를 쓸 수 있다. `merge`는 다른 사람의 작업내용을 나의 작업과 합칠 때 사용한다. `pull`은 `fetch`와 `merge`를 합친 기능이다.

- 다른 사람의 저장소를 모두 카피하고 싶을 때는 `clone`을 쓴다.

 `git clone https://github.com/USERNAME/REPOSITORY.git`

- 다른 사람의 새로운 작업을 가져오고 싶을 때는 `fetch`를 쓴다.

 `git fetch remotename`

- 다른 사람의 변화된 작업 내용과 당신의 새로운 작업내용을 합칠 때는  `merge`를 쓴다.

 `git merge remotename/branchname`

- `fetch`와 `merge`를 함께 실행하고 싶을 때는 `pull`을 쓴다.

 `git pull remotename branchname`

## [원격 서버와 함께 작업하기](http://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)

깃 프로젝트를 다른 사람들과 공동으로 작업하기 위해서는 원격 저장소를 다루는 법에 익숙해져야 한다. 원격 저장소에 데이터를 자유롭게 넣고 빼는 방법을 알아야 한다.

- 깃의 원격 저장소를 복제한다.

`$ git clone https://github.com/schacon/ticgit
Cloning into 'ticgit'...
remote: Reusing existing pack: 1857, done.
remote: Total 1857 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (1857/1857), 374.35 KiB | 268.00 KiB/s, done.
Resolving deltas: 100% (772/772), done.
Checking connectivity... done.
$ cd ticgit
$ git remote
origin`
