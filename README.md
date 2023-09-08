# clone_netflix

## 자료 준비

- Netflix 로고 : 구글링
- 버튼 아이콘 : [부트스트랩 웹 사이트](https://getbootstrap.kr/)(https://getbootstrap.kr/)
- 배경 콘텐츠 썸네일, 제목 : [넷플릭스 홈페이지](https://www.netflix.com/) 개발자도구 탭
- 기타 영화 및 드라마 썸네일 : [넷플릭스 홈페이지](https://www.netflix.com/)

## 헤더(Header)

- 로고
    - 좌측 상단 배치
      
        ![로고 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/acaaa19b-5799-49e2-8d15-7034271a30db)

        
        
- 메뉴 탭
    - 중단 배치 : 왼쪽 정렬
        
       ![메뉴 탭 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/df9be7a5-fa47-4ef4-8cb1-60c073784409)

        
    - 헤더 배경 색상 검정 → 투명 그라데이션 지정
        
       ![헤더 배경 그라데이션](https://github.com/Jiiker/clone_netflix/assets/100774811/a8afc36b-e1a6-4764-b5d3-bc999f7c8665)

        
    - 마우스 `**hover**`시 `**투명도 변경**`되도록 지정
        
        ![메뉴 탭 hover1 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/0f113f90-1108-4150-85de-19b8b8a4f7e8)

        ![메뉴 탭 hover2 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/80caa1ee-7729-4c3b-a3d4-509ff8c5fb59)

        
        
    - `**창 크기 줄였을 때**` 메뉴 탭 없어지고 `**‘▼메뉴’ 로 변경**` : `**미디어 쿼리**` 활용
        
        ![메뉴 탭 미디어쿼리 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/5511b61d-e2a8-4ff1-b569-d134b332b306)

        
- 유저 정보, 알람, 키즈, 검색 탭
    - 우측 상단 배치
        
        ![유저 및 검색 탭 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/1608972f-14de-4f3b-9591-516b98353173)

        
    

## 배경(Background)

- 전체 배경은 <body>탭의 background-image로 지정
    
    ![백그라운드 이미지, 텍스트이미지, 재생 버튼, 상세정보 버튼 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/e4a0027d-5081-4ec5-802c-86e599a4f2ce)

    
    - ‘국민사형투표’ 텍스트 이미지 및 재생 버튼, 상세 정보 버튼은 따로 탭을 만들어 줌
    - 재생 버튼, 상세 정보 버튼 `**hover시**` 버튼의 `**background만 투명**`해지도록 지정
        
        ![백그라운드 재생버튼 hover1 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/c706ea55-b602-4f02-b5c3-9b5632c816cd)

        ![백그라운드 재생버튼 hover2 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/d90858b4-7874-4445-8453-fca41d1263ca)

        ![백그라운드 상세정보 버튼 hover1 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/009e9a84-1690-47a9-88a9-3bc79645cd55)

        ![백그라운드 상세정보 버튼 hover2 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/62b62a16-7fe2-41ed-a1fb-21d4e400d667)

        
        
        

## 컨텐츠(Contents)

- 썸네일 담는 컨텐츠 박스에 `**display: flexbox**` 지정 : 가로로 담을 수 있도록 설정
    
    ![컨텐츠 부분 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/8c76cda3-11cd-4c12-ae94-f0a9800a2988)

    
- 썸네일 담는 컨텐츠 박스에 `**overflow-x: auto**` 지정 : 넘어가는 부분 생기면 스크롤로 넘기기 가능
    
    ![컨텐츠 썸네일 flexbox overflow_auto 지정 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/9a49a922-6275-4b2b-9dfd-0e78e638e7ff)

    
    - `**.new-content-thumb::-webkit-scrollbar { display: none; }**` 옵션으로 어울리지 않는 `**스크롤 바 삭제**` (방향키로 이동 가능)
- **썸네일 이미지에 hover시 확대 및 컨텐츠 상세 정보 표시**
    
    ![썸네일 hover 컨텐츠 정보탭 PNG](https://github.com/Jiiker/clone_netflix/assets/100774811/39a10a68-d2c2-48e1-8774-242d7d27c490)

    
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
