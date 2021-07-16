# CLI 명령어

## `pwd(print working directory)`

* 현재 경로 출력

##  `ls`

현재 경로에 있는 파일, 디렉터리 등 출력

## `cd`

* `chage directory`
* `~` : home directory
* `tap` 누르면 자동완성
* `..` : 상위 디렉토리



## `mkdir`

* 폴더 생성



## `rm -r`

* 디렉터리 삭제



## touch [파일명]

* 파일생성

* `rm 파일명` : 파일삭제



## `mv` [파일명] [바꿀 파일명]

파일명 변경

파일경로 변경



## `cp` [파일명] [복사할 경로명]



# 추가학습

* `명령어;[다음 실행할] 명령어`
  * 예) `mkdir test;cd test`
* `pipeline 개념:`하나의 프로그램의 결과를 다른 프로그램의 입력, 하나의 프로세스의 결과를 다른 프로세스의 입력으로 준다
  * `ls --help | grep sort` :` ls` 프로그램의 출력(`help`)를 `grep` 프로그램의 입력값으로 사용하여 `grep`의 결과를 출력(`sort`가 포함되어있는 행 출력)했다.

