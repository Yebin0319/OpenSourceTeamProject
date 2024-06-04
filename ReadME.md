# 오픈소스S/W 2팀 github 레포지토리

## 명단

#### 조장 : 오현우 / 201802265 / 전자물리학과

##### 팀원 :

1. 허준재 / 202103686 / 컴퓨터공학부
2. 구예빈 / 202303475 / 컴퓨터공학부
3. 이동재 / 201802493 / 전자물리학과

## 디자인

1. 홈, 인게임, 설정
2. 5월 첫째주까지
3. Boo 캐릭터 추가, 애니메이션 추가.

## 함수 설명

1. ﻿ButtonController:
    버튼을 클릭하는 기능을 처리하는 클래스를 정의합니다.
    Start 함수는 게임 object가 활성화되면 호출되는 함수입니다. Start()의 기능은 버튼이 클릭되면 TaskOnClick 메서드를 실행하는 것입니다.
    TaskOnClick 함수는 버튼이 Replay이거나 Play이면 InGameScene이 실행되고, Home이면 MainScene이 실행되는 것입니다.

2. ﻿CharacterManager 클래스:
    캐릭터와 관련된 기능을 할 수 있는 클래스를 정의합니다.
    캐릭터의 인덱스를 읽기 위해 index를 선언하고, 캐릭터 이름들을 배열로 정의하고, DSLManager로 캐릭터의 정보와 설정들을 가져오고, 버튼, 소리, 이미지, 이름 보여주는 변수들을 선언합니다.<br>
<br>
 1) ﻿Awake()는 선택된 캐릭터 인덱스를 가져와서 초기화하고, 오디오 소스를 가져와서 소리를 키거나 SoundBtn이 눌리면 음소거가 되는 코드를 추가하고, ArrowBtn을 초기화해줍니다.<br>
 2) ﻿ArrowBtn()은 버튼에 따라 방향을 결정하는 코드입니다. 만약 dir이 Right이면 인덱스를 하나 증가해주고 dir이 Left이면 인텍스를 하나 감소합니다. 또한 캐릭터 이미지와 이름을 업데이트 하며 버튼 활성화 상태를 결정해줍니다.<br>
 3) ﻿Character 클래스<br>
 캐릭터의 영어, 한글 이름을 전언하고, 선택여부를 설정하고 이를 배열로 나타냅니다.<br>
 4)﻿Inform 클래스<br>
 Inform클래스는 게임 설정란에 설정기능을 담당합니다. 에이쁠이 보2조는 설정란에 소리 on, off, 진동 기능을 추가했습니다. Inform()은 게임이 처음 시작될 때, 데이터를 로드 할때 등 현재 상태를 결정하는 함수입니다.<br>
 5)﻿ Ranking 클래스<br>
 점수와 캐릭터의 index를 빋아와서 캐릭터가 몇 점을 가지고 있는지 순위 정보를 저장하는 클래스입니다.<br>


3. ﻿DSLManager 클래스
 캐릭터, 랭킹, 설정 등 배열에 있는 정보 값들을 저장합니다. 
또한, gameManager, characterManager은 각각 다른 gameManager, characterManager 클래스를 참조하고, characterSprite은 캐릭터 이미지 배열을 저장하고, rankCharacterImg은 순위에 따라 캐릭터를 나열하는 배열입니다.

