# 개발 환경 세팅

> `개발중입니다` 팀의 공식 IDE는 `VSCode`입니다만 강제하지는 않습니다. 
> 만약 다른 IDE를 사용하고 싶다면 이 문서에 개발환경 구축 문서를 작성하시길 바랍니다.

# VSCode

> 언어에 따라 환경 세팅을 구축해주세요.

## Javascript

> 후일 작성 바람.

1. `ESLint`와 `Preitter`를 사용합니다. [참고 문서](https://veggie-garden.tistory.com/13)

## Java

> 미완성된 문서입니다. 후일 추가 바랍니다.

> 자바 11 이상을 설치했다 가정하고 진행합니다.

1. `Extension Pack for Java`을 설치합니다.
  - [링크](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)
2. `Spring Boot Extension Pack`을 설치합니다.
  - [링크](https://marketplace.visualstudio.com/items?itemName=Pivotal.vscode-boot-dev-pack)
3. 기타 확장을 설치합니다.
  - [Lombok Annotations Support for VS Code](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-lombok)
4. `Formatter` 설정을 합니다.
  - [google-java-formatter](https://github.com/google/google-java-format/releases/download/v1.15.0/google-java-format-1.15.0-all-deps.jar)를 설치합니다. (되도록이면 C드라이브와 가까운 곳에 파일을 둡시다.)
  - [Google-Java-Format](https://marketplace.visualstudio.com/items?itemName=mngrm3a.vscode-google-java-formatter) 확장을 설치합니다.
  - `google-java-formatter`를 설치한 경로를 복사합니다.
  - `Ctrl+,`을 눌러 설정을 열고 `grf`를 입력합니다.
  - 나타나는 입력창에 경로를 입력합니다.
  - 아무 `.java` 파일을 엽니다.
  - `.java` 파일의 문법을 엉망으로 만든 뒤 `Ctrl+P`를 눌러 명령 팔레트를 연 뒤 `Format Document`을 선택합니다.
  - 알림창이 뜹니다. `구성` 버튼을 누른뒤 `Google Java Format`을 선택합니다.
  - 파일의 문법이 정상으로 돌아온 것을 확인합니다.

## Python

> 미완성된 문서입니다. 후일 추가 바랍니다.

> 파이썬은 기본적으로 3.9를 사용합니다. `requirements.txt`를 주기적으로 갱신합시다. (최신버전의 `Linter`와 `formatter`를 이용합시다.)

> Conda를 설치했다 가정하고 진행합니다.

1. [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) 확장을 설치합니다.
2. `conda create -n <프로젝트명> python=3.9`를 터미널에 입력합니다.
3. 가상환경 설치가 완료됬다면. 다음 [파일](env\requirements.txt)을 다운로드 합니다.
4. `Ctrl+P`를 눌러 명령 팔레트를 연 뒤 `Python: Select Interpreter`를 선택합니다.
5. `3.9.12 <프로젝트명>`으로 되어있는 파이썬 인터프리터를 선택합니다.
6. 터미널을 열고 다음 명령어를 입력합니다. `pip install -r requirements.txt`
7. `Ctrl+P`를 눌러 명령 팔레트를 연 뒤 `Python: Select Linter`를 선택합니다.
8. `flake8`과 `mypy`를 입력합니다. (7~8 과정을 한번 더 합시다.)
9. `Ctrl+,`을 눌러 설정을 열고 `python.formatting.provider`를 입력한뒤 `black`을 선택합니다.
10. 아무 `.py` 파일의 문법을 엉망으로 만든 뒤 `Ctrl+P`를 눌러 명령 팔레트를 연 뒤 `Format Document`을 선택합니다.
11. `Python`을 선택하고 문법이 정상으로 돌아온것을 확인합니다.