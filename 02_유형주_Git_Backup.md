# GIT CLI Backup



## 1. GIT Backup 절차

![push](D:\1.png)

* 로컬 저장소(집)에서 원격 저장소(서버)에 저장

![clone](D:\2.png)



* 로컬 저장소(회사)에서 작업을 하려면 원격 저장소에 있는 버전들을 복제해야 하는데 이 작업을

  `clone`이라고 한다.

  ![push2](D:\3.png)

* 로컬 저장소(회사)에서 작업을 다하고 `push`를 통해 원격 저장소에 변경된 버전을 commit 한다.

![pull](D:\4.png)

* 로컬 저장소(집)에서 작업이 추가로 필요하여 원격 저장소에 저장된 변경된 commit을 받아오는 것을

  `pull`이라고 한다.



# 2. GIT backup 실습

* Github에 new repository를 생성한다.

  * https://github.com/hyeongju12/organized_class_materials-.git

* Git bash에서 로컬 저장소에 저장된 Commit을 Remote 저장소로 `PUSH` 하는 작업을 해준다

  * ```
    git remote add origin https://github.com/hyeongju12/organized_class_materials-.git
    ```

    * 원격 저장소를 **origin** 별칭으로 저장한다는 명령어이다.

  * ```
    git remote
    ```

    * 원격 저장소가 어떤게 있는지 확인

  * ```
    $ git push
    fatal: The current branch master has no upstream branch.
    To push the current branch and set the remote as upstream, use
    
        git push --set-upstream origin master
    # 위 같이 오류가 발생하면 아래 git push --set-upstream origin master을 
      입력해 준다. *위 의미는 현재 연결된 remote repository를 기본 저장소로 설정
      한다고 이해하면 편할듯*
    ```

  * ```
    git push --set-upstream origin master
    ```

  * ```
    git push -u origin master  / 지역저장소 master와 원격저장소의 master가 연결되면서 push
    ```

# 3. GIT Clone  실습

* 다른 로컬 저장소에서 원격 저장소에 있는 자료들을 받을 수 있게  `clone`을 실습해본다.

![clone](D:\5.png)

* ```
  https://github.com/hyeongju12/organized_class_materials-.git
  ```

  ![pci](D:\6.png)

* Github에서 위 그림과 같이 `clone` 주소를 복사한다.

* Git bash에서 `git clone`을 사용하여 Remote repository에 있는 commit을 복제해 온다.

```shell
git clone https://github.com/hyeongju12/organized_class_materials-.git [저장 디렉토리명]
```

* git clone [복제 대상 Remote repository 주소] [저장디렉토리명] 
  * 저장 디렉토리명을 입력하면 디렉토리가 생성되면서 복제 디렉토리가 하위에 생기게 된다.



# 4. Git Pull 실습

* Remote Repository에 있는 파일을 local repository 로 가져오는것(같은 원격 저장소를 사용중 (연결중))

* ```
  git pull
  ```

* 위에 명령을 입렵하니 작동을 안하면서 아래와 같은 내용이 나온다.

* ```
  $ git pull
  remote: Enumerating objects: 5, done.
  remote: Counting objects: 100% (5/5), done.
  remote: Compressing objects: 100% (2/2), done.
  remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0
  Unpacking objects: 100% (3/3), 848 bytes | 70.00 KiB/s, done.
  From https://github.com/hyeongju12/organized_class_materials-
     5bdb2bf..f869b73  master     -> origin/master
  There is no tracking information for the current branch.
  Please specify which branch you want to merge with.
  See git-pull(1) for details.
  
      git pull <remote> <branch>
  
  If you wish to set tracking information for this branch you can do so with:
  
      git branch --set-upstream-to=origin/<branch> master
  
  ```

* `git pull <remote> <branch>` <remote> : 연결되있는 원격저장소 <branch> : 어떤 브랜치의 자료를 가져올건지  branch 명을 입력하라는 말이다.

* `git pull origin master`

* 위 같이 지정하고 입력하였더니, 자료를 잘 가져왔다. `git log`를 입력해서 두 개의 작업공간이 같은 commit

  log를 가지고 있는지 확인해 보자.

* ```
  git branch --set-upstream-to=origin/master master
  ```

* 위 명령어를 입력하면 local master가 원격 repository의 origin/master를 연결 하게 한다.
* 그러면 `git pull` 만으로도 명령이 잘 수행된다.

> 위 Git 작업 순서 git pull > git add > git commit > git push 



# Git amend

commit이 잘못작성되여 변경할때 쓰는 명령어.. 지금 지식으로는 하지말자.. 



# 용어정리

`host` : 인터넷에 연결된 컴퓨터

`hosting` : 인터넷에 연결되어서 원격으로 사용할 수 있는 서버를 임대해 해주는 서비스

`git hosting` : 로컬저장소의 버전을 업로들 할 원격 저장소를 임대해주는 서비스

`Framework is open-source` : 사용자 서버에 설치할 수 있는 여부

`public` : opensource 프로젝트

`private` : 허가된 사용자만 참여 / 한달에 만원