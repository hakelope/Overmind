# 깃(Git)의 기초 개념

<br>

개발자가 필수적으로 다룰 줄 알아야 하는 것은 파이썬, 자바, 그 어떤 것도 아닌 **깃(Git)** 이라는 생각이 든다. 그 정도로 중요하지만, 정작 내가 아는 것은 어디서나 불러오고 업데이트 할 수 있다는 정도이기에, 기초부터 다져 보기로 했다.

<br>

---

<br>

## 1. Git이란?

Git이란 **분산형 버전 관리 시스템(Version Control System)** 의 한 종류이다.

우리가 과제를 할 때에도 '과제(1)', '과제(1)(최종)', '과제(1)(최종)(1)' 과 같이 저장하는 경험이 한번 쯤 있었을 것이다.

이렇게 파일들을 **복사, 백업, 저장** 등을 한 것이 `버전 관리` 이다.

<br>

---

<br>

## 2. 버전 관리 시스템은?

우리가 무언가 실수를 했을 때에, 되돌리기로 그것을 만회하는 데에는 어느 정도 한계가 있다.

이를 예방하기 위해서 수정할 때마다 다른 파일로 저장해두는 방법도 있겠지만, 이는 굉장히 비효율적인 방법임을 직감할 수 있을 것이다.

<br>

그럴 때 사용하는 것이 `버전 관리 시스템`이다.

버전 관리 시스템은 크게 네 종류로 나뉜다.

-   디렉토리로 파일을 복사하는 방법 (과제(1),과제(2) 등)
-   로컬 VCS (간단한 데이터베이스로 변경 정보 관리)
-   중앙집중식 버전 관리 (CVCS)
-   분산 버전 관리 시스템

> Git이 대표적인 분산 버전 관리 시스템이다.

<br>

---

<br>

## 3. 왜 꼭 분산 버전 관리 시스템(Git)일까?

다른 버전 관리 시스템과 달리, 클라이언트가 **Clone**을 통해 모든 데이터를 백업함으로서 여러 이점이 생긴다.

-   서버에 문제가 생겨도 복제물로 다시 작업이 가능하다.
-   매번 중앙 저장소를 조회하지 않아도 개발을 진행할 수 있다.
-   협업 개발에 유용하다.

이러한 이유들로, 분산 버전 관리 시스템을 택하는 것이다.

<br>

---

<br>

## 4. 깃허브의 원리

![깃허브 원리](https://velog.velcdn.com/images%2Fmouse0429%2Fpost%2Fbe49e8d9-da5d-44fd-9b58-402ca334b306%2Fimage.png)

깃허브의 업로드 과정은 이렇다.

<br>
<br>

### Working Directory

실제로 작업하는 공간이다.

> 내 기준으로, 바탕화면의 OVERMIND 폴더가 해당된다.

<br>

### Staging Area

Local Repository에 저장하기 전에 저장되는 공간이다. 이 공간에서 프로젝트의 버전을 만들 수 있다.

> 내 기준으로, VScode에서 변경 사항을 저장했을 때, 깃허브 데스크탑에서 보이는 변경 사항? 인 것 같다.

<br>

### Local Repository

변경 내역들과 함께 파일이 저장되는 공간이다. 프로젝트의 변경사항이 기록된다.

> 내 기준으로, 깃허브 데스크탑에서 커밋을 진행했을 때 저장되는 곳이다.

<br>

### Remote Repository

**깃허브**에 해당되는, 온라인 상의 저장소이다.

> 내 기준으로, 깃허브 데스크탑에서 커밋 후 푸쉬까지 했을 때 저장되는 곳이다.

## 5. 용어

### commit

local Repository에 파일을 업로드 하는 것이다.

> Staging Area -> Local Repository

### push

local Repository에서 Remote Repository로 갱신하는 것이다.

> local Repository -> Remote Repository

### pull

Remote Repository에서 local Repository로 가져오는 것을 말한다. clone과 비슷하지만, local Repository와 Remote Repository가 연결되어 있어 일부 내용만을 동기화 시킬 때 사용한다.

> Remote Repository -> local Repository

### clone

Remote Repository에서 local Repository로 가져오는 것을 말한다.pull과 비슷하지만, local Repository와 Remote Repository가 연결되어 있지 않은 초기 상태에서 사용한다.
