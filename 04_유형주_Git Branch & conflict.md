# Git Branch & conflict

### 1.1 git branch  실습

* 실습환경 : bash창 2개 사용
  * 하나는 명령어 실행, 하나는 로그 확인
* `git log --all --graph --oneline` 
* `git branch [생성 branch명]`



### 1.2 merge 실습

![image-20210716171423138](C:\Users\hyeon\AppData\Roaming\Typora\typora-user-images\image-20210716171423138.png)

* m지점을 `merge commit`이라고 한다.

* base : 합치려고 하는 공통의 조상

* merge를 수동으로 할 수 없음..  * 자동으로 merge가 되나 자동으로 안돼는 부분은 사용자에게 알려줌

* ```
  git branch o2
  nano master.txt
  git add master.txt
  git commit -am "work 2"
  git commit --amend *master add
  git checkout o2 
  nano o2.txt o22
  git add o2.txt
  git commit -m "o2 work2"
  ```

* master branch에 o2 branch를 병합

* ```
  git checkout master
  git merge o2
  * o2 branch를 merge하면서 생기는 merge commit
  git reset --hard [리셋하고 싶은 버전명]
  ```

# 동일한 파일 수정시 병합



* ```
  nano work.txt
  ># title
  >content
  
  ># title
  >content
  git add work.txt
  git commit -m "1"
  
  git branch o2
  nano work.txt > master branch에서 작업
  
  git commit -am "master work2"
  
  git checkout o2
  nano work.txt > o2 branch에서 작업
  git add work.txt
  git commit -m "o2 work2"
  ```

* o2 branch의 내용을 master로 병합

* ```
  git checkout master
  git merge o2 > o2를 master로 merge한다.
  cat work.txt
  ```

## 동일한 파일의 동일한 부분을 수정시 병합(conflict)

> 두 개의 브랜치가 같은 이름의 파일의 같은 부분을 수정했을때 git은 자동으로 merge하지 못한다.
>
> 사용자의 확인 후에 병합을 수행한다.

* ```
  git init manual-merge
  cd ./manual-merge
  
  nano work.txt
  > #title
  > content
  
  > #title
  > content
  
  git add work.txt
  git commit -m "work1"
  
  git branch o2
  
  git log
  
  master에서 중간 부분 수정
  git -am "master work 2"
  
  git checkout o2
  o2에서도 중간 부분 수정
  git commit -m "o2 work 2"
  
  git checkout master
  git merge o2
  > CONFLICT 발생 : 자동으로 merge하는데 실패했으므로 충돌을 해결한 후에 시도
  git status
  > both modified
  
  <<<<<HEAD 현재 브랜치의 내용 master내용
  =======
  >>>>>o2 브랜치의 내용
  
  둘중의 맞는 내용을 선택하던가 '==='을 삭제한다.
  
  git add work.txt > 충돌을 해결했어
  git commit -m "modified"
  
  
  ```

* 



