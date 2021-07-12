# Cardnews-Project
캡스톤디자인. 졸업 작품

<br>

## 0.
* 기술 스택<br>
![image](https://user-images.githubusercontent.com/60432062/125259974-d1a82c80-e33a-11eb-963e-0b97f3df263e.png)
*	프로젝트 기간 : 2020.09-2021.05
*	프로젝트 참여 인원 : 4인
*	프로젝트 내용
1.	사이트별 뉴스 데이터 크롤링
2.	자연어처리 및 Text Rank알고리즘을 이용한 요약문 추출 후 카드뉴스 형태로 제공
3.	코사인 유사도를 이용한 컨텐츠 기반 뉴스 추천 기능

* 개인 수행 내역 - 안드로이드 전반
1.	flask 웹에서 JSON 형태로 DB데이터 출력
2.	안드로이드 내 SQLite 이용하여 DB생성 및 받아온 정보 저장, 활용
3.	로딩, 로그인, 회원가입, 뉴스 열람 등 안드로이드에서 웹서버로의 각종 요청 처리
4.	로그인 후 저장 유지 정보 관리
5.	각 페이지 디자인 및 Activity 구현

<br>

## 1.
* 로딩화면
<img width="30%" alt="로딩" src="https://user-images.githubusercontent.com/60432062/120330347-adaeff80-c327-11eb-8c7a-0ebea8b836c1.png">
로딩화면이 뜨는동안 MySQL 데이터베이스에 새로 업데이트된 뉴스들을 불러와 SQLite에 저장한다.
<br>
<br>

* 메인화면
<img width="30%" alt="메인2" src="https://user-images.githubusercontent.com/60432062/120324743-ecda5200-c321-11eb-8bd1-b0edcc6f5a69.png">
현재 로그인한 사용자가 가장 최근에 관심있게 읽은 뉴스의 제목을 띄워준다. 또한 맞춤 추천 뉴스들을 제공한다.<br> 
최근 관심있게 읽은 3가지의 기사들을 기반으로 총 15개의 뉴스가 추천되며, 뉴스 목록은 스크롤뷰로 구성된다.<br> 
뉴스를 선택하면 바로 카드뉴스 화면으로 넘어가서 읽을 수 있도록 하였다.
<br> 
<br>

* 카테고리 바
<img width="30%" alt="카테고리바2" src="https://user-images.githubusercontent.com/60432062/120326922-2e6bfc80-c324-11eb-9ea6-901f6e82882c.png">
사용자 맞춤 추천 뉴스 이외의 뉴스들을 보고싶을 때 탭을 터치하여 카테고리 바를 열 수 있다.<br> 
가장 하단에는 로그아웃 버튼을 두어 다른 사용자 계정으로도 회원가입/로그인할 수 있도록 했다.
<br> 
<br>

* 카테고리 목록 화면(사회 카테고리 선택 모습)
<img width="30%" alt="카테고리2" src="https://user-images.githubusercontent.com/60432062/120328050-66277400-c325-11eb-8886-5c7210ef3a01.png">
정치/경제/사회/생활•문화/세계/IT•과학 중 카테고리 바에서 선택한 카테고리의 다양한 뉴스들을 확인할 수 있는 목록 화면이다.<br> 
스크롤뷰로 뉴스 목록을 훑어볼 수 있으며, 뉴스를 선택하면 카드뉴스를 읽을 수 있다.
<br> 
<br>

* 카드뉴스 화면
<img width="30%" alt="카드뉴스2" src="https://user-images.githubusercontent.com/60432062/120328128-7e978e80-c325-11eb-848f-282bd1e3b6b7.png">
해당 뉴스에서 가져온 이미지를 배경에 삽입하고 그 위에 텍스트를 배치했다. <br> 
일반 인터넷 뉴스에서 핵심 문장만을 요약•추출하여 총 7장의 카드뉴스로 구성한다. <br> 
카드 한 장에는 대개 1~2문장이 들어간다. 카드 7장은 좌우로 스와이프가 가능하기 때문에 가벼운 손동작만으로 넘겨가며 읽을 수 있다. <br> 
뉴스를 선택하여 카드뉴스 화면으로 넘어온 순간부터 시간을 측정하여 카드뉴스 화면에 20초 이상 머물렀다면, 관심있게 읽은 기사로 판정하고 관심 기사목록을 업데이트한다.
<br> 
<br>

* 로그인 화면
<img width="30%" alt="로그인2" src="https://user-images.githubusercontent.com/60432062/120328215-93742200-c325-11eb-9687-2050b8740f31.png">
앱을 처음 설치한 경우에, 앱 로딩화면이 끝난 직후 로그인 화면으로 넘어오도록 설정하였다. <br> 
카테고리바에서 로그아웃 버튼을 누른 경우에도 로그인 화면이 나타난다. 한번 로그인하면 앱 내에 로그인 정보를 저장하여, 앱을 껐다가 켰을때 다시 로그인 할 필요가 없도록 하였다. <br> 
잘못 된 로그인 정보를 입력했을 때는 로그인 오류 메시지를 띄운다. 회원가입을 원할 경우 회원가입 화면으로 이동할 수 있도록 버튼을 두었다.
 <br> 
 <br>
 
* 회원가입 시 뉴스선택 화면
<img width="30%" alt="뉴스 선택2" src="https://user-images.githubusercontent.com/60432062/120328288-a555c500-c325-11eb-8ecd-dd4a0f06af9c.png">
로그인 화면에서 회원가입 버튼을 누르면 이동하는 화면으로, DB에 존재하는 뉴스들 중에 중복을 제거하여 랜덤 10개 기사를 골라 화면에 띄워서 관심뉴스를 선택하도록 한다. <br> 
10개의 뉴스는 스크롤하여 모두 확인할 수있다. <br> 
회원가입이 완료됐을 때 선택된 3개의 뉴스 하나 당 5개씩, 도합 15개의 추천뉴스를 메인화면에서 보여줄 수 있게 된다.
<br> 
<br>

* 회원가입 화면
<img width="30%" alt="회원가입2" src="https://user-images.githubusercontent.com/60432062/120328378-b9012b80-c325-11eb-827e-7a6011cac3a8.png">
관심뉴스를 고르고 나면 넘어오는 화면이다. 회원가입 아이디와 비밀번호를 입력할 수 있다. <br> 
이미 존재하는 아이디로 중복 가입을 할 경우엔 오류 메시지를 띄워 가입을 반려시킨다. <br> 
회원가입 버튼을 누르고 회원가입이 완료되면, 다시 로그인 화면으로 돌아가 로그인을 할 수 있다.
