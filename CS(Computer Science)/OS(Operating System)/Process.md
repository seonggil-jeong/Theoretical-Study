# Process

# 1. 프로세스

## 1.1 What is process?

### **💡 What is process?**

메모리에 올려져있는 실행 중인 파일

🌟 Process와 Program의 차이

Programe : Disk에 저장된 실행 가능한 파일 → 메모리에 올려지면 Process

### **💡 Process in Memory**

Stack : 지역변수를 담음 (임시 데이터)

Heap : 동적 할당 데이터

Data : 전역변수

Text : 모든 코드

### **💡 Process State**

New : 프로세스 생성

Ready : 실행을 기다리는 상태

Running : 프로세스가 실행 중

Waiting : 입출력 등으로 인해서 대기 중인 상태

Terminated : 프로세스 실행이 끝난 상태

💫 PCB : 프로세스의 정보를 담고 있는 블록 / 하나의 프로세스는 하나의 PCB를 가짐

## 1.2 Process scheduling

한정된 CPU에서 여러개의 프로세스를 관리할 때 효율적으로 CPU를 사용하기 위해 프로세스간의 실행시간을 조정

### 💡 Context Switching

스케줄링에 의해서 실행중인 프로세스에서 다른 프로세스로 전환될 때

➡ 현재 프로세스의 정보를 저장하고, 새로운 프로세스를 로드하는 과정

- PCB가 프로세스를 저장하고 로드하는데 사용됨
- Context Switching하는 동안 시스템은 idle 상태 → overhead가 큼

※ **What is overhead**

어떤 처리를 하기 위해 들어가는 간접적인 처리 시간

ex.) 처리를 단순하게 실행하면 10초가 걸리는데, 안전성을 위해 B 처리를 추가 실행  처리시간 : 15

5초가 overhead

## 1.3 프로세스 생성

### 💡 fork() VS exec()

**fork() : OS가 새로운 메모리 공간을 할당하도록 함 → 프로세스의 코드와 정보를 새로운 공간에 복사**

- A, A_copy

**exec() : 현재 프로세스의 공간에 새로운 프로세스가 덮이는 것**

- A → A_v2