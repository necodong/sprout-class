# Django 개발 환경 세팅하기

## 공통으로 vscode 설치하기

Visual Studio Code (vscode)는 Microsoft에서 개발한 무료 오픈소스 에디터로 요즘 개발자들이 가장 많이 사용하는 애디터 중 하나입니다.
이번 과정에서도 vscode를 사용하게 됩니다.

https://code.visualstudio.com/Download 에서 실행 파일을 다운로드하여 설치하면 됩니다.
vscode 를 열고 좌측 Extension에서 python을 검색하여 설치합니다.

## 커맨드라인 시작하기

https://tutorial.djangogirls.org/ko/intro_to_command_line/

이미 vscode을 설치했으므로 vscode을 열어서 터미널을 사용할 수 있음

상단 메뉴 바 터미널 -> 새 터미널을 통해 터미널을 열 수 있음

터미널을 열었으면 본격적으로 파이썬을 설치해본다

터미널을 시작하기 전에 알아둬야 할 것이 몇 가지 있음

1. 프롬프트 

명령 프롬프트라면 C:\(사용자 이름)>

맥이라면 ~ 으로 시작하면서 커서가 깜빡거리고 있음
이것을 프롬프트라고 하며 이 상태에서 원하는 명령어를 입력하면 됩니다.

2. 터미널은 탐색기 or finder의 역할을 함

윈도우애서 파일을 열거나 관리하기 위헤셔 탐색기라는 프로그램을 이용하게 되는데 터미널은 이 탐색기의 역할을 하게 됨

윈도우에서는 cd 맥에서는 pwd 임

https://tutorial.djangogirls.org/ko/intro_to_command_line/

을 한 번 따라해본다


## 파이썬 설치하기

본 강의에서는 파이썬 3.8을 사용하게 됩니다.

## Django 개발 환경 세팅하기 (Mac)

Mac에는 이미 파이썬이 설치되어 있지만 맥북의 종류에 따라 파이썬 버전이 다릅니다. 따라서 python 3.8 버전 따로 설치해줘야 합니다. 먼저 homebrew가 설치되어 있지 않다면 터미널에 아래 명령어를 입력하여 설치합니다.

```sh
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

다음 brew install python@3.8 을 해서 파이썬 3.11을 설치합니다.

```sh
$ brew install python@3.8
```

파이썬을 설치했다면 파이썬 가상환경을 만들어줍니다.
(가상환경에 대한 설명 필요)

```sh
$ python3.8 -m venv myvenv
```

보통 터미널에서는 아무것도 안 뜨면 잘 되었다는 뜻입니다. venv는 파이썬3부터 추가된 virtualenv 를 설치하지 않아도 가상환경을 만들어주는 도구입니다.

이제 가상환경을 활성화합니다.

```sh
$ source myvenv/bin/activate
```

프롬프트 왼쪽에 (myvenv) 라고 뜨면 성공입니다. 이제 django를 설치합니다.

```sh
(myvenv) $ pip install django
```

django를 설치했다면 아래 명령어를 입력하면 requirements.txt 라는 파일이 생기는데요.
나중에 `pip install -r requirements.txt` 명령어를 통해 새로운 컴퓨터에서도 django를 설치할 수 있습니다.

이제 django의 버전을 확인할 수 있습니다. 4.1.7 이면 됩니다.
이제 django를 설치했으니 첫 장고 프로젝트를 만들 시간입니다. 
necodong 폴더가 만들어지면 성공입니다.

```sh
$ python -m django --version
4.1.7
$ django-admin startproject necodong
```
