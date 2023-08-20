# Optic Yellow
안녕하세요! <br>
테니스 코트 대여 & 운동용품 경매 서비스를 주제로 진행한 <br>
팀 프로젝트 입니다.

<hr>

### 사용 기술
<ul>
    <li>언어 : Java(JDK1.6), HTML/CSS, Javascript</li>
    <li>IDE : Spring Framework 3.1.1, Sql Developer</li>
    <li>DBMS : Oracle 11g</li>
    <li>서버 : Apache Tomcat 9.0, AWS EC2</li>
    <li>API, 라이브러리 : Kakao, OpenWeather, IQAir, jQuery, Spring Security</li>
</ul>

<hr>

### 프로젝트 기간
<ul>
    <li>2023.06.12 ~ 2023.07.21 (6W)</li>
</ul>

<hr>

### 담당 기능

#### 1. 회원가입
    <img src="https://github.com/tjwnsz/optic/assets/121169416/d4f3254e-6b4c-43ff-8dc3-1583b071c773">
    ![m_insert2](https://github.com/tjwnsz/optic/assets/121169416/c0e30e35-49d3-4e7b-aefb-fed83be39163)
<ul>
    <li>비회원 상태로 프로필 영역 클릭 시 회원가입 및 로그인으로 유도</li>
    <li>ID 중복체크, 정보 미입력 등의 유효성 체크 구현</li>
    <li>Spring Security의 BCryptPasswordEncoder 클래스를 이용해서<br>
  회원가입 시 입력한 비밀번호를 DB에 랜덤문자열(60글자)로 저장</li>
</ul>

#### 2. 로그인
    ![m_login1](https://github.com/tjwnsz/optic/assets/121169416/6364a76e-e0a0-43cf-9825-f5e0642a8de1)
<ul>
    <li>아이디 기억하기 체크 > 쿠키에 저장하여 다음 로그인 시 입력받은 아이디 정보를 불러옴</li>
    <li>비밀번호  찾기 > 랜덤문자열 생성하여 회원가입 시 입력한 메일로 전송</li>
    <li>로그인 성공 > 로그아웃, 마이페이지 이용 가능</li>
</ul>

#### 3. 접근 ROLE 인증/인가 로직
    ![role1](https://github.com/tjwnsz/optic/assets/121169416/0fb6d89f-98ab-4fde-b0f7-171b1855df7e)
<ul>
    <li>회원 가입 시 ROLE을 부여함 -> 일반회원 = “USER”, 관리자 = “ADMIN”</li>
    <li>로그인 없이 쿼리 스트링을 수기로 작성해서 이용할 수 없도록 설계함<br>
    Interceptor를 활용하여, 접근 시 로그인이 필요한 URL은<br>
    부여된 ROLE로 인증 후 접근이 가능함, 인증 실패 시 로그인 화면으로 이동</li>
</ul>

#### 4. 카카오페이 결제
    ![kakaopay1](https://github.com/tjwnsz/optic/assets/121169416/38941172-1d94-4645-b5b9-70778212337d)
<ul>
    <li>카카오페이 API 사용, 결제요청 > 결제승인요청 > 결제완료 구현</li>
    <li>매치 신청, 코트 예약 결제 시 활용</li>
</ul>

#### 5. 커뮤니티 게시판 CRUD
    ![board1](https://github.com/tjwnsz/optic/assets/121169416/06b05425-1061-4850-90ca-b6de260a791a)
    ![board2](https://github.com/tjwnsz/optic/assets/121169416/5c9bc424-1829-4f77-9905-820ad2fa5520)
<ul>
    <li>Summernote 에디터를 사용하여 게시글 등록 시 양식, 이미지, 영상 업로드 가능</li>
    <li>커뮤니티 게시글 조회, 추천, 댓글(댓글 추천) 기능 구현</li>
    <li>게시글/댓글 작성자 본인만 수정or삭제 가능</li>
</ul>

#### 6. 관리자 > 회원관리
    ![admin1](https://github.com/tjwnsz/optic/assets/121169416/7f58bf9e-9e14-4df7-b3c3-37f0cc2005cf)
<ul>
    <li>관리자로 로그인 후 프로필 영역 클릭 > 관리자 항목 노출</li>
    <li>회원 관리(회원정보 수정, 예약 내역 확인 등),
    공지사항, 1:1문의 관리 등 사이트 관리 가능</li>
</ul>

#### 감사합니다.
