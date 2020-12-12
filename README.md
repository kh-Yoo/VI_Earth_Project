# 임베디드 4조의 ViEarth

##팀원 : 이성민, 이시형, 최강현, 유종원, 유강현

## 4조가 사용한 제품 및 프로그램

![유니티로고](https://user-images.githubusercontent.com/62977669/101986011-ba369180-3cce-11eb-9843-810111218e52.jpg)

![포토샵어도베로고](https://user-images.githubusercontent.com/62977669/101986531-a6d8f580-3cd1-11eb-99fd-74e58e179ee2.gif)

![라즈](https://user-images.githubusercontent.com/62977669/101986014-bb67be80-3cce-11eb-9b56-494721a8a615.jpg)

## 라즈베리파이를 사용해야 하는 이유
![라즈와서버](https://user-images.githubusercontent.com/62977669/101986230-21a11100-3cd0-11eb-8db4-7e4f0372e7d3.JPG)

코로나 시대인 지금 ViiEarth라는 어플을  통해 친구들과 밖에서 만나지 않고 게임을 할 수 있도록 합니다.

저희는 닌텐도 스위치에서 영감을 받아 라즈베리 파이가 그 역할을 해서 서버 통신을 할 수 있도록 도와줄 것입니다.

## 작품을 만드는 것에 참고한 게임
![어몽어스로고](https://user-images.githubusercontent.com/62977669/101986022-c28ecc80-3cce-11eb-95e1-345379eb5c5f.jpg)

콘솔게임에 대한 진입장벽이 낮아져서 최근 많은 사람들이 돈을 주고 게임을 사는 것에 거리낌이 많이 사라졌습니다.

그러므로 저희는 전 세계인들이 즐겨 게임한 AmongUs를 참고해서 게임 제작했습니다.

# ViEarth 작품 발표 시작합니다!

## VI Earth의 4주차 프로젝트 진행 사항

![KakaoTalk_20200928_143005466](https://user-images.githubusercontent.com/54584364/94410075-e784a080-01b1-11eb-85ca-0c5053c17588.jpg)

[실행 영상](https://youtu.be/y_aLr3tahBc)

1. CinemachineVirtualCamera
- CinemachineVirtualCamera은 기준점을 정하고 해당 기준점에 따라 카메라 영역, 기준점 영역, 카메라 밖의 영역을 각각 따로 설정할수있으며
기준점 영역을 Dead Zone이라 부르며 기준점이 움직이면서 Dead Zone을 벗어나면 카메라가 따라가며 Dead Zone영역 안으로 유지하려는 성질을 갖는다
카메라영역을 Soft Zone이라 부르며 실제 제작된 타일맵 내 사용자에게 보여지는 화면이므로 스케일을 넓혀 광대한 범위를 시각적으로 보여주거나 축소하여 좁은 영역만을 보여줄수있다.

2. Grid(Ground/Trees and Rocks/Water)
- Ground레이어는 현재 화면에서 보여지는 풀밭과 논밭으로 구성이되어있으며 Player가 이동하는데 제약을 주지않는다
- Trees and Rocks 레이어는 Ground레이어 위에 추가된 오브젝트임으로 Player이동에 제약을 주는 Rigidbody2D와 Tilemap Collider2D를 설정하였다.
-Water 레이어는 Ground레이어 외각 부분의 바다를 나타내고 Player가 해당지역을 이동할수없게 Rigidbody2D와 Tilemap Collider2D를 설정하였다.

3. Coin Object/Heart Object
- Coin 오브젝트는 Player가 Coin에 다가가면 타일맵에 Coin이 사라지며 Inventory에 Coin이 나타나게 됩니다. Player가 직접 소지하게되는 아이템입니다
- 해당 Coin 오브젝트를 사용자의 임무로 변형하여 기존의 Coin을 먹으면 Inventory 슬롯에 증가하는것이 아닌 Inventory 슬롯에 다수의 임무를 지정해두고
임무를 클리어할때마다 오브젝트가 줄어드는 형식으로 제작할 예정입니다.

- Heart 오브젝트는 Player가 Heart에 다가가면 타일맵에 Heart가 사라지며 HealthBar에 HP가 10증가하게됩니다. Player의 상태를 변화시키는 아이템입니다.
- 해당 Heart 오브젝트를 플레이어의 임무 오브젝트로 변형하여 Heart오브젝트에 다가가면 HealthBar에 10 증가하는것이 아닌 Heart오브젝트에 다가가서 상호작용 버튼을 눌러
임무를 완료하면 HealthBar가 채워지는 형식으로 제작할 예정입니다.

4. Inventory/HealthBar
- Inventory는 부모 클래스인 Inventory와 자식 클래스인 Slot으로 구성되어있어 Inventory안에 5개의 Slot이 구성되어있고 Slot 내부에는 아이템의 이미지를 나타내는 Tray와 해당 아이템의 수량을 나타내는 QtyText가 구성되어있습니다.
- 해당 Inventory를 플레이어의 임무 표로 변형하여 비어있는 Inventory로 시작하여 아이템을 얻고 채워가는 형식이 아닌 임무(Coin Object)가 채워져있는 상태에서 임무를 완료할때마다
해당 임무의 갯수 및 이미지를 없애는 형식으로 제작할 예정입니다.

- HealthBar는 HealthBar는 큰 막대기 바 안에 플레이어의 체력상태를 비율로 나타내어주는 막대기 바와 밑에 숫자와 글로 표현된 Text로 구성되어있으며 플레이어의 상태를 시각적으로 표현을 해줍니다.
- 해당 HealthBar를 팀의 임무 현황 상태로 변환하여 플레이어 자신 뿐만 아니라 다른 플레이어의 임무까지 합산하여 임무를 할때마다 HealthBar에 일정 수치가 올라가게 표현을 할 예정입니다

5. Player Object
- 저번 주차 Player Object에는 타일맵 이동, 지정된 구역이외 이동 제한, Trees and Rocks오브젝트 부딪힘 설정, Coin및Heart Object 상호작용 기능들을 설정하였으며 위에 설명드렸던 Heart/Coin Object의 개선안에 따른 C#스크립트를 수정하여 제작할예정입니다.

github link : https://github.com/lionkiing33/VI_Earth_w2.git

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

VI Earth의 5주차 프로젝트 진행 사항

![KakaoTalk_20201005_210244275](https://user-images.githubusercontent.com/62977669/95077716-ee318b80-074e-11eb-82ea-70094ed1bb1f.jpg)

[실행 영상](https://youtu.be/I4jKNFJMS68)

터치패드를 이용한 캐릭터 이동

- 컴퓨터에서 이용하는 방향키 혹은 w,a,s,d 키가 아닌 스마트폰에서도 
이용이 가능하도록 터치패드를 이용해서 캐릭터 이동이 가능하게 했습니다.

github link : https://github.com/lionkiing33/VI_Earth_w2.git

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# VI_Earth_Our_Project
## 6주차

![1](https://user-images.githubusercontent.com/62977669/95690666-40454600-0c54-11eb-9c0b-89bb3262f5ab.JPG)
![2](https://user-images.githubusercontent.com/62977669/95690669-420f0980-0c54-11eb-8b60-4b4a3bfd9acc.JPG)
![3](https://user-images.githubusercontent.com/62977669/95690670-42a7a000-0c54-11eb-970d-a923d454d18c.JPG)

[실행 영상](https://youtu.be/xCcYH-45EbU)

-Panel을 이용한 미션 열기  
2개의 Button을 만들었습니다.  
일단 첫 번째 버튼은 캐릭터가 움직여도  
오른쪽 상단에 고정되고  
누르면 Panel이 보이면서 지도가 보이고 자신의 캐릭터 위치를  
표시해주는 역할을 하는 Map 버튼입니다.  
그리고 두 번째 버튼은 캐릭터가 미션을 하기 위해  
고정된 자리에서 캐릭터가 가까이 오면 클릭을 해서  
Panel이 보이면서 미션을 하도록 하는 Mission 버튼입니다.  
아직은 버튼들을 클릭 시 Panel이 뜨게 구현했고  
더 원활한 플레이를 하도록 구현중입니다.  

![1](https://user-images.githubusercontent.com/62977669/95690677-5521d980-0c54-11eb-9416-9af8f956e63e.PNG)
![2](https://user-images.githubusercontent.com/62977669/95690678-55ba7000-0c54-11eb-9dba-f9031edcd759.PNG)
![3](https://user-images.githubusercontent.com/62977669/95690679-56530680-0c54-11eb-8e0f-f842802c5de1.PNG)
![4](https://user-images.githubusercontent.com/62977669/95690680-56eb9d00-0c54-11eb-9180-fe0d5ae6f8ac.PNG)
![5](https://user-images.githubusercontent.com/62977669/95690681-56eb9d00-0c54-11eb-9ba3-a6e81ff7bbd7.PNG)

1. sign up 버튼을 클릭하여 회원가입 창을 생성
2. 생성된 회원가입 창의 공백이 있을 시 sign 버튼을 누를 수 없게 설정하고 cancel 버튼만 가능
   ID, Password, Email을 입력하고 sign 버튼 클릭
3. 입력한 정보 표시
4. 해당 정보가 서버로 전송됨.
5. 데이터베이스에 유저 회원가입 정보 저장

github link : https://github.com/kh-Yoo/VI_Earth_Our_Project.git

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 7주차

[실행 영상](https://youtu.be/-VA0qKtAGOA)

![일과표1](https://user-images.githubusercontent.com/62977669/96365322-c2fd6200-117a-11eb-82fb-903ba079ea8a.JPG)
![일과표2](https://user-images.githubusercontent.com/62977669/96365324-c42e8f00-117a-11eb-8369-ea62b2fcfa2b.JPG)

1. 일과표
기존의 플레이어가 오브젝트를 먹으면 인벤토리에 아이템이 추가되는것을
프로젝트 구성에 맞게 해당 오브젝트의 미션을 완료하여 일과표에 미션목록들이 줄어드는 효과로 변경하였습니다.
프로젝트 화면에는 2가지의 오브젝트가 가지는 미션 목록만 보여지고 있지만 이후 오브젝트와 해당 미션을 추가할 예정입니다.
일과표는 우선 흰색글로 미션 수행이 가능한 오브젝트의 위치, 미션 내용, 플레이어가 수행해야할 미션 갯수가 출력이 되어있습니다.
플레이어가 미션 하나를 클리어하면 노란색 글씨로 변하며, 미션을 모두 완료하면 초록색 글씨로 변합니다.
또한 사용자의 편의에 맞게 일과표를 보고싶지 않은경우 클릭해서 감추는 기능을 만들었습니다.

![상호1](https://user-images.githubusercontent.com/62977669/96365327-c4c72580-117a-11eb-91bf-dc289646b85d.JPG)
![상호2](https://user-images.githubusercontent.com/62977669/96365328-c55fbc00-117a-11eb-849d-603b38f6fe28.JPG)

2. 플레이어와 미션오브젝트의 상호작용
우선 플레이어가 미션 오브젝트를 기존의 배경(타일)과 헷갈리지 않도록 구성하기 위해 거리가 먼경우에는 변화가 없지만
일정거리에 닿을 경우 오브젝트 태두리에 노란색 컬러를 입히고, 오브젝트와 가까운 거리일 경우에는 오브젝트의 색깔을 노란빛으로 만들었습니다.
기존의 오브젝트의 역할이 소모품이었던 것을 우측하단의 버튼을 누르면 미니게임을 플레이하고 성공을 하면 미션이 완료되는 형식으로 제작할 예정입니다.

![지도1](https://user-images.githubusercontent.com/62977669/96365325-c42e8f00-117a-11eb-9c05-5a648220c518.JPG)
![지도2](https://user-images.githubusercontent.com/62977669/96365326-c4c72580-117a-11eb-9ff0-458312a82d45.JPG)

3. 지도 Panel 업그레이드
기존에 만들던 지도 패널에는 지도 이미지만 뜨고 꺼지는 작동이였지만 지금은 지도를 실제 맵의 x축에서 1200 : 1,
y축에서는 900 : 1 비율로 나눠서 사용자의 위치가 지도 패널에 뜨고
실시간으로 지도 패널에 사용자의 위치에 따라 노란 점이 움직인다.
제작하는 게임에 맞는 지도 이미지가 완성이 되면 경계선을 조금 더 정확하게 해서 완성도를 높일 것입니다.

github link : https://github.com/kh-Yoo/VI_Earth_Our_Project.git

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
VI Earth의 8주차 프로젝트 진행 사항

![KakaoTalk_20201026_190214463](https://user-images.githubusercontent.com/54584364/97159289-f9139500-17bd-11eb-924c-fa3693f92459.jpg)

[실행 영상](https://youtu.be/GmK19T4plcA)

플레이어와 미션 오브젝트 사이 거리에 따른 UI변경
- 저번주차에 플레이어가 미션 수행이 가능한 오브젝트에 접근할때 일정 거리에 따른 UI변화를 주어 플레이어에게 미션이 가능한 오브젝트인지 아닌지를 쉽게 확인할수있게끔 보여주었습니다.
- 요번주차에는 플레이어가 미션 오브젝트 내 미션을 수행하기 위한 버튼이 오브젝트와 가까이 있을경우만 버튼이 활성화되고 버튼이미지의 투명도를 낮추고 근처에 오브젝트가 없으면 버튼을 비활성화하고 버튼이미지의 투명도를 높혔습니다.

미션오브젝트 근처에서 미션 수행 버튼 클릭시 이벤트
- 플레이어가 미션 오브젝트에 접근하여 미션 수행 버튼을 클릭하면 화면에 미션패널이 활성화되고 해당 패널의 미니게임을 플레이하고 미니게임을 완료하면 플레이어의 업무표, 미션게이지가 업데이트되고 해당 미션 오브젝트와 플레이어간의 상호작용을 없애는것입니다.
- 요번주차에서는 간단한 미니게임을 구상하였고 해당 미니게임은 미로처럼 구현된 지형에서 빨간색 원에 부딪히지 않고 이동하여 노란색 원에 부딪히면 미션이 완료되는 게임입니다.
- 해당 미니게임의 구성으로는 전체적인 미니게임 패널 안에 하얀색 벽이 있고 좌측의 파란색 네모가 플레이어, 중간에 빨간색 원이 장애물, 우측의 노란색 원은 목표지점입니다. 그리고 해당 패널의 좌측상단에 X표시되어있는 버튼은 해당 미션을 나갈수있는 종료버튼입니다.
- 요번주차에는 플레이어가 미션오브젝트에게 다가가 미션수행버튼을 누르면 미니게임화면이 나오면서 해당 미니게임을 플레이할수있게 구현하였으며 미션 완료 시 이루어지는 업무표,미션게이지의 업데이트 및 해당 미션오브젝트와의 상호작용 해제는 다음주차에 구현할 예정입니다.

github link : https://github.com/lionkiing33/VI_Earth_w2.git

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# VI_Earth_w2

VI Earth의 9주차 프로젝트 진행 사항

![KakaoTalk_20201102_193431859](https://user-images.githubusercontent.com/54584364/97858559-ab110b00-1d42-11eb-8a97-f0ac3fcdb791.jpg)

![KakaoTalk_20201102_193426572](https://user-images.githubusercontent.com/54584364/97858602-ba905400-1d42-11eb-9e78-6fc73b620ffe.jpg)

![KakaoTalk_20201102_193426572_02](https://user-images.githubusercontent.com/54584364/97858630-c845d980-1d42-11eb-877b-2977ccf84217.jpg)

![KakaoTalk_20201102_193426572_01](https://user-images.githubusercontent.com/54584364/97858663-d3006e80-1d42-11eb-9fd0-0a0cdc221471.jpg)

[실행 영상](https://youtu.be/BPOsaszNyBs)

미니맵 패널 수정
- 기존의 미니맵 패널에는 미니맵 내 플레이어의 위치를 알려주는 오브젝트가 미니맵으로 지정한 크기를 벗어나는 문제가 있었습니다. 이를 해결하기 위해 미니맵 패널 내 경계선을 만들고 경계선에 box collider(박스 콜라이더)를 설정하여 충돌되어 지나갈수없게 구현하였습니다.

미니 게임 패널 내 미니게임 완료시 일과표 및 미션진행게이지 업데이트
- 저번주차에 미니게임을 완료하여도 일과표 및 미션 진행 게이지가 업데이트 되지 않는 문제점이 있었습니다. 이를 해결하기 위해 플레이어와 가장 가까운 거리에 위치한 미션오브젝트를 미니게임패널 스크립트에 전달하였고 해당 미션오브젝트 내 미션에 대한 정보를 가진 속성을 따로 추출하여 일과표와 미션진행게이지에 정보를 전달하여 업데이트를 구현하였습니다. 추가적으로 해당 미니게임은 하나의 미션오브젝트에 해당하기 때문에 미니게임의 미션과 일치하지 않는 오브젝트는 미니게임을 활성화 시키지 않았습니다.

github link : https://github.com/lionkiing33/VI_Earth_w2

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Vi_Earth

VI Earth의 11주차 프로젝트 진행 사항(게임 관련)

![KakaoTalk_20201117_001527080_02](https://user-images.githubusercontent.com/54584364/99271224-2d80eb00-286a-11eb-868d-b5f88ead8057.jpg)

![KakaoTalk_20201117_001527080_03](https://user-images.githubusercontent.com/54584364/99271446-3d003400-286a-11eb-9cfc-9a72bfb3b15c.jpg)

[실행 영상](https://youtu.be/r1GyV1tAzdM)

![KakaoTalk_20201117_001527080](https://user-images.githubusercontent.com/54584364/99271619-48ebf600-286a-11eb-948c-d7aaf82650a2.jpg)

[실행 영상](https://youtu.be/QUyOxa9Z-UU)

![KakaoTalk_20201117_001527080_01](https://user-images.githubusercontent.com/54584364/99271773-57d2a880-286a-11eb-91fb-68b437bc0a4b.jpg)

[실행 영상](https://youtu.be/ycVoJ6Xu7p4)

1. 전체적인 맵 재구성
- 저희 Vi_Earth는 할로윈 분위기의 마을에서 벌어지는 마피아게임을 구상하였으며 해당 맵은 그런 분위기에 맞게끔 어두운 느낌을 주는 Sprite만을 사용하여 플레이에 좀 더 몰입감을 제공해 줍니다.
- 해당 맵은 Ground, Object, Inside, Outside 총 4개의 타일 팔레트로 구성되어 있으며 각 타일팔레트는 플레이어에게 있어 layer sorting으로 겹쳐져 사용될수있으며 충돌을 설정하여 지나갈수없게 보여줄수있습니다.
- 해당 맵은 추후에 좀 더 풍성하게 장식품을 추가할 예정입니다.

2. 맵을 기반으로 미니맵 재구성
- 미니맵은 전체적인 맵을 토대로 제작되었으며 맵의 크기와 미니맵의 크기의 비율을 찾아서 해당 비율만큼 축소하여 밑그림을 그렸습니다. 미니맵은 대표적인 공간의 벽만을 본떠서 사용자가 자신 플레이어의 위치를 좀더 이해하기 쉽게 알수있도록 표현해주는것입니다.
- 해당 미니맵은 아직 미니 플레이어의 속도와 플레이어의 속도를 잘 맞추지 못해 싱크로율이 맞지 않기 때문에 수정할 예정입니다.
3. 미션에 해당하는 미니게임 구성

  3-1. 서점 미션 미니게임
  - 사용자가 책 오브젝트에 다가가서 상호작용 버튼을 누르면 책 이미지가 보여지고 주어진 조건의 페이지를 펼치면 미션이 완료됩니다.
  - 해당 미션은 Asset Store에 무료로 업로드되어 있는 "Book - Page Curl"을 활용하였으며 해당 오픈코드의 출처는 명확히 제시하겠습니다.
  - 해당 미션은 아직 책 넘기는 기능만을 담고있어 미션 오브젝트와 연결하지 못하였고 랜덤 페이지 수 조건을 생성하여 미션이 완료되는 진행은 아직 구현하지 못했습니다.

  3-2. 발전소 미션 미니게임
  - 사용자가 발전기 오브젝트에 다가가서 상호작용 버튼을 누르면 전체적인 발전소 이미지가 보여지고 발전기 앞에 손잡이를 돌리면 주변에 8개의 빛이 차례대로 생성되며 8개의 빛이 모두 생성되면 미션이 완료됩니다.
  - 해당 미션은 사용자가 터치를 할때 초기 좌표값을 저장하고 그 이후 변화된 좌표값의 차이를 구하여 터치의 벡터값을 구하고 해당 벡터로 기준점으로부터의 각도로 변환하여 손잡이 오브젝트를 rotation시켰습니다.
  - 해당 미션은 아직 미션오브젝트와 연결하지 못하였고 한바퀴 돌때마다 하나의 빛이 보여줘야하는데 이부분이 아직 보완되지 않았습니다. 

github link : https://github.com/lionkiing33/Vi_Earth.git

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# UnitySihyung VI Earth의 11주차 프로젝트 진행 사항(서버 관련)
배경사진 위에 UI를 구축하여 기능을 구현하였다. 배경사진과 Virus이미지, 케릭터 그림은 모두 직접 그린 그림을 사용하였고 sprite폴더에 저장되어있다.
Canvas안에 Canvas Group을 사용하여 각 UI메뉴들을 통제하였고 FallingVirus라는 화면에 떠다니는 UI image를 따로 구현하였다.
FallingVirus는 각 이미지에 virusScript를 설정하여 구현하였다.
각 메뉴들은 MenuType과 Btn Type 스크립트를 활용해 기능을 구현하였다. 한 메뉴에서 다른 메뉴로 이동할 때 현재 메뉴는 끄고 다음 메뉴를 띄우는 형식이다. 메뉴안의 버튼들의 기능은 Btn Type스크립트를 사용하였다. Btn Type애서 각 버튼의 기능에 맞는 메소드를 버튼과 연결하여 구현하였다. PlayMenu와 JoinMenu의 동작은  RoomScript 스크립트로 구현하였다. ToastMessage는 github자료를 사용하였다.
링크 : https://github.com/herbou/Unituts__toast-messages
StartMenu는 어플 실행 시 가장 먼저 나오는 UI로 Login과 Sign UP기능을 수행한다. 각 버튼을 클릭할 시 LoginMenu, SignUpMenu로 이동한다.
SignUpMenu는 InputField를 활용해 ID를 받아 DataBase에 접근하여 중복체크(ID Check)를 한 뒤 나머지(Email, PassWord)값을 받고 DB에 회원 정보를 저장한다.
LoginMenu는 InputField를 활용해 ID와 PassWord값을 받고 DB에 접근하여 회원정보를 확인 한 뒤 MainMenu로 이동한다. User가 회원 정보를 모른다면 Find ID/PW 버튼을 눌러 FindMenu로 이동하도록 구현하였다.
FindMenu는 InputField를 활용해 Email값을 받고 FindID 버튼을 누를 시 DB에 접근하여 회원 정보를 받은 뒤 ToastMessage로 회원의 ID를 보여준다. 이때 회원의 ID가 여러개라면 모두 보여준다. PassWord의 경우 ID와 Email값을 사용한다. 방법은 Find ID와 동일하다.
MainMenu는 InputField를 활용해 User의 nickname(변경가능한 이름)을 받고 Play 버튼 클릭 시 DB에 접근하여 값을 저장한 뒤 PlayMenu로 이동한다. 그리고 소켓 통신을 활용하여 PlayMenu에 있는 방들의 참가자 정보를 받아 참가자 수를 "?/5"에서 "(참가자 수)/5"로 바꿔 보여주도록 구현하였다. Tutorial, Cash Shop 버튼은 각각 TutorialMenu, CashShopMenu로 이동하도록 구현하였다. Logout 버튼은 StartMenu로 이동한다.
PlayMenu는 User가 접속할 수 있는 방(2개)의 Pannel을 ScrollView를 활용해 만들었다. Pannel에는 방의 이름, 참가자 수, Join버튼을 포함한다. 각 방의 Join버튼을 누르면 JoinMenu로 이동한다. 그리고 소켓 통신을 사용하여 서버에 해당 방의 이름(Room 1 혹은 Room 2)과 함께 Join버튼을 누른 유저의 정보(ID, Name, Character)를 보내준다. 정보를 받은 서버는 해당 방의 참가자 모두에게 방에 참가한 유저의 정보(Name, Character)와 Ready값(게임 시작 준비가 된 참가자의 수)을 보내준다. 각 유저는 서버로부터 받은 정보를 배열을 활용해 저장하고 JoinMenu에서 보여주도록 구현하였다. Back 버튼을 클릭할 시 PlayMenu로 이동한다.
JoinMenu는 유저가 참가한 방의 이름, 게임 시작 준비를 한 User의 수, 방에 참가한 각 유저의 Character와 NickName을 보여준다. Start 버튼을 클릭할 시 소켓 통신을 활용하여 서버에 Start버튼을 누른 유저의 정보(ID, bool값)과 방 이름을 보낸다. 정보를 받은 서버는 true인 bool값의 수를 해당 방의 모든 참가자들에게 보내준다. 정보를 받은 유저들은 Ready값이 변하도록 구현하였다. 모든 참가자(5인)들이 Start버튼을 눌러 Ready값이 5가되면 게임 Scene으로 전환하도록 구현할 ""예정이다"". Back 버튼은 PlayMenu로 이동한다. 그리고 소켓통신을 활용하여 서버에 떠난 유저의 정보(ID, Name)를 보내준다. 정보를 받은 서버는 떠난 유저의 bool값을 false로 초기화하고 방에 남은 참가자들에게 변한 방의 정보(참가한 유저, Ready값)을 보내준다. 방에 남은 참가자들이 받은 정보를 다시 배열에 저장하여 보여주도록 구현하여 순서가 뒤죽박죽되지 않도록 구현하였다.
TutorialMenu는 게임의 설명, 조작법, 플레이방법 등을 설명하는 메뉴이다. 스크롤뷰(Scrollrect)를 사용하여 텍스트로 설명하였고 스크롤바를 추가하였다. Back버튼을 누를 시 MainMenu로 돌아간다.
CashShopMenu는 각 캐릭터(7개)의 이미지와 함께 Toggle을 보여준다. Image와 Toggle은 Grid Layout을 사용하여 정렬하였고 Toggle은 Toggle Group을 활용해 1가지만 선택이 되도록 하였다. Toggle을 선택하고 Select버튼을 누르면 DB에 접근하여 User의 케릭터 정보에 저장한다. Back 버튼을 누를 시 PlayMenu로 이동한다. User의 DB에 보유하고 있는 케릭터 정보를 저장해 두고 Buy버튼을 활용하여 케릭터를 구매하는 등 수익화를 할 수 있도록 구현할 예정이다.

github link : https://github.com/qlqlf/UnitySihyung

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# VI Earth의 12주차 프로젝트 진행 사항(서버 관련)

github link : https://github.com/kh6815/unity-nodejs_server/tree/master
