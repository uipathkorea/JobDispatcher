# JobDispatcher
분산처리를 위한 Job 분배 로봇 예제 코드  
1. JobDispatcher는 여러개 Robot에 동시에 처리를 해야 할 프로세스에 필요한 데이터를 Queue에 기록하고 복수개의 Job을 Orchestrator에게 지시한다.  
2. Orchestrator는 동일한 Process를 여러개의 Robot에서 실행을 시킨다. 
3. Work Process는 여러개의 Robot에서 구동되면서 필요한 데이터를 Queue로 부터 하나씩 읽어 처리하고 필요시 입력 매개변수로 넘겨준 Result Queue에 처리결과를 저장한다. 
4. JobDispatcher는 Work Process의 실행상태를 주기적으로 체크하면서 모든 작업이 종료된 경우 필요시 Merge Process를 실행하여 Result Queue에 저장된 데이터를 취합하도록 호출한다. 


