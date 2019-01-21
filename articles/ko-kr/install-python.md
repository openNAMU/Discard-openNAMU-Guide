0장 파이썬 설치
====

## I. 파이썬 설치
파이썬을 시작하려면 기기에 파이썬 개발환경이 설치되어 있어야합니다. 파이썬 개발환경을 설치해봅시다.

### Windows/Mac 환경
![](/assets/0/1.png)  

[파이썬 공식 홈페이지](https://python.org)에서 파이썬을 다운로드받습니다.

![](/assets/0/2.png)  

```Add Python 3.7 to PATH```에 체크하고 Install Now를 눌러 파이썬을 설치합니다. ```Add Python 3.7 to PATH```를 체크하지 않고 파이썬을 설치했다면 [여기](#앗-add-python-37-to-path에-체크하지-않고-설치를-눌러버렸어요)를 참고하세요.  

 * ```Add Python 3.7 to PATH```에 체크해야하는 이유:  
오픈나무 설치 가이드는 _명령 프롬프트_ 라는 프로그램을 통해 오픈나무를 실행하도록 안내하고 있습니다.  
그러나 명령 프롬프트에서 파이썬을 손쉽게 사용하려면 몇가지 복잡한 설정이 필요하고, 그 설정을 프로그램이 쉽게 해주는 것이 이 메뉴입니다.  
![](/assets/0/10.png)  
만약 이 설정이 제대로 이루어지지 않았다면 이후에 파이썬을 실행하면 이런 문구가 나타날 것입니다.

```
 * 덧붙임
파이썬은 나날이 발전하는 언어입니다. 이 가이드 작성일 기준 최신 버전은 3.7이지만
이후엔 3.7.4, 3.8 등 더 높은 버전이 나올지도 모르는 법이죠. 토씨 하나 가이드와
다르다고 모든게 달라지는 것은 아닙니다.
```

![](/assets/0/3.png)  

파이썬 설치가 완료되었습니다. 명령 프롬포트나 터미널을 열어서 파이썬을 실행할 차례입니다.  

![](/assets/0/4.png)  

Windows 환경에서 <img src="/assets/common/windows.svg" width="10px" height="10px"> + R 을 눌러 실행창을 엽니다.  

![](/assets/0/5.png)  

실행창에 ```cmd```를 입력하여 명령 프롬프트를 실행합니다.  

![](/assets/0/6.png)  

명령 프롬프트에서 ```python```을 입력하여 파이썬을 실행합니다.  

![](/assets/0/18.png)  

```
Python 3.7.0 (v3.7.0:1bf9cc5093, Jun 27 2018, 04:06:47) [MSC v.1914 32 bit (Intel)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
이런 형식의 문자열이 나타나면 설치가 완료된 것입니다.

```
 * 덧붙임
기본적으로 이 검은창에 무언가를 입력해서 작업해야 한다면, 모두 입력한 뒤
Enter키를 눌러야 컴퓨터는 명령받은 작업을 실행합니다.  
```

### 앗 Add Python 3.7 to PATH에 체크하지 않고 설치를 눌러버렸어요.

![](/assets/0/11.png)  

컴퓨터를 우클릭하여 속성을 엽니다.

![](/assets/0/12.png)  

또는 제어판의 시스템을 통해서도 열 수 있습니다.

![](/assets/0/13.png)  

좌측 탭의 ```고급 시스템 설정```을 클릭하여 엽니다.

![](/assets/0/14.png)

이어서 열리는 ```시스템 속성```에서 ```환경 변수```를 클릭하여 엽니다.

![](/assets/0/15.png)  

```환경 변수``` 에서 ```Path``` 값을 수정합니다. ```Path```를 선택하고 편집을 누릅니다.

![](/assets/0/16.png)  

새로 만들기를 눌러 아래 두 줄을 각각 추가하고 저장합니다.
```
%userprofile%\AppData\Local\Programs\Python\Python37-32
%userprofile%\AppData\Local\Programs\Python\Python37-32\Scripts
```

![](/assets/0/17.png)  

_Python37-32_ 는 파이썬 버전에 따라 경로가 달라질 수 있습니다. <img src="/assets/common/windows.svg" width="10px" height="10px"> + R 을 눌러 실행창을 열고 _%userprofile%\AppData\Local\Programs\Python_ 을 입력하면 _Python37-32_ 대신 어떤 폴더가 있는지 확인할 수 있습니다.

마지막으로, 컴퓨터를 재부팅합니다.

### Linux(Debian 계열) 환경
다음 명령어를 차례로 입력합니다.
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install python3 python3-pip python3-setuptools
```
 * `sudo apt-get upgrade` 작업은 오래 걸릴 수 있습니다.

![](/assets/0/9.png)  

```
 * 덧붙임
리눅스는 윈도우 환경에서와는 달리 파이선 2와 3을 엄격하게 구분해두고 있습니다.
윈도우와 달리 리눅스에서 파이썬은 ```python3```를 통해 실행할 수 있습니다.  
```

```
Python 3.5.2 (default, Nov 23 2017, 16:37:01)
[GCC 5.4.0 20160609] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

이런 형식의 문자열이 나타나면 설치가 완료된 것입니다.