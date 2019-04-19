스킨 패키징
====

**주의!** 실험적 기능

스킨 패키징은 아직 정식 채택된 기능이 아닙니다.  
이 문서는 사양서이며, 차후 지원될 예정입니다. 개발 상태는 [skin_ver](https://github.com/2du/openNAMU/tree/skin_ver) 브랜치에서 확인할 수 있습니다.

개요
----
스킨 패키지의 루트 폴더에 `package.json` 파일을 만들어 스킨 정보를 작성할 수 있습니다.

package.json
```json
{
    "name" : "스킨 이름",
    "support" : {
        "r_ver" : "오픈나무 버전(display)",
        "c_ver" : "오픈나무 버전(내부)",
        "s_ver" : "오픈나무 버전(내부)"
    },
    "thumbnail" : "스킨 썸네일 경로"
}
```

#### 스킨 이름
스킨 이름을 작성합니다.
   
#### 오픈나무 버전
오픈나무 메인 코드(`app.py`)의 r_ver, c_ver, s_ver 부분을 가져옵니다.

보통 코드 내에서 다음과 같은 형태를 띄고 있습니다. (작성일 기준 11-13번째 줄 코드)

 ```python
r_ver = 'v3.1.0-master-05'
c_ver = '400000'
s_ver = '1'
```

#### 스킨 썸네일 경로
스킨 썸네일 이미지 경로를 작성합니다.

예) 스킨 패키지의 루트 경로에 썸네일 이미지로 `thumb.png`파일이 위치한다면, `"thumbnail" : "thumb.png"`가 될 것입니다.

파일 작성 예시
----
`package.json` 파일의 작성 예시는 아래와 같습니다.
```json
{
    "name" : "neo_yousoro",
    "support" : {
        "r_ver" : "v3.1.0-master-05",
        "c_ver" : "400000",
        "s_ver" : "1"
    },
    "thumbnail" : ""
}
```
