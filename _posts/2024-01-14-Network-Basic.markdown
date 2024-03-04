---
title: Network 기초 용어
author: Alme
date: 2024-01-14 11:33:00 +0800
categories: [네트워크, 개념]
tags: [네트워크, 개념]
pin:  true
math: true
mermaid: true
---

<img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/91a20d3c0664f3fceb9ba24cce20504cc3b761de/_posts/images/20240114/test.png">

![이미지](https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/91a20d3c0664f3fceb9ba24cce20504cc3b761de/_posts/images/20240114/test.png)

## 네트워크(Network)
<hr>
통신 가능한 장비(노드)들이 데이터를 주고받을 수 있게 연결한 통신망  

<br>

## 노드(Node)
<hr>
IP주소와 MAC주소의 조합으로 구성된 NAC(Network Access Control)의 논리적인 연결 단위  
즉, 노드는 통신(네트워크에 연결) 가능한 장비라고 생각하면 된다  

<br>

## 네트워크 유형
<hr>

### 1. LAN(Local Area Network)  
- LAN(근거리 통신망)은 일반적으로 지역화된 영역 내에서 연결된 컴퓨팅 장치 그룹  
<br>

### 2. WAN(Wide Area Network)  
- WAN(광역 네트워크)은 디바이스가 넓은 지역에서 통신할 수 있도록 장거리에 걸쳐 여러 LAN을 연결하는 네트워크  
( WAN은 여러 개의 상호 연결된 LAN으로 구성 )

<br>

## 토폴로지(Topology)
<hr>
컴퓨터 및 기타 네트워크 구성요소의 물리적 연결(배치) 형태

### 토폴로지 종류
> 
1. 버스형
2. 링형
3. 스타형 등
<br>


## IPv4 주소
<hr>
IPv4 주소는 4개의 옥탯(1 옥탯 = 8bit)으로 구성되어 있으며, 5개의 클래스로 구분된다 (A, B, C, D, E)  
IPv4 주소는 네트워크 부분(N)과 호스트 부분(H)으로 구성되어있으며 IPv4 주소의 첫 번째 옥탯을 통해 해당 주소의 클래스를 판별할 수 있다  

### IPv4 주소 클래스 구분
<hr>

| Class   | 첫 번째 옥탯 |첫 번째 옥탯의 범위 | N & H          |
|:-------:|:---------:|:--------------:|:--------------:|
| A Class |    0      | 1 - 127        | N.H.H.H ( /8 ) |
| B Class |    10     | 128 - 191      | N.N.H.H ( /16 )|
| C Class |   110     | 192 - 223      | N.N.N.H ( /24 )|
| D Class |   1110    | 224 - 239      | 멀티캐스팅용      |
| E Class |  11110    | 240 - 255      | 미래를 위해 예약   | 

<br>

## 서브넷 마스크
<hr>
IP 주소의 네트워크와 호스트를 구분해주는 값으로 서브넷 마스크가 있어서 정확한 네트워크 대표 주소와 호스트를 구할 수 있음

<br>

## IP 주소의 클래스의 네트워크와 호스트를 구분하는 과정
<hr>
  > 1. 2진수 변환
  > 2. 경계선 설정 (서브넷 마스크의 1과 0의 경계에 경계선 생성)
  > 3. Bit 단위 AND 연산 (경계선 좌측까지만 연산)
