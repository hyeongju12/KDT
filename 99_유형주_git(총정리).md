# nano editor



### 1. nano(명령어 기반 시스템의 편집기 )

mac : control + shift + number

window : ctrl + 명령어



#  Git

### (버전을 통해) 코드 관리 도구 



## SCM & VCS

* scm : source code management(소스 코드 관리)
* vcs : version control System(버전 관리 시스템)



## Git 버전관리

> 중요 : Git은 **폴더단위** 로 코드를 관리



## 생활코딩(GIT)

* Git 목적 3가지
  1. Version  ***Git은 폴더단위로 코드 관리**
     1. 변경 이력
     2. 언제든 특정 시점으로 이동 가능 
  2. backup
  3. collaborate

* 실습

  * Version 관리

    * `git init .` : 현재 디렉터리를 git에게 관리하도록 하는 명령어

      * `(master)`프롬프트에 표시, `.git` 디렉토리 생성, 폴더 내 변경사항 모두 추적

      * git 해제시 `.git` 삭제

        

        ## git status : git 상태 확인 

    ```
    On branch master : master라고 하는 branch에 있어
    
    No commits yet : 아직 commit 없어
    
    nothing to commit (create/copy files and use "git add" to track)
    : commit 할 게 없어(트래킹 하고 싶으면 'git add' 명령어 사용해)
    ```

    ```
    Untracked files: 추적되지 않는 파일이 있어
     (use "git add <file>..." to include in what will be committed)
            a.txt(빨강)
    
    nothing added to commit but untracked files present (use "git add" to track) :
    
    ```

    ```
    Changes to be committed: commit될 변경 사항이 있어
      (use "git rm --cached <file>..." to unstage)
            new file:   a.txt(초록)
    ```

    ## git add [파일명]

    ```
    git add hello.txt // staging area[=Snapshot]에 올려라
    ```

    

    ## git commit

    > 버전을 생성하는 행위

    * commit(버전) 구성 요소
      * Hash(해쉬)
      * 작성자
      * 날짜
      * 커밋 메시지

    ```
    git commit -m "Message 1" // Repository로 올라감
    * -m 옵션 : git log에서 git commit을 하면서 남긴 메시지를 바로 
               입력해 줄 수 있도록함
               
    git config --global user.name "hyeongju you"
    git config --global user.email "hyeongju123@naver.com"
    위 내용은 git log에서 누가 / 언제 / 무엇을 수정했는지(comment가 입력되있을때)
    나오게 한다.
    
    working tree : 워킹트리에 아무 것도 없다
    nothing to commit : 버전으로 만들게 없다
    Author identity unknown : 작자 미상
    ```

    

    ## git log

    ```
    git log
    ```

    

    * 용어정리

      ```
      1) Repository : 버전이 저장되는 공간
      
      2) Working Tree : 아직 버전으로 만들어지기 이전 단계
      
      3) Staging area : Working area의 작업 파일중 버전 관리할 파일을 올리는 공간
         * 혹은  Index
      4) commit : 버전
      ```

​							Staging area에 있는것을 버전으로 만듬

![image-20210715173638148](C:\Users\hyeon\AppData\Roaming\Typora\typora-user-images\image-20210715173638148.png)

> **GIT 구조**

## `git log --oneline`

git log 요약 명령어



## `git checkout [commit number]`

해당 commit으로 돌아간다



## `git checkout master`

checkout 이전으로 돌아간다

### git & Visual studio Code

* git bash에서 `code [현재경로 / 작업을 원하는 경로]`
* Visual Studio Code에서 /recap 폴더 내 README.MD 파일생성
* git bash에서 git repository 생성
* git diff README.MD : README.MD 의 변경사항 확인



# Backup

* git hub new repository 생성
* remote 정보 입력
* git push

### `git remote`

* `git remote add` [저장소별명] [저장소 주소]
  * `git remote add origin https://github.com/hyeongju12/first.git`
  * `git remote` : 연결된 Remote repository 확인
  * `git remote -v` : 세부 정보확인
  * `git remote remove [name]` : remote 삭제

### `git push`

> 원격 저장소에 코드 백업

* `git push` [저장소 별명] [브랜치 이름]
  * git push origin master
