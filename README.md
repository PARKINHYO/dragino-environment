드라지노 환경구축하기
=====================


THE THINGS NETWORK 회원가입 후 Gateway 등록 (console.thethingsnetwork.org)
-----------------------------------------------------------------------------------

* Gateway EUI : I'm using the legacy packet forwarder 체크 후 LG-01 gateway 뒤편의 EUI 번호 기입 + 끝에는 숫자 4자리 추가 기입(ex: 1111, 1112)
* Frequency Plan: Europe 868MHz
* Router: ttn-route-eu
* Antenna Placement: indoor
* (ttn 사이트 사진 넣기)

LG01-N Gateway 설정
-------------------------------------------------------------

* 공유기의 랜선을 드라지노 WAN 포트에 연결
* dragino wifi 연결 후 10.130.1.1 접속(사이트 아이디와 비번: root, dragino)

### 사이드바 Sensor -> LoRa/LoRaWan 클릭
* Server Address: router.eu.thethings.network
* Gateway ID: the things network에 등록한 게이트웨이 EUI 기입
* TX Frequency: 868100000
* RX Frequency: 868100000
* Spreading Factor: SF7
* Transmit Spreading Factor: SF9
* 나머지는 default 값
* Save & Apply 버튼으로 저장

### 사이드바의 Sensor -> Flash MCU 클릭
* [사이트](http://www.dragino.com/downloads/index.php?dir=LoRa_Gateway/LG01-P_LG01-S/Arduino%20Sketch/)에서 Single_pkt_fwd_v004.ino.hex 우클릭 후 다른이름으로 링크 저장(파일 형식: *.hex)
* 저장한 파일을 파일 선택 -> 해당파일을 upload <br>
* 사이드바 Sensor -> MicroController MCU Version이 맞는지 확인 후 우측하단에 Save & Apply 클릭

THE THINGS NETWORK Application(Device)등록
--------------------------------------------------------------

ADD APPLICATION
* Application ID: 임의의 아이디 설정
* Handler registration: ttn-handler-eu
* 우측 하단의 Add application로 어플리케이션 등록

REGISTER DEVICE
* DEVICES -> register device 클릭
* Device ID: 임의의 아이디 설정
* Device EUI: 좌측의 버튼을 눌러 this field will be generated로 변경
* App key: this field will be generated
* 우측 하단의 Register 클릭
* 우측 상단의 Settings 클릭 후 Activation Method를 ABP모드로 변경


Arduino IDE
--------------------------
* Application_ex1 폴더 코드


























[여기](http://www.dragino.com/downloads/index.php?dir=LoRa_Gateway/LG01-P_LG01-S/Arduino%20Sketch/)

[코드](승훈이 카톡보냄)