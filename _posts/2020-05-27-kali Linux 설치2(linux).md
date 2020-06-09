---
title:  "칼리리눅스 - 2(Linux 설치)"
date:   2020-05-26 22:50:23
categories: [kali]
tags: [kali]
---
**kali리눅스 설치** 

## Kali Linux 설치법
<hr>
가상화 기반에서 진행한다는 조건하에 설명을 진행하다. 우선 필자는 VMWare Workstation Pro버전이 있기에 이로 진행하지만 Virtual box로도 큰 문제는 없이 진행된다.

우선은 Kali Linux ISO를 다운받아주자. 2020년 5월 기준 최신 릴리즈 버전은  2020.2 버전이다.

<br>
추가 컴포넌트부터 네트워크 설정까지 마무리 된다.


<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_021.png">
<br>
우선 설치할 때 넣지 않았던 ISO 파일을 넣어준다. Virtual Machine Settings - CD/DVD (IDE)에서 오른쪽 아래 Use ISO Image file에서 다운받았던 Kali ISO를 지정해주자.
<br>

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_022.png">
<br>
그리고 가상머신을 시작해주면 다음과 같은 초기화면이 나온다. 해당화면에서 아래 방향키를 눌러 5번째 Graphical Install에서 엔터키를 눌러주자
<br>

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_023.png">
<br>

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_024.png">
<br>

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_025.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_026.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_027.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_028.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_029.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_030.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_031.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_032.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_033.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_034.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_035.png">
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_036.png">
<br>
### Kali Linux의 Root권한 얻기.

> https://www.kali.org/docs/policy/kali-linux-user-policy/

2020.1 버전으로 Kali의 root계정을 그대로 쓰는게 불가능하고 Sudo를 이용하거나 pkexec라는 명령어를 사용해야 한다.
