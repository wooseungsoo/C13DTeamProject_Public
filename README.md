
https://github.com/user-attachments/assets/03f8bdd9-3502-4f21-8bd7-df290625366b
<img width="1064" height="624" alt="image" src="https://github.com/user-attachments/assets/1755c37f-57b1-4c81-8f95-bf13d441211b" />
<시작부분>

https://github.com/user-attachments/assets/869f0aa7-354a-4b01-9d91-a2bf0c232846

<추격부분>


https://github.com/user-attachments/assets/580f9096-5d0a-45c4-a3d2-e3b12b48569a

<<리드미 업로드용 영상에는 심약자를 위하여 사운드를 제거하였습니다>>

📌 Role & Contribution

본 프로젝트에서 NPC(적) AI 행동 로직 구현을 담당했습니다.
FSM(State Machine) 구조를 기반으로 NPC의 배회 → 감지 → 추적 → 공격 → 이탈 흐름을 설계하고 구현했습니다.

특히 다층 구조 맵에서 발생하는 감지 오탐 문제를 직접 겪고 해결한 경험이 있습니다.
초기 구현에서는 X축 거리 기준 감지로 인해, 다른 층에 있는 플레이어까지 추적 및 BGM이 트리거되는 문제가 발생했습니다.

이를 해결하기 위해 Raycast 기반 접근도 검토했으나,
최종적으로는 플레이어와 NPC 간 Y축(높이) 차이를 조건으로 추가하여
일정 높이 이상 차이가 날 경우 감지/추적이 발생하지 않도록 보정했습니다.

해당 수정 이후, 불필요한 추적과 사운드 트리거가 줄어들어 플레이 체감이 안정화되었습니다.

🧠 Key Implementation Details

FSM 기반 NPC 상태 관리 (Idle / Wandering / Attacking / Fleeing)

NavMeshAgent를 활용한 이동 및 추적

시야각(Field of View) + 거리 기반 플레이어 감지

Y축 높이 차이를 고려한 감지 조건 보정

추적 상태 진입 시 BGM 트리거 제어(hasBgm 플래그)

전투 거리 내 접근 시 공격 애니메이션 및 데미지 처리

💡 What I Learned

실제 플레이 상황에서 발생하는 엣지 케이스를 기준으로 로직을 수정하는 중요성

Vector 계산을 통한 거리/방향 판단

기획 의도와 실제 구현 간 괴리를 코드 레벨에서 조정하는 경험

팀 프로젝트 환경에서 질문과 피드백을 통해 빠르게 개선하는 협업 방식
