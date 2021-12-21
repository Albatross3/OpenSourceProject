# Term Project: 편하게 외출하자!
이 프로그램은 외출할 때 바깥 상황에 대한 데이터를 종합 및 판단해서 개별 카카오톡 메세지로 보고를 해주는 프로그램입니다.

<img src = "https://user-images.githubusercontent.com/43260658/146926939-b093ca62-ec64-4eab-9928-30ccae48743e.png" width="30%" height="30%">

## 🔥 만들게 된 동기
평소에 외출하기 전 날씨를 습관적으로 검색했었는데 매일 검색하기보다 자동적으로 프로그램만 실행하면 카톡으로 원하는 데이터를 받아보면 좋을 것 같아서 만들게 되었습니다.

## 사용 조건
* 실행 전 환경 설정
  1. Python Selenium 설치
  1. Chrome Driver 설치
  1. Driver 위치 설정
* 소스 코드 내에 개인 **카카오톡 ID**, **Password** 입력 
* 카카오톡 인증 2단계 x

위 조건 3가지를 만족해야 개인 카카오톡으로 메시지를 보고받을 수 있습니다

## 사용 조건_상세 설명
* 실행 전 환경 설정

<img src="https://user-images.githubusercontent.com/43260658/146931709-c12126ca-5952-41b3-99c2-165484d02d3b.png" width="20%" height="30%">

위와 같이 spyder console 창에 pip install selenium을 입력해서 selenium을 설치해줍니다.

다음으로 [크롬 드라이버](https://chromedriver.chromium.org/downloads) (https://chromedriver.chromium.org/downloads)로 들어가서 현재 자신이 사용하는 
크롬 버전과 맞는 것을 설치합니다.

<img src="https://user-images.githubusercontent.com/43260658/146932996-35348453-f5bb-4de3-ab76-bf263ba976b5.png" width="40%" height="40%">

※크롬 버전은 위와 같이 확인할 수 있습니다※

마지막으로 chromedriver.exe 파일을 현재 .py 파일이 있는 위치에 저장합니다.

<img src="https://user-images.githubusercontent.com/43260658/146934033-38219a34-3941-4158-9059-8dfbbe51c870.png" width="40%" height="40%"> 

* 소스 코드 내에 개인 **카카오톡 ID**, **Password** 입력 
~~~
#카카오 계정 로그인(단, 로그인 하는 계정이 2단계 인증을 하지 않아야 한다)
driver.find_element_by_xpath('//*[@id="id_email_2"]').send_keys("")
driver.find_element_by_xpath('//*[@id="id_password_3"]').send_keys("")
~~~
위 코드에서 첫 번째 send_keys("") 안에는 카카오톡 로그인 할 때의 이메일 계정을 두 번째 send_keys("") 안에는 비밀번호를 입력한다.

* 카카오톡 인증 2단계 x

카카오톡내에서 인증 2단계가 되어있다면 해제하고 사용해주시면 됩니다. 
2단계 인증은 카카오톡 -> 설정 -> 개인/보안 -> 카카오 계정에 들어가면 2단계 인증을 했는지 안 했는지 파악 가능합니다.
