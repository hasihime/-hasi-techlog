---
title:  "칼리리눅스 - 1"
date:   2020-05-26 22:50:23
categories: [kali]
tags: [kali]
---
**kali리눅스 설치** 

## Kali Linux 설치법
<hr>
가상화 기반에서 진행한다는 조건하에 설명을 진행하다. 우선 필자는 VMWare Workstation Pro버전이 있기에 이로 진행하지만 Virtual box로도 큰 문제는 없이 진행된다.

우선은 Kali Linux ISO를 다운받아주자. 2020년 5월 기준 최신 릴리즈 버전은  2020.2 버전이다.

> (다운로드 링크)[https://www.kali.org/downloads/]

해당 링크에 들어가서 64bit 두번째 파일을 다운받아준다.


<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_005.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_006.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_007.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_008.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_009.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_010.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_011.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_012.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_013.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_014.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_015.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_016.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_017.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_018.png">
<br>
<img src="https://github.com/hasihime/hasi-techlog/blob/master/images/img/kali/200526/200525_019.png">




추가 컴포넌트부터 네트워크 설정까지 마무리 된다.

### Kali Linux의 Root권한 얻기.

> https://www.kali.org/docs/policy/kali-linux-user-policy/

2020.1 버전으로 Kali의 root계정을 그대로 쓰는게 불가능하고 Sudo를 이용하거나 pkexec라는 명령어를 사용해야 한다.
