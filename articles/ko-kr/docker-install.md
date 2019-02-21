1장 -1 오픈나무 도커 시작
====

## I. 오픈나무 도커 다운로드
docker pull 명령어로 도커 허브에 업로드 된 오픈나무 도커를 가져옵니다.

안정화 릴리즈
```
docker pull opennamu/stable
```

개발중
```
docker pull opennamu/opennamu
```

## II. 도커 시작
docker run 명령어로 불러온 도커를 실행합니다.

```
docker run -p <port>:3000 -v <data>:/app/data --name <container> opennamu/<repository>

<port>          도커 호스트에서 오픈할 포트
<data>          도커 호스트와 오픈나무가 연결될 데이터 저장소
<container>     도커 컨트롤을 위한 컨테이너 이름
<repository>    docker pull로 가져온 도커 저장소 이름
* 스킨을 추가하고 싶다면 -v <skin>:/app/views를 -v <data>:/app/data 뒤에 추가하세요.
```

 * 도커는 호스트와 공유하는 도커 내 디렉토리를 최초 1회 초기화합니다. 도커 실행후 오류가 발생하면, 그것은 데이터파일 손실일 가능성이 높습니다.
 * 데이터파일은 [깃허브 오픈나무 저장소 stable 브랜치](https://github.com/2du/openNAMU/tree/stable)에서 가져올 수 있습니다.

권장하는 도커 실행 명령은 다음과 같습니다:
```
cd <path>
git clone -b stable https://github.com/2du/openNAMU.git
cp opennamu/data data
cp opennamu/views skin
docker pull opennamu/stable
docker run -p 3000:3000 -v data:/app/data -v skin:/app/views --name opennamu opennamu/stable

<path>는 호스트가 오픈나무를 저장할 디렉토리 경로를 의미합니다.
```