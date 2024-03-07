---
title: Network 기초
author: Alme
date: 2024-01-08 11:33:00 +0800
categories: [네트워크, 개념]
tags: [네트워크]
pin:  true
math: true
mermaid: true
---

<!-- <img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/91a20d3c0664f3fceb9ba24cce20504cc3b761de/_posts/images/20240114/test.png"> -->

<!-- ![이미지](https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/91a20d3c0664f3fceb9ba24cce20504cc3b761de/_posts/images/20240114/test.png) -->

## <b>네트워크(Network)
<hr>
- 통신 가능한 장비(노드)들이 데이터를 주고 받을 수 있게 연결한 통신망  

<br>

## <b>노드(Node)
<hr>
- IP주소와 MAC주소(2계층 주소 체계)의 조합으로 구성된 NAC(Network Access Control)의 논리적인 연결 단위  
  즉, 노드는 통신(네트워크에 연결) 가능한 장비라고 생각하면 된다  

  <br>

  ​※ NAC(Network Access Control)란?
  - 네트워크에 접속하는 장치가 네트워크에 접근하기 전 보안 정책 준수 여부를 검사하여 네트워크 사용을 제어하는 것

<br>

## <b>네트워크 유형
<hr>
<b>1. LAN(Local Area Network)  
- LAN(근거리 통신망)은 일반적으로 지역화된 영역 내에서 연결된 컴퓨팅 장치 그룹  
<br>

<b>2. WAN(Wide Area Network)  
- WAN(광역 네트워크)은 디바이스가 넓은 지역에서 통신할 수 있도록 장거리에 걸쳐 여러 LAN을 연결하는 네트워크  
( WAN은 여러 개의 상호 연결된 LAN으로 구성 )

<br>

## <b>토폴로지(Topology)
<hr>
컴퓨터 및 기타 네트워크 구성요소의 물리적 연결(배치) 형태

### <b>토폴로지 종류</b>  
<b>1. 버스형</b>  
<img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/main/_posts/images/20240108/Bus Topology.png" width="500" height="500">
  - 하나의 긴 케이블이 네트워크상의 모든 장치를 연결하는 중추 네트워크의 역할을 하는 형태  

    > <b>장점</b>  
    > - 설치가 쉬움  
    > - 비용이 저렴  
    > - 각 호스트의 고장이 네트워크 내의 다른 부분에 영향을 주지 않음  

    > <b>단점</b>
    > - 재구성이나 결합 분리의 어려움  
    > - 탭에서 일어나는 신호의 반사는 신호의 질을 저하시킴  
    > - 기저대역(Baseband) 전송 방식을 사용할 경우 거리에 민감하여 거리가 멀어지면 중계기가 필요함  
    > - 버스 케이블에 결함이 발생하면 전체 스테이션은 모든 전송을 할 수 없음  
    > - 호스트의 수가 증가하면 처리 능력은 급격히 감소함(CSMA/CD)  
    > - 네트워크에 부하가 많으면 응답시간이 늦어짐  
      ​※ Baseband : 기본 신호를 그대로 전송하는 방법, 원거리 전송X  
      ​※ Broadband : 변조해서 전송, 원거리(장거리) 전송O​  

<br>

<b>2. 링형</b>  
<img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/main/_posts/images/20240108/Ring Topology.png" width="500" height="500">
  - 닫​힌 루프 형태로 각 호스트가 자신의 양쪽 호스트와 전용으로 점 대 점으로 연결된 형태  

    > <b>장점</b>
    > - 설치와 재구성이 쉬움
    > - 장애가 발생한 호스트를 쉽게 찾음
    > - 호스트의 수가 늘어나도 네트워크의 성능에는 별로 영향을 미치지 않음
    > - Star형보다 케이블링에 드는 비용이 적음  

    > <b>단점</b>
    > - 링을 제어하기 위한 절차가 복잡하여 기본적인 지연이 존재함
    > - 단방향 전송이기 때문에 링에 결함이 발생하면 전체 네트워크를 사용할 수 없기 때문에 이를 해결하기 위해 이중 링(FDDI:Fiber Distributed Data Interface)을 사용함
    > - 새로 호스트 추가하기 위해서는 물리적으로 링을 절단하고 호스트를 추가해야 함  

<br>

<b>3. 스타형</b>  
<img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/main/_posts/images/20240108/Star Topology.png" width="500" height="500">
  - 중앙집중식 구조를 가짐 ( = 중앙에 위치한 주 노드(허브, 스위치 등)에 연결된 케이블로 다른 노드(컴퓨터)들을 연결 )    

    > <b>장점</b>
    > - 중앙에 위치한 노드(허브, 스위치 등)를 두고 컴퓨터가 별 모양으로 연결되어 있어 설치와 재구성이 쉬움  
    > - 장애 발생 시 발견이 쉬움  
    > - Network 관리가 쉬움  
    > - 하나의 장애가 다른 네트워크 장비에 영향을 주지 않음  

    > <b>단점</b>
    > - 링을 제어하기 위한 절차가 복잡하여 기본적인 지연이 존재함
    > - 단방향 전송이기 때문에 링에 결함이 발생하면 전체 네트워크를 사용할 수 없기 때문에 이를 해결하기 위해 이중 링(FDDI:Fiber Distributed Data Interface)을 사용함
    > - 새로 호스트 추가하기 위해서는 물리적으로 링을 절단하고 호스트를 추가해야 함  

<br>

<b>4. 메쉬형, 트리형 등등</b>

<br>

## <b>IPv4 주소
<hr>
IPv4 주소는 4개의 옥탯(1 옥탯 = 8bit)으로 구성되어 있으며, 5개의 클래스로 구분된다 (A, B, C, D, E)  
IPv4 주소는 네트워크 부분(N)과 호스트 부분(H)으로 구성되어있으며 IPv4 주소의 첫 번째 옥탯을 통해 해당 주소의 클래스를 판별할 수 있다  

#### <b>IPv4 주소 클래스 구분  

| Class   | 첫 번째 옥탯 |첫 번째 옥탯의 범위 | N & H          |
|:-------:|:---------:|:--------------:|:--------------:|
| A Class | <b><span style="color:red">0</span></b>XXXXXXX.~ |   1 - 127 | N.H.H.H ( /8 ) |
| B Class | <b><span style="color:red">10</span></b>XXXXXX.~ | 128 - 191 | N.N.H.H ( /16 )|
| C Class | <b><span style="color:red">110</span></b>XXXXX.~ | 192 - 223 | N.N.N.H ( /24 )|
| D Class | <b><span style="color:red">1110</span></b>XXXX.~ | 224 - 239 | 멀티캐스팅용      |
| E Class | <b><span style="color:red">11110</span></b>XXX.~ | 240 - 255 | 미래를 위해 예약   | 

<br>

## <b>서브넷 마스크
<hr>
IP 주소의 네트워크와 호스트를 구분해주는 값으로 서브넷 마스크가 있어서 정확한 네트워크 대표 주소와 호스트를 구할 수 있음

<br>

## <b>IP 주소의 클래스의 네트워크와 호스트를 구분하는 과정
<hr>
  > 1. IP주소의 옥택을 2진수로 변환
  > 2. 경계선 설정 (서브넷 마스크의 1과 0의 경계에 경계선 생성)
  > 3. Bit 단위 AND 연산 ( 경계선 좌측까지만 연산 )

<br>

## <b>IPv4의 통신(전송) 방식의 종류  
<hr>
  1. 브로드캐스트(Broadcast) : 1 대 불특정 다수 통신 
    - 동일 네트워크 안의 모든 호스트들에게 통신하는 방식  
  2. 유니캐스트(Unicast) : 1 대 1 통신 ( ≒ 개인톡 )  
  3. 멀티캐스트(Multicast) : 1 대 특정 다수 통신 ( ≒ 단톡방 )  

<br>

## <b>IPv6의 통신(전송) 방식의 종류  
<hr>
  1. 유니캐스트(Unicast) : 1 대 1 통신( ≒ 개인톡 )  
  2. 멀티캐스트(Multicast) :  1 대 특정 다수 통신 ( ≒ 단톡방 )  
  3. 애니캐스트(Anycast)  