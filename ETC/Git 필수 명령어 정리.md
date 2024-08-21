![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F99AF97395AA61E4C0B)

## Git 필수 명령어 정리
- git init: git 저장소 초기화
- git clone: 원격 저장소 복제
- git add: 변경된 파일을 스테이징 영역에 추가
- git commit: 스테이징된 변경 사항 커밋
- git status: 현재 상태 확인
- git log: 커밋 기록 조회
- git branch: 현재 브랜치 목록을 확인하거나 새 브런치를 생성
- git checkout: 다른 브랜치로 전환
- git merge: 특정 브랜치의 변경 사항을 현재 브랜치로 합침
- git pull: 원격 저장소의 변경 사항을 가져와 병합
- git push: 로컬 커밋을 원격 저장소에 업로드
- git stash: 임시로 작업 중인 변경 사항을 저장해 두고, 나중에 다시 꺼내서 작업할 수 있다.

## git Cherry-pick
- 특정 커밋을 선택해서 현재 브랜치로 복사하는 작업
- 특정 커밋만 골라서 브랜치에 적용하고 싶을 때 사용
- 예를 들어, 여러 개발건이 개발계에 검증되지 않은 채 배포되어 있는 상황에서 특정 개발 건만 검증계로 긴급 배포 해야 하는 경우 사용할 수 있다.
- 하나의 커밋만 선택하는게 아닌, 여러 개의 커밋도 선택할 수 있다.
```text
(사용 예시)
git cherry-pick abc1234
```
- cherry-pick 도중에도 충돌이 발생할 수 있으며, 복사된 커밋은 원본 커밋과 별개의 새로운 커밋으로 추가되므로, 히스토리 중복에 주의하며 사용해야 한다.

## git Rebase
- git에서 한 브랜치에서 다른 브랜치로 합치는 방법은 merge와 rebase 가 있다.
- merge와 rebase는 실행결과는 같지만, 커밋 히스토리가 달라진다는 차이가 있다.
- 현재 브랜치의 기반(base)를 다른 브랜치의 끝으로 옮겨서 브랜치의 변경 사항을 재정렬하는 작업.
```text
(사용 예시)
git checkout feature-branch
git rebase main
```
- 위 명령어를 수행하면 feature-branch의 커밋들이 재배치된다.
- 리베이스 후, main 브랜치에 merge하면 선형적인 깔끔한 커밋 히스토리를 유지할 수 있다.
- 주의사항: rebase 중 충돌이 발생할 수 있다.

## Submodules
- 하나의 Git 저장소에 다른 저장소를 포함시키는 기능


## Git GUI 어플리케이션
- Sourcetree
- Fork
    - min 파일과 같은 압축 파일에서 merge시, 충돌이 일어나면 Sourcetree에서는 확인이 불가능하다.
    - 위와 같은 상황에서는 Fork를 사용하면 해결할 수 있다. 