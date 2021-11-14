
# reset
> 원하는 커밋으로 브랜치를 되돌리기


#### reset의 option

   - Soft
   - Mixed
   - Hard

<br>

## 1. Soft
  
   - 원하는 커밋으로 이력을 되돌림
   - 되돌린 커밋버전 이후의 변경사항은 스테이지아래에 존재

   - 작동방식

  <br> 
- 작동 전 모습
<img src="https://user-images.githubusercontent.com/89792058/141664788-547c4f05-5542-46c8-9fea-fb95b15096da.png" width="500" height="350"/>
<img src="https://user-images.githubusercontent.com/89792058/141665190-529d16c8-0e50-49e7-86fb-4dd16751fb30.png" width="500" height="250"/>
- 1단계: HEAD 이동
<img src="https://user-images.githubusercontent.com/89792058/141664811-7732cc2c-4a31-497a-aefa-c139354cafb2.png" width="500" height="350"/>
checkout 명령처럼 HEAD가 가리키는 브랜치를 바꾸는 것은 아님.
HEAD는 작업하던 현재 브랜치 내의 커밋을 바꿈. <br>
- 2단계: 종료
<img src="https://user-images.githubusercontent.com/89792058/141664824-f6bca6ba-7bf2-4b5e-becc-049c5f107f7f.png" width="500" height="250"/>

> Index나 워킹 디렉토리는 그대로 놔두고 브랜치가 가리키는 커밋만 이전으로 되돌린다.

<br>

## 2. Mixed
  
   - 원하는 커밋으로 이력을 되돌림
   - 되돌린 커밋버전 이후의 변경사항은 스테이지 위에 존재

   - 작동방식

  <br> 
- 작동 전 모습
<img src="https://user-images.githubusercontent.com/89792058/141664788-547c4f05-5542-46c8-9fea-fb95b15096da.png" width="500" height="350"/>
- 1단계: HEAD 이동
<img src="https://user-images.githubusercontent.com/89792058/141664830-9d5869ff-fe95-40c9-aaf4-26f69b759ca1.png" width="500" height="350"/>
- 2단계: 종료
<img src="https://user-images.githubusercontent.com/89792058/141664836-82247fe0-ea0f-4a0a-a77e-fdd79c086314.png" width="500" height="250"/>

> Index 업데이트. Staging Area 를 비움.

<br>

## 3. Hard

   - 원하는 커밋으로 이력을 되돌림
   - 커밋하지 않은 변경사항 모두 삭제

   - 작동방식

  <br> 
- 작동 전 모습  
<img src="https://user-images.githubusercontent.com/89792058/141664788-547c4f05-5542-46c8-9fea-fb95b15096da.png" width="500" height="350"/>
- 1단계: HEAD 이동
<img src="https://user-images.githubusercontent.com/89792058/141664841-38380745-b06c-434e-9e72-588a6394cba5.png" width="500" height="350"/>
- 2단계: 종료
<img src="https://user-images.githubusercontent.com/89792058/141664844-f8309e91-7e48-4cf2-a493-4031ef4161ba.png" width="500" height="250"/>

> Index와 워킹 디렉토리 업데이트. 워킹 디렉토리의 파일까지 강제로 덮어씀.

<br>

## 4. 원격 브랜치 반영

   - reset은 히스토리를 수정하는 작업.
   - 로컬저장소에서 reset 한 변경사항을 원격 브랜치에도 반영하려면? [강제 푸시(force명령어)]
   - 따라서 나만 쓰는 브랜치에서만 하는 것을 권장. 다른사람의 히스토리가 꼬일 수 있음.




<br>


# revert
> 변경사항을 취소하는 새로운 커밋 만들기

- cherry-pick 명령의 반대
- 해당 커밋을 되돌리는 커밋을 새로 생성하는 것.

<br>

# Git으로 관리하는 파일의 상태
1. untracked
   - 추적안됨
      : 한번도 커밋되지 않은 파일


2. tracked 
   - 스테이지됨(staged)
        : 커밋할 파일로 선택해놓은 파일. add명령어
   - 수정없음(unmodified)
        : commit명렁어
   - 수정함
        : commit 이후 파일을 수정한 상태.
