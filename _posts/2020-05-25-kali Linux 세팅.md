---
title:  "칼리리눅스 - 0"
date:   2020-05-25 22:50:23
categories: [kali]
tags: [kali]
---
**kali리눅스 입문기** 

## Kali Linux는 꼭 써봐야....
<hr>
최근에 리버싱과 포렌식을 전문으로 한 지인과 이야기를 하는 도중 보안과 관련되서 재미있는 이야기를 들었다. 보안에 있어서 잔머리가 있는 사람들이 잘 한다고 말이다.

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200525_001.png"><br>
  
>부르트포스에 있어서 2의 n승을 다 계산한다고..?
>
>&nbsp; &nbsp; &nbsp; --> 그러면 키를 늘려버려!

솔직히 단순한 생각이긴 한데 맞는 말이다. 시간을 늘리면 대부분의 공격자들은 다른 취약점이 있는 곳을 해킹하는 것이 유리하기 때문이다.(물론 APT공격같은 경우는 집요하게 다른 취약점을 파겠지만 일단은 넘어가고...)


그리고선 이어진 대화

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200525_002.png"><br>

보안 공격에 있어서 정해진 해답이 없으니 공격자든 방어자든 들고 있는 패가 많다면 공격, 대응을 하는데 유리하다는 점이다.

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200525_003.png">

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200525_004.png"><br>

개인적으로 IDS쪽 보안에 관심이 있는데 이를 분석하는 툴도 다양하게 있어서 이를 활용하면 도움이 될 것이라고 했고 적극적으로 Kali를 사용해보라고 권해주셨다.

<br>
사실 Kali리눅스를 보안을 조금해본 사람이거나 관심이 있다면 한 번쯤은 들어봤을 것이다. 나도 몇 년 전에 Kali리눅스를 사용하기 위해 부팅USB를 만들어서 사용해봤다. 처음에는 MetaExploit이란 툴, Nmap을 이용한 포트 스캐닝 등을 사용해봤는데 USB를 잃어버리고선(...) 그 뒤로 사용을 안하게 되었다.
<br>
<br>
하지만 보안팀 인턴활동도 해보면서 보안에서 다양한 툴이 사용되고 있었다. 대표적으로 <b>Fiddler</b>. <br>request를 보내는걸 proxy에서 가로채고 response를 수정하는 식으로, 대표적으로 업로드, 다운로드 취약점을 분석 할 때 사용해봤다. <br>그 외에 <b>dnspy</b>라는 툴을 이용해  디컴파일 및 디버깅을 하였다. <br>또한 개인적으로 <b>china chopper</b>라는 툴을 사용해서 웹서버의 취약점을 분석하는 툴에 관심이 있었는데 프로그램을 구하지를 못했다.
<br>
이 때에도 다양한 툴의 사용법이 필요하다고 느꼈고, 이 기회에 Kali Linux를 본격적으로 사용을 함으로써 다양한 툴을 통한 보안의 패를 늘려야겠다 필요성을 느껴서 이 포스트를 작성하게 되었다.

## Kali Linux 설치법
<hr>
가상화 기반에서 진행한다는 조건하에 설명을 진행하다. 우선 필자는 VMWare Workstation Pro버전이 있기에 이로 진행하지만 Virtual box로도 큰 문제는 없이 진행된다.

우선은 Kali Linux ISO를 다운받아주자. 2020년 5월 기준 최신 릴리즈 버전은  2020.2 버전이다.

> [https://www.kali.org/downloads/]

해당 링크에 들어가서 64bit 두번째 파일을 다운받아준다.



### Kali Linux의 Root권한 얻기.

> https://www.kali.org/docs/policy/kali-linux-user-policy/

2020.1 버전으로 Kali의 root계정을 그대로 쓰는게 불가능하고 Sudo를 이용하거나 pkexec라는 명령어를 사용해야 한다.
