# clone_netflix

## 자료 준비

- Netflix 로고 : 구글링
- 버튼 아이콘 : [부트스트랩 웹 사이트](https://getbootstrap.kr/)(https://getbootstrap.kr/)
- 배경 콘텐츠 썸네일, 제목 : [넷플릭스 홈페이지](https://www.netflix.com/) 개발자도구 탭
- 기타 영화 및 드라마 썸네일 : [넷플릭스 홈페이지](https://www.netflix.com/)

## 헤더(Header)

- 로고
    - 좌측 상단 배치
        
        ![로고.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/399ba89e-0df4-44cb-9433-956ca321de1b/%EB%A1%9C%EA%B3%A0.png)
        
- 메뉴 탭
    - 중단 배치 : 왼쪽 정렬
        
        ![메뉴 탭.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fe389f07-49ef-434e-ac8e-b81863ef0aaf/%EB%A9%94%EB%89%B4_%ED%83%AD.png)
        
    - 헤더 배경 색상 검정 → 투명 그라데이션 지정
        
        ![헤더 배경 그라데이션.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a1daf128-82c1-41ba-bb51-ed07b12e1768/%ED%97%A4%EB%8D%94_%EB%B0%B0%EA%B2%BD_%EA%B7%B8%EB%9D%BC%EB%8D%B0%EC%9D%B4%EC%85%98.png)
        
    - 마우스 `**hover**`시 `**투명도 변경**`되도록 지정
        
        ![메뉴 탭 hover1.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6731a691-6dcb-4aca-bc2a-dae675ad7ae7/%EB%A9%94%EB%89%B4_%ED%83%AD_hover1.png)
        
        ![메뉴 탭 hover2.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/80bbb5e7-e880-4c22-8e82-0450a9b4553b/%EB%A9%94%EB%89%B4_%ED%83%AD_hover2.png)
        
    - `**창 크기 줄였을 때**` 메뉴 탭 없어지고 `**‘▼메뉴’ 로 변경**` : `**미디어 쿼리**` 활용
        
        ![메뉴 탭 미디어쿼리.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8ef988ca-1bfe-4aa5-b654-5a1d7b47c1f5/%EB%A9%94%EB%89%B4_%ED%83%AD_%EB%AF%B8%EB%94%94%EC%96%B4%EC%BF%BC%EB%A6%AC.png)
        
- 유저 정보, 알람, 키즈, 검색 탭
    - 우측 상단 배치
        
        ![유저 및 검색 탭.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/773b5f3e-dfb9-40ad-b207-b96739ba9a31/%EC%9C%A0%EC%A0%80_%EB%B0%8F_%EA%B2%80%EC%83%89_%ED%83%AD.png)
        
    

## 배경(Background)

- 전체 배경은 <body>탭의 background-image로 지정
    
    ![백그라운드 이미지, 텍스트이미지, 재생 버튼, 상세정보 버튼.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/16a4bd7d-2da2-4d8b-943a-9cfcc7b4d2a5/%EB%B0%B1%EA%B7%B8%EB%9D%BC%EC%9A%B4%EB%93%9C_%EC%9D%B4%EB%AF%B8%EC%A7%80_%ED%85%8D%EC%8A%A4%ED%8A%B8%EC%9D%B4%EB%AF%B8%EC%A7%80_%EC%9E%AC%EC%83%9D_%EB%B2%84%ED%8A%BC_%EC%83%81%EC%84%B8%EC%A0%95%EB%B3%B4_%EB%B2%84%ED%8A%BC.png)
    
    - ‘국민사형투표’ 텍스트 이미지 및 재생 버튼, 상세 정보 버튼은 따로 탭을 만들어 줌
    - 재생 버튼, 상세 정보 버튼 `**hover시**` 버튼의 `**background만 투명**`해지도록 지정
        
        ![백그라운드 재생버튼 hover1.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4a1c7ad8-185c-459b-bd3d-7a3630dd442c/%EB%B0%B1%EA%B7%B8%EB%9D%BC%EC%9A%B4%EB%93%9C_%EC%9E%AC%EC%83%9D%EB%B2%84%ED%8A%BC_hover1.png)
        
        ![백그라운드 재생버튼 hover2.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4cfe2187-9978-492b-a0a4-a93987486e02/%EB%B0%B1%EA%B7%B8%EB%9D%BC%EC%9A%B4%EB%93%9C_%EC%9E%AC%EC%83%9D%EB%B2%84%ED%8A%BC_hover2.png)
        
        ![백그라운드 상세정보 버튼 hover1.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e0caa038-7e51-48eb-a9b0-5c37c52b411e/%EB%B0%B1%EA%B7%B8%EB%9D%BC%EC%9A%B4%EB%93%9C_%EC%83%81%EC%84%B8%EC%A0%95%EB%B3%B4_%EB%B2%84%ED%8A%BC_hover1.png)
        
        ![백그라운드 상세정보 버튼 hover2.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f7603ab1-a756-4c4f-8dac-0d4c7c614b7b/%EB%B0%B1%EA%B7%B8%EB%9D%BC%EC%9A%B4%EB%93%9C_%EC%83%81%EC%84%B8%EC%A0%95%EB%B3%B4_%EB%B2%84%ED%8A%BC_hover2.png)
        

## 컨텐츠(Contents)

- 썸네일 담는 컨텐츠 박스에 `**display: flexbox**` 지정 : 가로로 담을 수 있도록 설정
    
    ![컨텐츠 부분.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d6b13bbf-cde6-4af1-a78f-14f22571e76c/%EC%BB%A8%ED%85%90%EC%B8%A0_%EB%B6%80%EB%B6%84.png)
    
- 썸네일 담는 컨텐츠 박스에 `**overflow-x: auto**` 지정 : 넘어가는 부분 생기면 스크롤로 넘기기 가능
    
    ![컨텐츠 썸네일 flexbox overflow_auto 지정.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/84666efa-196b-4ac2-bc68-d0d404eb88dd/%EC%BB%A8%ED%85%90%EC%B8%A0_%EC%8D%B8%EB%84%A4%EC%9D%BC_flexbox_overflow_auto_%EC%A7%80%EC%A0%95.png)
    
    - `**.new-content-thumb::-webkit-scrollbar { display: none; }**` 옵션으로 어울리지 않는 `**스크롤 바 삭제**` (방향키로 이동 가능)
- **썸네일 이미지에 hover시 확대 및 컨텐츠 상세 정보 표시**
    
    ![썸네일 hover 컨텐츠 정보탭.PNG](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6dff8f28-c7ab-4838-93cf-06aa303101f4/%EC%8D%B8%EB%84%A4%EC%9D%BC_hover_%EC%BB%A8%ED%85%90%EC%B8%A0_%EC%A0%95%EB%B3%B4%ED%83%AD.png)
    
    - `**display: grid**` 이용하여 썸네일 이미지와 상세정보 컨텐츠박스를 **`각 행에 배치`**
    - **`상세정보 컨텐츠 박스`**는 기본 상태를 **`display:none 상태`**로 지정
        
        📌 이 부분에서 `**dsplay: none**` 과 `**opacity**` 변경, `**visiblity: hidden**` 속성 이용, `**animation**` 활용 등 방법으로 구현해봤었는데 각각 문제가 발생.
        
        📌 **`display: none`** : **`transition 적용이 안됨`**
        
        📌 **`opacity`** 변경 : 투명도가 달라질 뿐 **`컨텐츠 박스가 남아있어서`** 투명할 때 컨텐츠 박스 자리에 마우스를 **`hover시 반응`**
        
        📌 **`visiblity: hidden`**속성 이용 : 마찬가지로 **`컨텐츠 박스가 남아있어서`** 컨텐츠 박스 자리에 마우스 **`hover시 반응`**
        
        📌 **`animation`** 활용 **`커서가`** 이미지 박스와 상세정보 박스를 **`왔다갔다 할 때마다 animation이 재생`**
        
    - 썸네일 **`이미지에 hover시`** 상세정보 **`컨텐츠 박스를 diplay:block`** 해 줌
    - **`썸네일과 상세정보의 부모 탭에 hover`**시 **`transform: scale(1.3)`** 지정
        
        📌 **`이미지에 hover시 부모 탭의 스케일 증가`**로 지정했었는데 **`안돼`**서 부모 탭 자체에 hover시 스케일 증가로 처리함!!
        
    - 상세정보 **`컨텐츠 박스 hover시`**에도 **`display:block`** 으로 지정
        
        📌 그렇게 해야지 **`확대 이후 커서를 상세 정보 쪽으로 옮겨도 display:none 상태가 되지 않음!!!`**
