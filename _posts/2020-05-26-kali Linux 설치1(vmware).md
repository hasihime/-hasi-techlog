---
title:  "칼리리눅스 - 1(VMWare 세팅)"
date:   2020-05-26 22:50:23
categories: [kali]
tags: [kali]
---
**kali리눅스 설치** 

## Kali Linux 설치법 -(VMWare 세팅)
<hr>
가상화 기반에서 진행한다는 조건하에 설명을 진행하다. 우선 필자는 VMWare Workstation Pro버전이 있기에 이로 진행하지만 Virtual box로도 큰 문제는 없이 진행된다.

우선은 Kali Linux ISO를 다운받아주자. 2020년 5월 기준 최신 릴리즈 버전은  2020.2 버전이다.

[다운로드 링크](https://www.kali.org/downloads/)

해당 링크에 들어가서 64bit 두번째 파일을 다운받아준다.


<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_005.png">
<br>
우선 VM에 새로운 가상머신을 생성해주자. File - New Virtual Machine 클릭하면 다음과 같은 화면이 나온다. 여기서 Comstom(advanced)를 선택하고 Next.<br>

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_006.png">
<br>
다음은 vmware의 버전을 설정하는 것인데 특별한 이유가 없으면 최신 버전으로 해주자. 필자는 워크스테이션 12이므로 12로 진행<br>

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_007.png">
<br>
다음은 이미지를 추가하는 것인데 첫번째는 실제로 CD Disk를 넣어서 설치 두번째는 ISO를 선택 세번째는 나중에 설치인데 일단은 나중에 설치를 선택하고 Next <br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_008.png">
<br>
다음은 운영체제를 선택하는 것인데 게스트 운영체제를 Linux에 맞추고 아래 버전은 Debian 8.x 64bit를 선택. Kali리눅스는 보이지 않으므로 데비안으로 설정하자. <br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_009.png">
<br>
다음은 가상머신의 이름과 설치 위치를 지정하는 것이므로 원하는 이름과 편한 위치를 설정하고 다음 클릭 <br>

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_010.png">
<br>
다음은 프로세스와 코어수를 설정하는 화면인데 넉넉잡아 프로세서당 코어 2, 2프로세서를 추가해주자<br>

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_011.png">
<br>
다음은 메모리 설정이다. 메모리 권장사항은 칼리 홈페이지에 다음과 같다.<br>

[해당 문서 원본](https://www.kali.org/docs/introduction/installation-requirements/)
>Kali Linux installation requirements
>
>The installation requirements for Kali Linux vary depending on what you would like to install. On the low end, you can set up Kali as a basic Secure Shell (SSH) server with no desktop, using as little as 128 MB of RAM (512 MB recommended) and 2 GB of disk space. On the higher end, if you opt to install the default XFCE4 desktop and the kali-linux-default meta-package, you should really aim for at least <b>2048 MB of RAM and 20 GB of disk space</b>.
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_017.png">

즉 2048MB의 메모리와 20GB의 디스크 용량이 필요하다. 각각 상황에 맞게 최소 2GB가 넘는 메모리 설정을 해주자. 여기선 4GB로 잡아주었다.<br>

<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_012.png">
<br>
다음은 네트워크 설정. 여기서 브릿지와 NAT에 대해 자세히 설명하기는 힘들지만 간단하게 설명하면 Bridge는 호스트PC(여기서는 설치하는 PC겠죠.)와 같은 네트워크 대역의 IP를 가지게 됩니다. NAT는 호스트 밑에 자체 네트워크 대역을 만들어서 통신하죠. 그래서 대체로 NAT로 설치한 리눅스의 IP 주소는 사설주소 (10.0.0.0~10.255.255.255 대역, 172.16.0.0~172.31.255.255 대역, 192.168.0.0~192.168.255.255대역)를 가지게 되고 Bridge는 호스트 PC와 같은 네트워크 대역을 가집니다.(물론 호스트 PC도 공유가 같이 밑에 있으면 같이 사설 IP대역을 가집니다. 공유기가 NAT 역할을 하기 때문에..)<br>
그래서 일단은 Bridge로 설정해줍시다. 외부에서도 접속이 가능하고 테스팅을 원할하게 하기 위함입니다.<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_013.png">
<br>
이부분은 I/O 컨트롤러 타입 설정입니다. 딱히 건들일 것은 없으니 다음.
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_014.png">
<br>
디스크의 종류 설정입니다. 다들 하드디스크의 차이고 원래는 속도의 차이나 안정성의 차이가 있긴 합니다만 가상머신 환경에서는 크게 신경쓰지 않아도 됩니다 .SCSI를 선택.
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_015.png">
<br>
다음은 어떤 디스크를 사용할지인데 첫번째는 새 가상디스크 생성, 두번째는 이미 있는 가상 디스크 사용, 새번째는 물리디스크를 사용인데 여기서는 새 가상디스크를 생성을 클릭합니다. 다음
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_016.png">
<br>
다음은 Disk의 사이즈를 넣어줍니다. 아까 권장사항이 20GB였으니 최소 20GB이상으로 잡아줍시다.
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_018.png">
<br>
다음은 디스크의 이름을 설정해줍니다. 이거는 원하는 이름으로 설정해줍시다.
<br>
<img src="https://hasihime.github.io/hasi-techlog/images/img/kali/200526/200525_019.png">
<br>
이제까지 세팅한 모습을 총괄적으로 볼 수 있습니다. finish를 누르면 VMware상에서 새 가상머신을 만드는데 성공한 것입니다.



나머지 Linux 설치는 다음 포스트에 올리겠습니다.
<br>
추가 컴포넌트부터 네트워크 설정까지 마무리 된다.

### Kali Linux의 Root권한 얻기.

> https://www.kali.org/docs/policy/kali-linux-user-policy/

2020.1 버전으로 Kali의 root계정을 그대로 쓰는게 불가능하고 Sudo를 이용하거나 pkexec라는 명령어를 사용해야 한다.
