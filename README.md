# eddies-vote

조직에서 멤버들의 심리적인 안정감, 행복 또는 뭐든지를 정기적으로 체크하고 트래킹하는 슬랙봇입니다.

### 이런 순서로 서비스가 작동해요 😇

1. 멤버들에게 매일 물어보고 싶은 질문을 정해주세요. 답변은 1~10 점으로만 받을 수 있어요
  ex) ㅇㅇ님은 오늘 얼마나 행복한가요?
2. 평일 같은 시간에 멤버들에게 슬랙봇이 개인 메시지로 1의 질문을 물어봅니다. 멤버들은 답변할수 있어요. 하루동안 답변을 안하면 답을 안한걸로 넘어갑니다.
3. 월요일부터 금요일까지 투표를 받고, 다음주 월요일 오전에 지난주의 평가를 그래프로 슬랙봇이 전송합니다.
  - 지정된 채널에 전체 구성원의 일별 평균 행복도 4주치(20일)의 트렌드 그래프를 전송합니다.
  - 봇이 개인별로 DM으로 개인의 일별 평균 행복도 4주치(20일)의 트렌드 그래프를 전송합니다.


이런 스펙이 필요합니다. 

### 1. 질문 셋팅하기
  - 스페이스당 한개의 질문을 입력할 수 있어요
  - 질문을 전송하는 시간대를 설정합니다. - KST 19:00
  - 답변은 1~10점으로 고정이에요. 
  - 질문을 받았을 때만 답변할 수 있어요. 미리 답변할 수는 없어요.
  - 답변 아이콘을 한 번 누르면 투표. 두 번 누르면 취소가 돼요.
  - 질문은 전송시간~당일 23시59분 동안만 유효해요. 날짜가 바뀌면 답변을 할 수 없어요.
  - 질문 결과 분석을 받을 시점과 받을 채널을 정해요
  
### 2. 질문을 저장하기
  - space, 유저id, 답변날짜, 답변 을 저장합니다.
  
### 3. 그래프를 그리기
  - 스페이스의 응답자들의 일별 평균 점수를 최근 20일까지 그래프로 그래요
  - 개인의 일별 점수를 최근 20일까지 그래프로 그려요
  
### 4. 조직과 개인에게 전송하기
  - 3의 스페이스 평균은 지정 채널에
  - 3의 개별 점수는 DM으로 보냅니다.
