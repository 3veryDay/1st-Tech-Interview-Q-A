# Operating System

## 운영체제 기초
<details>
<summary>운영체제란 무엇일까요?</summary>

<hr>
운영체제란 컴퓨터 시스템의 자원을 효율적으로 관리하며 사용자가 컴퓨터를 편리하고 효과적으로 사용할 수 있는 환경을 제공하는 여러 프로그램들의 모임이다.
또한, 응용 프로그램과 하드웨어 간의 인터페이스이다.

넓은 의미에서 커널 뿐만 아니라, 시스템을 위한 유틸리티를 포함하는 개념이며, 좁은 의미에서는 메모리에 올라가 있는 커널을 의미한다.
커널은 전체 운영 체제 코드 중 메모리에 올라가있는 부분이다.

<hr>
</details>

<details>
<summary>운영체제는 어떤 기능을 하는지 설명해주세요</summary>

<hr>
 1. CPU 스케줄링
 
 2. 메모리 관리

 3. 파일 관리
 
 4. 입출력 관리
 
 5. 프로세스 관리
 
 6. 네트워킹
 
 7. 보호

  - 시스템의 오류를 검사하고 복구한다.
    
  - 자원 보호 기능을 제공한다.
<hr>
</details>

<details>
<summary>운영체제가 관리하는 5가지 지원에 대해 설명해주세요</summary>

<hr>
프로세스, 저장장치, 네트워킹, 주변 장치, 사용자 이렇게 5가지 지원을 한다.

1. 프로세스 관리

프로세스의 스케줄링과 동기화 관리를 담당한다.
프로세스의 생성과 제거, 시작과 정지, 메시지 전달 등의 기능을 담당한다.

2. 저장장치 관리

저장 장치에는 메인 메모리인 1차 저장장치와 하드디스크, NAND 등인 2차 저장장치가 있다.
운영체제는 이러한 저장장치를 관리하며, 프로세스에게 메모리 할당 및 회수, 파일 생성과 삭제, 변경 유지 등의 관리를 한다.
  - 1차 저장장치(Main Memory)
    프로세스에 할당하는 메모리
    영역의 할당과 해제각 메모리 영역 간의 침범 방지
    메인 메모리의 효율적인 활용을 위해서 가상 메모리 기능도 제공
  - 2차 저장장치(HDD, NAND Flash Memory 등)
    파일 형식의 데이터 저장
    이런 파일 데이터 관리를 위한 파일 시스템이 있는데, 이를 OS에서 관리
    FAT, NTFS, EXT2, JFS, XFS 등 많은 파일 시스템이 개발되어서 사용 중

##### HDD와 NAND Flash Memory에 대해서
메모리 반도체는 무조건 스위칭 기능과 데이터 저장 기능을 갖는다.

DRAM은 스위칭 기능이 빠르고, NAND Flash Memory는 데이터 저장 기능이 월등하다. NAND Flash Memory는 전원이 꺼져도 창고라는 공간에 저장된 데이터가 존재하므로 '비휘발성 메모리'라고 하고, DRAM은 전원이 꺼지면 데이터는 무조건 소멸하기 때문에 '휘발성 메모리'라고 부른다.

3. 네트워킹

TCP/IP 기반의 인터넷에 연결하거나 응용 프로그램이 네트워크를 사용하면 OS에서 네트워크 프로토콜을 지원한다.
이처럼 OS는 응용 프로그램과 하드웨어 사이의 인터페이스 역할을 하면서 하드웨어를 소프트웨어적으로 제어 및 관리를 하고 있다.

4. 주변 장치 관리

입출력 장치의 스케줄링 및 전반적인 관리를 담당한다.
디바이스 드라이버를 OS가 관리해서 여러 하드웨어를 사용할 수 있도록 해준다


##### 디바이스 드라이버
디바이스란 하드 디스크, USB, 프린터, 단말기, 네트워크 어댑터, 터치 스크린, 오디오 등 컴퓨터 시스템 이외의 다른 주변 장치들을 말한다.

디바이스 드라이버(DD) 란 위의 디바이스들을 동작시키기 위해서 필요한 구동용 소프트웨어이다.
응용 프로그램에서 하드웨어 장치를 이용해서 데이터를 접할 때, DD를 사용한다.

5. 사용자 관리

사용자별 계정을 관리할 수 있는 사용자 관리 기능을 제공한다.
<hr>
</details>

<details>
<summary>시분할 시스템, 다중 프로그래밍 시스템, 대화형 시스템은 각각 무엇을 의미할까요?</summary>

<hr>
시분할 시스템이란 CPU 작업시간을 여러 프로그램이 나누어 쓰는 시스템이다.

다중 프로그래밍 시스템은 메모리 공간을 분할해 여러 프로그램들을 동시에 메모리에 올려서 처리하는 시스템이다.

대화형 시스템은 사용자 관점에서 각 프로그램에 대한 키보드 입력의 결과를 곧바로 화면에 보여주 시스템이다.

3 시스템 모두 하나의 컴퓨터에서 여러 프로그램이 동시에 실행되는 **다중 작업용 운영체제**에 속한다.

<hr>
</details>

<details>
<summary>인터럽트란 무엇일까요?</summary>

<hr>

 CPU가 프로그램을 실행하고 있는 중, 예기치 않은 상황이나 먼저 수행해야할 일이 발생한 경우, 현재 실행중인 작업을 즉시 중단하고, 발생한 상황이 먼저 처리되어야 함을 CPU에게 알리 것이다.

 인터럽트는 크게 Hardware Interrupt와 Software Interrupt가 있다.

 하드웨어 인터럽트는 각각의 하드웨어 I/O device에서 발생한 인터럽트다.

 - 입출력 인터럽트
 - 정전 전원 이상 인터럽트
 - 기계 착오 인터럽트 = CPU의 기능적인 오류
 - 외부 신호 인터럽트

소프트웨어 인터럽트가 더 중요하다. (Trap)

CPU 내부에서 자신이 실행한 명령이나 CPU 명령 실행에 관련된 모듈에서 오류가 생기거나 System call을 호출할 때 발생한다.
- System Call : 애플리케이션이 커널의 함수를 실행하기 위해서 발생시킨다.
- Exception : divide by zero, overflow, underflow ...

d
<hr>
</details>

<details>
<summary>폴링(Polling)이란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>Mode bit이란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>System Call이란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>System Call과 Function Call의 차이점에 대해 설명해주세요</summary>

<hr>
<hr>
</details>

<details>
<summary>DMA란 무엇일까요?</summary>

<hr>

<hr>
</details>

## 프로세스와 스레드
<details>
<summary>프로세스와 프로세서의 차이에 대해 설명해주세요.</summary>

<hr>

<hr>
</details>

<details>
<summary>프로세스와 스레드의 차이를 설명해주세요</summary>

<hr>


<hr>
</details>

<details>
<summary>프로세스의 주소 공간은 어떻게 이루어져 있을까요? 그리고 각각의 주소 공간에는 어떤 데이터가 저장될까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>프로세스 주소 공간을 나눈 이유는 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>프로세스의 상태에는 어떤 것이 있을까요?</summary>

<hr>


<hr>
</details>

<details>
<summary>프로세스의 Running State에서 CPU 자원을 뺐기는 3가지 상황에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>OS는 프로세스의 정보를 어떻게 관리하며 어떤 데이터들을 저장하고 있는지 설명해주세요 (hint.PCB)</summary>

<hr>

<hr>
</details>

<details>
<summary>PCB가 왜 필요할까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>PCB는 어떻게 관리될까요??</summary>

<hr>

<hr>
</details>

<details>
<summary>Process Context란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>IPC란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>스레드란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>하나의 프로세스 안에서 만들어진 스레드들간 공유하는 공간과 독립적으로 할당하는 공간은 각각 무엇이 있을까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>커널 스레드와 유저 스레드란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>TCB란 무엇일까요?</summary>

<hr>


<hr>
</details>

<details>
<summary>멀티 스레드의 장단점에 대해 설명해주세요.</summary>

<hr>

<hr>
</details>

<details>
<summary>멀티 스레드와 멀티 프로세스의 차이에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

## CPU 스케줄링
<details>
<summary>장기, 중기, 단기 스케줄러에 대해 설명해주세요.</summary>

<hr>

<hr>
</details>

<details>
<summary>선점과 비선점 스케줄링의 차이에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>CPU Scheduling을 측정하는 척도에는 무엇이 있을까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>CPU Scheduling의 종류에는 무엇이 있을까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>Starvation은 어떤 스케줄링에서 발생하는 문제일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>Aging이란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>선점 스케줄링과 비선점 스케줄링에는 각각 어떤 것이 있을까요?</summary>

<hr>

<hr>
</details>

## Synchronized
<details>
<summary>경쟁 상태(Race Condition)이란 무엇이며 언제 발생할까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>임계영역(Critical Section)에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>Mutex Lock과 Semaphore에 대해 설명해주세요. (+ 둘은 어떤 차이가 있나요?)</summary>

<hr>

<hr>
</details>

<details>
<summary>Priority Inversion은 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>데드락(Deadlock)이란 무엇이며 언제 발생할까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>데드락 예방, 회피, 무시에 대해 각각 설명해주세요.</summary>

<hr>

<hr>
</details>

## 메모리
<details>
<summary>메모리 계층 구조를 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>가상 주소는 왜 사용할까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>주소 바인딩(Address Binding)의 3가지 방법은 무엇이 있으며 각각의 특징에 대해 설명해주세요.</summary>

<hr>

<hr>
</details>

<details>
<summary>MMU란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>캐시란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>지역성(Locality)이란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>동적 로딩과 동적 연결에 대해 각각 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>스와핑(Swapping)에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>메모리의 연속 할당과 불연속 할당에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>페이징(Paging)에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>TLB에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>세그먼테이션(Segmentation)에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>페이지드 세그먼테이션(Paged Segmentation)이란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>페이징과 세그먼테이션의 차이점에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>가상 메모리란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>외부 단편화(External Fragmentation)와 내부 단편화(Internal Fragmentation)에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>Demand Paging에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>페이지 교체(Page fault 처리)의 전반적인 순서에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>페이지 교체 알고리즘은 어떤 것이 있을까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>페이지의 전역 교체와 지역 교체에 대해 설명해주세요</summary>

<hr>

<hr>
</details>

<details>
<summary>스레싱(Thrashing)이란 무엇일까요?</summary>

<hr>

<hr>
</details>

<details>
<summary>워킹셋 알고리즘과 페이지 부재 빈도 알고리즘에 대해 설명해주세요.</summary>

<hr>

<hr>
</details>
