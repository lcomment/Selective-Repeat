# Selective Repeat ARQ with UDP Socket
  
  
> ### **1. Selective Repeat ARG란?**
 
 Selective Repeat ARQ에서 수신 측은 정확하게 수신된 각각의 패킷에 대해 ACK를 보낸다. 이 때 송신 측은 ACK를 받지 못한 각각의 패킷들에 대해 Timer를 유지하고, 오류가 발생해 Timeout 된 패킷에 대해서만 재전송이 이루어져 불필요한 재전송을 피할 수 있다.

 패킷에는 순서 번호가 존재한다. 수신 측에서는 순서가 틀린 패킷들은 분실된 패킷이 수신될 때까지 버퍼에 저장하고, 직렬 화 된 패킷들은 순서대로 상위 계층에 전달된다. 송신 측은 N개의 연속적인 순서 번호를 가진 버퍼를 가지고, 특정 크기의 윈도우를 유지하여 아직 확인 응답이 안 된 패킷의 수를 제한한다. 이 때 윈도우의 크기는 순서번호를 2로 나눈 값보다 작거나 같아야 딜레마에 빠지지 않는다.
 
 * * *
   
- [보고서 참고](https://github.com/khsexk/Selective-Repeat/blob/main/Documents/%EC%BB%B4%EB%84%A4_%EB%B3%B4%EA%B3%A0%EC%84%9C.hwp)
