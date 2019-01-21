1장 오픈나무 시작
====

## I. 오픈나무 다운로드
[릴리즈](https://github.com/2du/openNAMU/releases)에서 오픈나무의 릴리즈 판을 다운로드 받고, 압축을 해제합니다.  
릴리즈 판은 stable 브랜치에도 업로드되어 리눅스 환경에서 wget을 사용하거나, 레포지토리를 클론하여 릴리즈를 적용하는 것도 가능합니다.

wget (wget 설치 필요)
```
wget https://github.com/2du/openNAMU/archive/stable.zip
```

클론 (Git 설치 필요)
```
git clone -b stable https://github.com/2du/openNAMU.git
```

## II. 모듈 설치
터미널 또는 명령 프롬프트를 열고 다음 명령어로 오픈나무 구성 파일이 위치한 디렉토리로 이동합니다.
```
cd [path]

* [path]는 오픈나무가 위치한 폴더 경로를 의미합니다.
```


다음 명령어로 오픈나무 실행에 필요한 모듈을 설치합니다.
```
pip install -r requirements.txt
```
리눅스 환경의 경우 다음 명령으로 실행해야 합니다.
```
pip3 install -r requirements.txt
```
## III. 애플리케이션 시작
오픈나무를 시작합니다.
```
python app.py
```
리눅스 환경의 경우 다음 명령으로 실행해야 합니다.
```
python3 app.py
```

 * 오픈나무의 첫 계정은 소유자 계정으로 설정됩니다.

## IV. 애플리케이션 공개
현재 오픈나무에서 권장하는 애플리케이션 공개 방법은 아파치나 nginx와 같은 웹 서버 구동 소프트웨어를 통해 리버스 프록시를 설정하는 것입니다.

 * [apache 설정 파일 예시](/conf_example/apache/)
 * [nginx 설정 파일 예시](/conf_example/nginx.conf)

만약 HTTPS 리버스 프록시를 설정하는 경우, 보안을 위해 오픈나무 설정에서 호스트를 `127.0.0.1` 또는 `localhost`로 변경할 것을 권장합니다.
