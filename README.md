# 통신

블루투스(bluetooth)는 근거리 무선통신 규격의 하나로, 2.45GHz주파수를 이용하여 반경 10~100m 범위 안에서 각종 전자, 정보통신 기기를 무선으로 연결, 제어하는 기술규격을 말한다.

ISM(Industrial Scientific and Medical)대역인 2400 ~ 2483.5MHz를 사용한다.다른 시스템과의 간섭을 막기위해 하위영역(2400MHz ~ 2402MHz) 및 상위 영역(2481MHz ~ 2483.5MHz)은 제거하고 2402MHz에서 2480MHz까지 총 79개의 채널을 사용한다.

여러 시스템들과 같은 주파수 대역을 이용하기 때문에 시스템간 전파 간섭이 생길 우려가 있는데, 이를 예방하기 위해 블루투스는 주파수 호핑(Frequency Hopping)방식을 취한다. 주파수 호핑이란 많은 수의 채널을 특정 패턴에 따라 빠르게 이동하며 패킷(데이터)를 조금씩 전송하는 기법이다. 블루투스는 할당된 79개의 채널을 1초당 1600번 호핑한다.

이 호핑 패턴이 블루투스 기기 간에 동기화되어야 통신이 이루어진다. 블루투스는 SPI, I2C 통신과 마찬가지로 기기 간 마스터(Master)와 슬레이브(Slave)구성으로 연결되는데, 마스터 기기가 생성하는 주파수 호핑에 슬레이브 기기를 동기화시키지 못하면 두 기기 간 통신이 이루어지지 않는다. 이를 통해서 다른 시스템의 전파간섭을 피해 안정적 연결을 할 수 있다.

참고로 하나의 마스터에 최대 7개의 슬레이브기기를 연결할 수 있으면 마스터와 슬레이브 간의 통신만 가능할 뿐만 아니라 슬레이브 기기 간의 통신은 불가능하다. 그러나 마스터와 슬레이브의 역할은 고정된 것이 아니므로 상황에 따라 서로 역할을 바꿀 수 있다.

<img src="https://user-images.githubusercontent.com/71697729/108474180-5d5ce600-72d2-11eb-9500-576940cc8d6b.png" width="200" height="200"><img src="https://user-images.githubusercontent.com/71697729/108474100-3f8f8100-72d2-11eb-8c0c-f7069251b2fd.png" width="200" height="200">

※참고※
하나의 공동 마스터로 최대7개의 슬레이브가 연결되어 하나의 피코넷을 형성한다. 
피코넷상의 모든장치들은 마스터의 주파수 호핑 순번과 시간에 동기화된다.
하나의 장치가 두 개이상의 피코넷에 참여되어 있는 상태를 스캐터넷이라고한다.


## 비트레이트(Bit Rate) & 보드레이트(Baud rate)
1. 비트레이트(Bit Rate)
비트 레이트(Bit Rate)는 초당 얼마나 많은 데이터 비트(1 or 0)를 전송할 수 있는가를 나타내느 말이다.
bps(Bit Per Second)는 초당 보낼 수 있는 비트의 수를 나타낸다.

2. 보드레이트(Baud rate)
보레이트는 초당 얼마나 많은 심볼(Symbol, 의미있는 데이터의 묶음)을 전송할 수 있는 지를 나타낸 말이다.

시리얼 통신에서는 Data bit가 8-bit를 사용하므로 이를 하나의 심볼이라고 이야기 할 수 있다.


<img src="https://user-images.githubusercontent.com/71697729/108465441-5ed3e180-72c5-11eb-9d13-1ae0715881b8.png" width="700" height="300">

