# Hueflix
📝개요

• 프로젝트 명: HueFlix

• 일정: 2023년 12월 4일 ~ 2023년 12월 22일

• 개발 목적: 영화를 좋아하는 사용자들에게 다양한 정보를 제공하기 위한 웹 사이트 제작

• 개발 환경

· Server: Apache-tomcat-9.0.0

· Java EE: Eclipse (version 2023-06)

· Database: Oracle SQL developer

· Language: Java, Jsp, HTML, CSS, JavaScript, SQL, Spring Legacy, mybatis

· Framework: Spring Tool suite 3.9.1


📝내용

• 팀원 역할

· 공통: 웹사이트 UI 기획 및 구현, ERD 설계

· 신민하: 영화정보 구현(영화 API 활용), 게시판 UI/UX 구현

· 신수인: 메인 홈페이지 UI 및 로그인/회원가입 구현, 회원정보 수정 구현, 권한별 기능 구현

· 임지선: 상영예정작 API를 활용하여 정보 구현, 메인 UI/UX 기능 구현, 영화상세정보 메뉴 기능 구현

· 이도민: 공지사항 게시판 CRUD 구현, 댓글 구현, 영화정보 UI 구현

· 심기훈: 영화정보의 평점 및 댓글 구현, 영화정보 UI/UX 구현, 공지사항 CRUD 구현

· 김보성: 영화정보 UI 및 개발, 유지보수, 영화정보 UI/UX 구현

· 박다진솔: 검색페이지 구현, 검색결과에서 영화 상세정보 이동 구현

• 구현 기능

• DB ERD 설계
![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/69da1075-31bf-45ae-b4ec-1cb1553c8440)

📝구현기능

⁘ 메인 홈페이지

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/1efb1929-2674-4256-86f6-331fb09861c4)

• 설명

· 영화를 슬라이드로 배치되어 있는 페이지입니다. (Swiper 라이브러리 사용)

· 영화DB는 TMDB 사이트의 API입니다.

· JavaScript Ajax함수를 사용하여 TMDB API의 데이터를 요청하였음.

· API에서 반환한 JSON형식의 데이터를 받아와 처리하였음.


⁘ 회원가입, 로그인

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/38204dae-1a16-4aca-85d2-008bb61e9ecb)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/730258b0-2596-484a-8918-c7854e50826b)

• 설명

· 사이트를 이용하기 위한 회원가입과 로그인 화면.

· 회원가입은 유효성 검사를 거쳐 진행(Spring Security)

⁘ 정보 수정(1)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/a18935ea-1e76-4ef0-acd0-59b77c51a1ff)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/fefbb6d8-61df-41c0-a8e1-42829878468a)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/8983f372-63e7-407c-a04b-be67553adf52)

• 설명

· 닉네임, 비밀번호를 변경할 수 있는 페이지.

· 유효하지 않은 비밀번호를 입력했을 경우 수정할 수 없도록 구현

⁘ 메뉴-현재상영작, 개봉 예정작

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/df971d11-4d83-4558-a8c9-b41199699e84)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/a90cc382-44b0-4786-a910-8678b3d007a2)

• 설명

· TMDB API key를 통해 현재상영중인 최신 영화정보를 받아와 표시

· 영화 포스터를 클릭하면 해당 영화상세정보 이동

⁘ 게시판(일반 로그인 상태)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/8c579ab6-7d4b-4261-9f02-2ea182e6b1cb)

• 설명

· 게시판 읽기와 키워드 검색이 가능한 게시판.

· 1페이지에 게시글 10개가 출력되도록 구현(페이지네이션)

⁘ 게시판(관리자 로그인 상태)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/630e2e01-5ceb-464d-baa4-a6f4c98e252e)

• 설명

· 게시판 작성, 키워드 검색이 가능한 게시판

· 제목을 누르면 해당 읽기 페이지로 이동

⁘ 영화 상세정보(줄거리, 출연, 영상/포토, 평점/댓글)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/c1ea224d-763b-4cf7-808a-6ed05ee40f9c)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/8e62fc32-549a-43b2-a888-57065caf0c0e)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/e63b4244-a434-4ecb-87c3-16c03bd77eca)

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/2d4840de-9822-473f-a340-2a21cbb40bc8)

• 설명

· 특정 영화 아이디 값을 활용하여 API를 호출하며 이를 통해 해당 영화의 줄거리, 출연, 영상/포토, 평점/댓글을 표시하는 페이지

· 사용자의 평점 및 댓글은 댓글 작성시 별 모양 버튼을 누르면 평점을 추가하고 영화 관련된 내용을 평가할 수 있음.

· 관리자 권한을 가진 아이디는 사용자의 댓글을 삭제할 수 있음.

· 일반 사용자 권한을 가진 아이디는 자신이 작성한 댓글만 삭제할 수 있음.

⁘ 영화, 영화인 검색

![image](https://github.com/Parkdajinsol/Hueflix/assets/148019092/8407aa53-338b-4d11-a8c1-8aef43544c42)

• 설명

· 검색창의 입력문자열을 검색 API를 통해 각 영화, 영화인을 검색할 수 있음.

· 검색결과에 출력되는 영화 포스터를 클릭하면 해당 영화상세정보로 이동

