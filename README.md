# 개발중입니다 팀 공식 개발 규칙

> 만약 당신이 팀으로 들어왔다면 **무조건** 읽어야 합니다.

**이 문서는 아직 미흡하여 많은 개선이 필요합니다! 아주 사소한 개선점이라도 있다면 언제든지 [PM](https://github.com/Roharui)에게 연락주세요!**

## 당신이 처음 들어왔다면?

> 다음 [문서](NEWER.md)부터 읽어주세요!

## 개발 규칙

> 보다 자유로운 개발을 위한 최소한의 규칙입니다. 말그대로 최소한의 규칙이므로 보다 융통성있고 유연한 방식이 있으면 그 방식을 채용하도록 합시다. 규칙의 개선점이 있다고 생각하는 경우 언제든지 말씀해주세요.

> [개발 순서도 정리본](https://drive.google.com/file/d/1GCQ8DqOKEC_WgVHo5nX-6UQpZGUw6G-t/view?usp=sharing) 확인 바랍니다.

1. 개발에 관련된 모든 사항은 repo의 `issue`탭에 정리합니다.
    1. 무조건 [라벨](#라벨)을 달아둡시다.
    2. 이슈 내용에는 간단한 설명과 함께 `하위 기능`들을 달아줍니다.
    3. `하위 기능`은 체크박스 형태로 나타냅니다.
    4. 개발중 `문제`(버그X 기획상의 문제점)가 생긴다면 해당 `issue`에 코멘트를 남기고 다음 회의에 그 문제에 대해 토의합시다.
2. 모든 프로젝트는 `github project`로 개발 일정을 관리합니다.
    1. 개발 목록: 자신이 담당하고 싶은 기능이 있다면 여기서 자신이 개발하겠다고 선택합시다.
    2. 개발 중: 열심히 개발합니다! 개발 중간중간 `코드 리뷰`를 한다면 더욱 좋습니다!
    3. 개발 완료: 버그가 있는지 없는지 검사하여 버그가 있다면 `issue`에 코멘트를 남깁시다. (버그는 어쩔수 없이 생기기 마련입니다! 망설임없이 `issue`에 등록합시다.)
    4. 디버그 중: 개발완료 탭에서 찾아낸 버그를 고치며 테스트 코드를 작성합니다.
    5. 디버그 완료: 기능이 완성되었습니다! `issue`를 닫습니다.
3. 일주일에 1번은 회의를 합니다. 회의하는 날은 일정을 비워둡시다.
    1. **1시간 이상 회의를 하지 않습니다.** (불가피한 이유로 1시간이 넘어간다면 10분 휴식후 다시 회의를 진행합니다.)
    2. 회의에서는 지난 일주일동안 개발된 프로젝트의 문제점에 대해 생각해봅시다.
    3. 한가지 문제에 너무 오랫동안 파고들지 말도록 합시다.
    4. 회의록은 디스코드에 작성합니다.
4. 모든 `repo`에는 `gitflow`를 사용합니다. 하지만 융통성 있게, 유연하게 사용합시다.
    1. 상세한 내용은 아래 [gitflow](#gitflow)를 참고합시다.
5. [커밋 메세지](#커밋-메세지)와 [기능 브랜치](#기능-브랜치)는 아래 형식을 지켜주세요!
6. `테스트 코드`를 저는 **굉장히** 좋아합니다만, 테스트 코드를 짜느라 일정을 놓치는 경우는 없도록 합시다.
7. `코드 리뷰`는 중간중간 시간이 남는 팀원에게 부탁하도록 합시다.
    1. `코드 리뷰`가 필요없을 정도로 가벼운 기능이라면 생략하셔도 상관없습니다.
8. `코딩 컨벤션`은 `Formatter`를 이용하고 있습니다. [이곳](#코딩-컨벤션) 참고 바랍니다.
9. 서로 돕고 배우며 재밌게 개발합시다!

## gitflow

> 유연성과 융통성을 위해서 별다른 제한을 두지 않았습니다. 하지만 되도록 규칙을 따르도록 합시다.

1. `master` 브랜치는 배포용 브랜치입니다. 모든 기능이 완료된 후에 merge하도록 합시다.
    1. 실수로 `master` 브랜치에 `feature` 브랜치를 merge 하지 않도록 합시다.
    2. 생성된지 5일이 지난 브랜치는 리뷰를 하지 않는 리뷰어가 남아있더라도 merge 합니다.
    3. merge 된 브랜치는 삭제합니다.
2. `develop` 브랜치는 개발용 브랜치 입니다. 
    1. 자동배포 시스템이 적용되어 있으니 개발완료후 디버그하는데 이용하도록 합시다.
    2. 만일 자동 배포가 되지 않는다면 `PM`에게 연락 바랍니다.

## 커밋 메세지

> *표시가 들어간건 필수적으로 들어가야 하는 것입니다

```
[type*]: [message*] 

[body*]

[footer]
```

- `type`: 이 커밋이 어떤 종류의 일을 수행했는지 나타냅니다.
    - `feat`: 기능을 추가했을때
    - `fix`: 버그를 수정했을때
    - `docs`: 문서를 수정했을때
    - `test`: 테스트를 추가/수정했을때
- `message`: 이 커밋에 대한 짧은 설명입니다.
- `body`: 이 커밋에 대한 상세한 내용입니다.
- `footer`: 아무거나 적으셔도 됩니다.

```
예시 )
feat: 스크린샷 업로드 기능 개발 완료

스크린샷 업로드 API json 형식으로 변경
사진 데이터를 RAW 데이터로 변경후 전달함

근데 form 안쓰고 보내도 되는거 맞아요?
```

## 기능 브랜치

```
f/<작성자>/#<이슈번호>
```

## 라벨

> `issue`에는 `label`을 필수적으로 달아줍니다.

|이름|설명|
|---|-----|
|`B-E`|백엔드 담당|
|`BUG`|무언가가 작동하지 않음|
|`CI/CD`|CI/CD 관련|
|`Design`|UI/UX 개선|
|`Documentation`|문서 개선 또는 추가|
|`F-E`|프론트엔드 담당|
|`feature`|기능 일람|
|`HELP!`|도움! 필요!|
|`TEST`|테스트 관련|

## 버전 관리

> 버전관리는 서비스 이후 진행합니다.

## 코딩 컨벤션

> 공식적인 `Javascript`의 코딩 컨벤션은 따로 존재하지 않습니다. 하지만 한 프로젝트를 생성할때 자동으로 가져오는 `ESLint`와 `Preitter`를 사용하고 있습니다.

- `Javascript` 또는 `Typescript`는 `ESLint`와 `Preitter`를 사용합니다. [참고 문서](https://veggie-garden.tistory.com/13)
- `Java`는 Language Support for Java(TM) by Red Hat을 사용합니다 [참고문서](https://marketplace.visualstudio.com/items?itemName=redhat.java)
- `Python`의 경우 `flake8`, `Black`의 기본설정을 사용합니다. [참고 문서](https://engineer-mole.tistory.com/282)

더 자세한 세팅 방법은 이 [문서](ENVIRONMENT.md)를 확인합시다.
