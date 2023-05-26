Get a match timeline by match id
- get api : /lol/match/v5/matches/{matchId}/timeline
- understand timeline data
- define "한타" and detect when does "한타" starts.
- 한타 : 팀내 거리가 400 이하일 때 시작된다.
- 팀내 거리 : 5명 중 2명씩 유클리디안 거리를 구하고 이를 평균낸다.



* 더 생각해야 할 것들 *

- 어느정도 거리 이내에 모여있어야 한타 진행중이라고 판단할 수 있을까?

- 실제 데이터를 같이 봐야 알 수 있을것 같다.

- 그리고 4명만 모였을 때 팀의 distance로 판단해야 할 수도 있음 (탑이나 정글 한타에 안올수도 - 그럼 한타에 참여하지 않은 소환사는 어떻게 평가해? 포탑 부시던가 정글 데미지 입힌거?)

- 한타 시작 시점을 정의했는데, 끝나는 시점은 어떻게 정의할 수 있을까?

- 한타 중의 데이터로 각 라인별 1인분 여부를 판단한다면 사용 지표는 뭐가있을까?

    탑 : 'totalDamageTaken' , 'totalDamageDoneToChampions'

    미드 : 'magicDamageDoneToChampions' , 'totalDamageDoneToChampions'

    정글 : 'totalDamageTaken' , 정글 킬 이벤트

    원딜 : 'totalDamageDoneToChampions',

    서폿 : 'totalDamageTaken' , 와드관련 이벤트, 힐이나 방어막 정보는 어디있지? , 이동방해 관련 ?
