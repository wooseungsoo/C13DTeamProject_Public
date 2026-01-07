
🎮 C13D Team Project – NPC AI (FSM & Detection)

Unity 팀 프로젝트에서 NavMesh 기반 NPC FSM과 플레이어 감지 로직을 구현한 3D 게임 프로토타입입니다.
기획 의도를 실제 플레이 상황에서 검증하는 것을 목표로, NPC의 상태 전이·추격·감지 조건 문제를 직접 설계·수정했습니다.

▶️ Gameplay Videos
🔹 Start / Idle & Wandering

https://github.com/user-attachments/assets/869f0aa7-354a-4b01-9d91-a2bf0c232846

🔹 Chase / Player Detection

https://github.com/user-attachments/assets/580f9096-5d0a-45c4-a3d2-e3b12b48569a

<<리드미 업로드용 영상에는 심약자를 위하여 사운드를 제거하였습니다>>

🧩 Role & Contribution (기여 요약)

NPC AI 시스템(FSM) 설계 및 구현

Idle / Wandering / Attacking / Fleeing 상태 구조 설계

플레이어 감지 로직 개선

단순 거리 기반 감지 문제 해결 (층 차이 오인식 이슈)

NavMeshAgent 기반 이동 및 추격 로직 구현

NPC 행동에 연동된 사운드 트리거 및 연출 처리

시작 씬 및 초반 UI 일부 제작

본 프로젝트에서는 NPC AI와 관련된 시스템 구현을 중심으로 기여했으며,
기획 의도가 실제 플레이에서 어떻게 드러나는지를 반복적으로 검증했습니다.

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
