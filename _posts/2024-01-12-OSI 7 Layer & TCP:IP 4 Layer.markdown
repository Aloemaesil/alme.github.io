---
title: OSI 7 Layer & TCP/IP 4 Layer
author: Alme
date: 2024-01-12 15:33:00 +0800
categories: [네트워크, 개념]
tags: [네트워크, OSI, TCP, IP]
pin:  true
math: true
mermaid: true
---
## <b>OSI 7 레이어 & TCP/IP(Protocol) 4 Layer
<hr>

<table border="OSI 7 레이어 & TCP/IP(Protocol) 4 Layer">
	<th> </th>
	<th>OSI 7 계층</th>
	<tr><!-- 첫번째 줄 시작 -->
	    <td>첫번째 칸</td>
	    <td>두번째 칸</td>
	</tr><!-- 첫번째 줄 끝 -->
	<tr><!-- 두번째 줄 시작 -->
	    <td>첫번째 칸</td>
	    <td>두번째 칸</td>
	</tr><!-- 두번째 줄 끝 -->
</table>  


|              |      OSI 7 계층     |     TCP/IP 4 계층   |
|:------------:|:------------------:|:------------------:|
| <b>7 계층</b> | Application Layer  |                    |
| <b>6 계층</b> | Presentation Layer | Application Layer  |
| <b>5 계층</b> | Session Layer      |                    |
| <b>4 계층</b> | Transport Layer    |  Transport Layer   |
| <b>3 계층</b> | Network Layer      |  Internet Layer    |
| <b>2 계층</b> | Data-Link Layer    |  Network Access Layer | 
| <b>1 계층</b> | Physical Layer     |       Layer        |    
  
<br>  
  
  ### <b> 서브넷팅 실습 </b>  
  <b>1. 토폴로지 구성 & IP와 서브넷 마스크 할당</b>  
    <center>
      <img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/main/_posts/images/20240109/192.168.0.X%3A24.png">
    </center>
    - 다음과 같이 같은 브로드캐스트 도메인을 가지는 토폴로지는 구현
    <center>
      <img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/main/_posts/images/20240109/192.168.0.2%3A24.png">
      <img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/main/_posts/images/20240109/192.168.0.130%3A24.png">
    </center>
    - 192.168.0.X/24 대역대의 IP와 서브넷 마스크를 할당 및 확인 

  <br>

  <b>2. Ping 테스트</b>  
  <center>
    <img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/91a20d3c0664f3fceb9ba24cce20504cc3b761de/_posts/images/20240109/ping 192.168.0.130:24.png">
  </center>
  - 서브넷팅 전에는 192.168.0.1/24와 192.168.0.130/24은 서로 같은 브로드캐스트 도메인이기 때문에 서로 ping 통신이 정상적으로 작동하는 것을 확인할 수 있다.  

  <br>

  <b>3. 서브넷팅 적용</b>  <!-- OK -->
    <center>
      <img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/main/_posts/images/20240109/192.168.0.2%3A25.png">
      <img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/main/_posts/images/20240109/192.168.0.130%3A25.png">
    </center>
    - 기존에 할당된 255.255.255.0의 서브넷 마스크를 255.255.255.128로 수정하여 브로드캐스트 도매인을 나누기.  
  
  <br>

  <b>4. Ping 테스트 및 결과</b>  <!-- OK -->
    <center>
      <img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/91a20d3c0664f3fceb9ba24cce20504cc3b761de/_posts/images/20240109/ping 192.168.0.130:25.png"> 
      <img src="https://raw.githubusercontent.com/Aloemaesil/aloemaesil.github.io/91a20d3c0664f3fceb9ba24cce20504cc3b761de/_posts/images/20240109/192.168.0.X:25.png">
    </center>
    - 서브넷팅이 적용된 이후에는 192.168.0.1/25와 192.168.0.130/25는 사진으로 보이는 것처럼 서로 다른 브로드캐스트 도메인을 가지기 때문에 ping 통신이 정상적으로    되지않는 것을 확인할 수 있다.  

  <br>


## <b>슈퍼넷팅(Supernetting)
<hr>
- 서로 다른 네트워크를 합쳐 하나의 네트워크처럼 만드는 것

<br>

## <b>VLSM(Variable Lenth Subnet Mask)
<hr>
  - 서브넷팅한 네트워크를 다시 서브넷팅 하는 것

<br>

  <!-- 
  	특정 네트워크의 서브넷 마스크를 변경했을 때 해당 네트워크가 나누어지는 가짓수는
  기존 경계선에서 변경된 경계선으로 이동한 비트 수(n)만큼 2를 곱한 값이다.(2n)
   -->
