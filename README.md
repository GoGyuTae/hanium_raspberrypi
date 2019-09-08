# Node-RED
**Node-RED**를 사용해 **온습도, 미세먼지, 유해가스검출, GPS 센서 데이터를 수집&전송**한다.
**이동형 장치**에서 값을 확인하기위한 **GUI** 개발


### 실행

Check out http://nodered.org/docs/getting-started/ for full instructions on getting
started.

1. `sudo npm install -g --unsafe-perm node-red`
2. `node-red`
3. Open <http://localhost:1880> or  <http://연결된 _IP:1880>

### 도움받기

More documentation can be found [here](http://nodered.org/docs).

For further help, or general discussion, please use the [Node-RED Forum](https://discourse.nodered.org) or [slack team](https://nodered.org/slack).


---

## 온습도
>**DHT22 Seonsor**를 통해 온도 및 습도를 받아와 표시, GUI 구현

- 각 msg.temperature, msg.humidity에 온습도 리턴
- 초록색 pallette 들은 Debug용

![dht22](/uploads/7fc4393058f14e4f5c434f05b8fa7d63/dht22.PNG)


## 미세먼지
>**PMS7003** 으로 **미세먼지**(PM1.0) 와 **초미세먼지**(PM0.1, 0.5) 측정, GUI구현 

- PMS7003 에는 Python code 사용

![PMS7003](/uploads/253254cdb982d0f8c550a436eb2e65b5/PMS7003.PNG)

## 유해가스 검출
> **MQ-2 Seonsor** 를 이용하여 **RaspberryPi 3B** PIN12 에서 검출유무를 알려준다.


핀은 초기값(정상)이 1이지만 DB 를 통한 관리를 위해 기록되는 값은 아래와같이 변경

- 유해가스 검출시 1
- 유해가스 미검출시 0

![mq2](/uploads/e25d6dae5d91540645d64ec888407184/mq2.PNG)