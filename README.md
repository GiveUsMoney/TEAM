# 개발중입니다 팀 공식 개발 규칙

> 만약 당신이 처음 팀으로 들어왔다면 **무조건** 읽어야 합니다.

**이 문서는 아직 미흡하여 많은 개선이 필요합니다! 아주 사소한 개선점이라도 있다면 언제든지 [PM](https://github.com/Roharui)에게 연락주세요!**

## 처음으로 해야할일

1. [디코 서버](https://discord.gg/J6EzpzFMcM)에 가입합니다. (저희 팀은 디코로 소통 및 회의를 진행합니다)
    - `PM`과의 면접 후 합격시 다음 절차를 보냅니다.
2. `#자기소개` 채널에서 자신의 자기소개를 올려주세요.
3. `구글 이메일`과 `Github`아이디를 PM(`Roharui`)에게로 보내주세요.
4. `Github Organization`의 초대를 수락합니다. (이메일로 초대 메세지가 전달됩니다.)
4. 담당하는 분야의 `repo`를 PM에게 말하고 초대를 받으세요.
5. 이 `repo`를 정독하고 모르거나 헷갈리는 부분이 있으면 다른 팀원에게 물어봅니다.
    - 되도록이면 PM에게 물어보세요! ~~PM이 현재 백수라 시간이 널널합니다~~

## 개발 규칙

> 보다 자유로운 개발을 위한 최소한의 규칙입니다. 말그대로 최소한의 규칙이므로 보다 융통성있고 유연한 방식이 있으면 그 방식을 채용하도록 합시다. 규칙의 개선점이 있다고 생각하는 경우 언제든지 말씀해주세요.

1. 개발에 관련된 모든 사항은 repo의 `issue`탭에 정리합니다.
    1. 개발에 관련된 기능이면 앞에 기한을 적습니다. ex) [08.01~08.24] A기능 개발
2. 모든 프로젝트는 `github project`로 개발 일정을 관리합니다.
    1. 개발 목록: 자신이 담당하고 싶은 기능이 있다면 여기서 자신이 개발하겠다고 선택합시다.
    2. 개발 중: 개발중 문제가 생긴다면 `issue`에 코멘트를 남기고 다음 회의에 그 문제에 대해 토의합시다.
    3. 개발 완료: 버그가 있는지 없는지 검사하여 버그가 있다면 `issue`에 코멘트를 남깁시다. (버그는 어쩔수 없이 생기기 마련입니다! 망설임없이 `issue`에 등록합시다.)
    4. 디버그 중: 개발완료 탭에서 찾아낸 버그를 고칩니다.
    5. 디버그 완료: 기능이 완성되었습니다! `issue`를 닫습니다.
3. 일주일에 1번은 회의를 합니다. 회의하는 날은 일정을 비워둡시다.
    1. **1시간 이상 회의를 하지 않습니다.**
    2. 회의에서는 지난 일주일동안 개발된 프로젝트의 문제점에 대해 생각해봅시다.
    3. 한가지 문제에 너무 오랫동안 파고들지 말도록 합시다.
    4. 회의내용은 앞서 말했듯 `issue`에서 정리하도록 합시다.
4. 모든 `repo`에는 `gitflow`를 사용합니다. 하지만 융통성 있게, 유연하게 사용합시다.
    1. 기본적으로 `master`, `develop`, `production` 브랜치를 사용합니다. 상세한 내용은 아래 [gitflow](#gitflow)를 참고합시다.
    2. 한 사이클 마다 버전이 올라가며 상세한 버전관리 내용은 아래 [버전관리](#버전-관리)를 참고합니다.
5. [커밋 메세지](#커밋-메세지)는 아래 형식을 지켜주세요!
6. `테스트 코드`를 저는 **굉장히** 좋아합니다만, 테스트 코드를 짜느라 일정을 놓치는 경우는 없도록 합시다.
7. `코드 리뷰`는 중간중간 시간이 남는 팀원에게 부탁하도록 합시다.
    1. `코드 리뷰`가 필요없을 정도로 가벼운 기능이라면 생략하셔도 상관없습니다.
8. 좋은 `아이디어`가 있으면 바로바로 공유합시다!
9. 서로 돕고 배우며 재밌게 개발합시다!

## gitflow

> 유연성과 융통성을 위해서 별다른 제한을 두지 않았습니다. 하지만 되도록 규칙을 따르도록 합시다.

1. `master` 브랜치는 버전 관리를 위한 브랜치입니다. 일주일마다 `tag`를 달아 버전을 표시합니다.
    1. 실수로 `master` 브랜치에 `feature` 브랜치를 merge 하지 않도록 합시다.
2. `develop` 브랜치는 개발용 브랜치 입니다. 
    1. 자동배포 시스템이 적용되어 있으니 개발완료후 디버그하는데 이용하도록 합시다.
    2. 만일 자동 배포가 되지 않는다면 `PM`에게 연락 바랍니다.
3. `production` 브랜치는 `배포용` 브랜치입니다! 조심해서 `pull request`를 합시다!

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
- `footer`: 그냥 아무거나 적으셔도 됩니다.

```
예시 )
feat: 스크린샷 업로드 기능 개발 완료

스크린샷 업로드 API json 형식으로 변경
사진 데이터를 RAW 데이터로 변경후 전달함

근데 form 안쓰고 보내도 되는거 맞아요?
```


## 버전 관리

1. 일주일에 한번씩 개발된 사항을 `master`브랜치에 옮기고 X.Y.Z에서 Z의 버전을 1 올립니다.
2. Goal에 도착할때 마다 X.Y.Z에서 Y의 버전을 1 올리고 Z의 버전을 0으로 맞춥니다.
3. 최종적인 목표에 도달했을때 X.Y.Z에서 X의 버전을 1 올리고 Y, Z의 버전을 0으로 맞춥니다.
