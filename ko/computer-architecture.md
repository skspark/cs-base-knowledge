컴퓨터 시스템은 크게 아래 4가지로 구분된다.
```
CPU, 메모리, 디스크, IO
```

# CPU
![ca-cpu](/ko/images/ca-cpu-1.png)
[image source](https://www.tutorialspoint.com/computer_logical_organization/cpu_architecture.htm)

CPU의 내부 구성은 크게 산술/논리 연산 장치(ALU), 제어 장치와 레지스터로 구성되어 있다.

1. 산술논리연산장치(ALU: Arithmetic Logic Unit)는 산술적인 연산과 논리적인 연산을 담당하는 장치로 가산기, 보수기, 누산기, 기억 레지스터, 데이터 레지스터 등으로 구성된다.
2. 제어장치는 CPU가 자신 및 주변기기들을 컨트롤하는 장치로, 프로그램의 수행 순서를 제어하는 프로그램 계수기(program counter), 현재 수행중인 명령어의 내용을 임시 기억하는 명령 레지스터(instruction register), 명령 레지스터에 수록된 명령을 해독하여 수행될 장치에 제어신호를 보내는 명령해독기(instruction decoder)로 이루어져 있다.



CPU가 하나의 명령(Operation)을 처리하는 과정은 다음과 같다.

1. 읽기(Fetch Instruction): 메모리에서 명령을 가져온다.
2. 해석(Decode Instruction): 명령을 해석한다.
3. 실행(Execute Instruction): 명령을 수행한다.
4. 기록(Write Back): 수행한 결과를 기록한다.

명령어를 수행하기 위해서 명령어를 가져오는데 이를 Fetch라 한다. Fetch 사이클은 아래와 같다.

1. Program Counter (PC)는 Fetch할 다음의 명령어 주소를 갖고 있다. 프로세스는 PC가 가리키는 주소위치에서 명령어를 가져오면서 PC를 증가시킨다.
2. 명령문은 Instruction Register(IR)에 Load된다. 
3. Load된 명령어는 수행 과정이 진행되는데, 명령어를 수행하는 Execute Cycle Fetch과정에서 가져온 명령어를 실제 ALU(가산기)에서 처리하게 된다.




## Context Switch
하나의 프로세스가 CPU를 사용 중인 상태에서 다른 프로세스가 CPU를 사용하도록 하기 위해, 이전의 프로세스의 상태를 보관하고 새로운 프로세스의 상태를 적재하는 작업을 말한다.
### PCB
![ca-pcb](/ko/images/ca-pcb-1.png)
[image source](https://www.gatevidyalay.com/process-control-block-process-attributes/)




# References
- https://wikidocs.net/22295
- https://wikidocs.net/63816 