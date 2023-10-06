# 딸기 케이크 침대(Strawberry Cake Bed)
- 딸아이가 스케치한 그림을 바탕으로 레고 작품을 만들었습니다.

## 작품 설명 페이지
- https://blog.naver.com/pcmola/222588494320

## 이미지
![20211114＿135403](https://github.com/pcmola/strawberry-cake-bed/assets/20479087/2f23e4d9-39f3-484c-82e9-ce9444ca1675)
 
## 동영상
- [YouTube - [레고 창작] 딸기 케이크 침대](https://youtu.be/0Gr8m8-oP4c)

## 소스 설명
- 이미지 12개를 순환하면서 보여줍니다.  

📦auto_view  
 ┣ 📂img  
 ┃ ┣ 📜img_1.jpg  
 ┃ ┣ 📜img_10.jpg  
 ┃ ┣ 📜img_11.jpg  
 ┃ ┣ 📜img_12.jpg  
 ┃ ┣ 📜img_2.jpg  
 ┃ ┣ 📜img_3.jpg  
 ┃ ┣ 📜img_4.jpg  
 ┃ ┣ 📜img_5.jpg  
 ┃ ┣ 📜img_6.jpg  
 ┃ ┣ 📜img_7.jpg  
 ┃ ┣ 📜img_8.jpg  
 ┃ ┗ 📜img_9.jpg  
 ┗ 📜view.html  


## 실행 방법
- 라즈베리파이 4에서 테스트했습니다.
   
### 1. HTML/IMG 소스 내려받기  
- /home/pi/Downloads/ 아래에 내려받는다고 가정합니다.

### 2. 크로미움을 최신 버전으로 업데이트  
- 이렇게 하지 않으면, 크로미움 실행 시 'Chromium이 이전 버전임'이라고 경고가 뜹니다.
```
$ sudo apt update
$ sudo apt full-upgrade
```

### 3. 부팅 시 크로미움 자동 실행하면서 전체화면으로 열기
- 라즈베리파이 부팅 후 바로 실행할 수 있도록 다음과 같이 합니다.

3.1. 크로미움 전체화면으로 띄우는 Shell Script 작성
```
pi@raspberrypi:~ $ cat start_view.sh 
chromium-browser /home/pi/Downloads/view.html --args --start-fullscreen
```  

3.2. 부팅 시 Shell 자동 실행  
```
cat /etc/xdg/lxsession/LXDE-pi/autostart
...
lxterminal -e /home/pi/start_view.sh
```

