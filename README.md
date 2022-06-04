# helloworld_20212583
## 리눅스 명령어에 대해 조사

1) ### 리눅스 명령어 top
> **top란?** 

top 명령어는 시스템의 프로세스/메모리 사용 상태를 5초의 간격으로 업데이트하여 출력한다.

---

화면에 출력되는 기본값은 현재시간, 시스템 업데이트 시간, 시스템에 로그인한 사용자 수, 지난 1분, 5분, 15분간의 시스템 평균부하를 출력한다.

***

**사용방법**

top [옵션]

* -b : 배치모드로 정보를 출력한다. 실시간 상화 대화형모드로 정보를 화면에 일렬로 출력한다.
* -d delay : 지정한 시간(delay 초)의 간격으로 정보를 업데이트하여 출력한다.
* -i idle : 토글값이 off일 때, idle 프로세스나 좀비 프로세스 정보를 출력하지 않는다.
* -n num : 지정한 시간(num)만큼 업데이트 정보를 출력한다.
* -p pid : 지정한 프로세스 ID(pid)의 정보만을 출력한다.
* -q : 시간의 간격 없이 계속하여 업데이트 정보를 출력한다.
* -s : 몇 개의 대화식 명령을 비활성화한다(시큐어 모드).
* -S : 누적된 정보를 출력한다(cumulative 모드).
 
* [네이버 지식백과] top (유닉스 리눅스 명령어 사전, 2010. 11. 30., 우종경, 박종오)

2) ### 리눅스 명령어 ps
> **ps란?** 

ps 명령어는 프로세스의 현재 상태를 출력한다.

***

**사용 방법**

ps [옵션]

* ps : pid, cmd 등 프로세스의 기본적인 내용만 출력
* -e : 모든 프로세스를 출력
* -f : 풀 포맷으로 출력(uid, pid, ppid, TTY 등 정보를 보여줌)
* -l : 긴 포맷으로 출력(풀 포맷+F, S, PRI 등 정보를 더 보여줌)
* -p 1 : 프로세스 번호가 1인 프로세스를 출력
* -u seek : 계정이 seeek인 프로세스들을 출력
* -ef | more : 모든 프로세스를 풀 포맷으로 출력, more 명령어를 이용하여 페이지 단위 출력
* -ef | grep seek : 모든 프로세스를 풀 포맷으로 출력한 목록에서 grep를 이용해 seek이 포함된 행(Row)을 출력

* <https://blog.naver.com/dktmrorl/222416977486>

3) ### 리눅스 명령어 jobs
> **jobs란?** 

jobs는 작업이 중지된 상태, 백그라운드로 진행 중인 작업 상태, 변경되었지만 보고되지 않은 상태 등을 표시한다.

***

**사용 방법**

* -l : 프로세스 그룹 ID를 state 필드 앞에 출력한다.
* -n : 프로세스 그룹 중에 대표 프로세스 ID를 출력한다.
* -p : 각 프로세스 ID에 대해 한 행씩 출력한다.
* command : 지정한 명령어를 실행한다.

* [네이버 지식백과] jobs (유닉스 리눅스 명령어 사전, 2010. 11. 30., 우종경, 박종오)

**주요 옵션**
|옵션|설명|
|------|------|
|-l|프로세스 ID표시|

**사용 예제**
|상태|내용|
|-----|-----|
|Running|실행 중|
|Stopped|일시 중단(Ctrl + Z)|
|Terminated|강제 종료(kill 명령 종료)|
|Done|정상 종료|

![image](https://user-images.githubusercontent.com/104884546/171999316-b4beedcf-40d8-4c71-9d76-c8ac0db4eccb.png)

4) ### 리눅스 명령어 kill
> **kill란?** 

kill 명령어는 프로세스에 종료 시그널을 보낸다. 시스템에 얘기치 않은 문제가 생긴 프로세스를 종료시킬 수 있다.

***

**사용 방법**


![image](https://user-images.githubusercontent.com/104884546/172019365-5e5742c5-5ec0-4af7-bc49-09d52c3c8963.png)

* pid ··· : 종료시킬 프로세스 ID나 프로세스 이름을 지정한다.
* -s : 전달할 시그널의 종류를 지정한다. 여기에는 시그널 이름이나 번호를 써준다.
* -l : 시그널로 사용할 수 있는 시그널 이름들을 보여준다. 이것은 /usr/include/linux/signal.h 파일에서도 알 수 있다.
* -1, : -HUP 프로세스를 재활성화한다.
* -9 : 프로세스를 강제로 종료시킨다.

* [네이버 지식백과] kill (유닉스 리눅스 명령어 사전, 2010. 11. 30., 우종경, 박종오)

## VIM 에디터 명령어조사

### 매크로(macro) 사용방법

1) #### 매크로 저장하기

