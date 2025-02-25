# HTML-CSS-Javascript
웹페이지 만들기
visual studio code에서 index.html 파일을 생성한다. 
!+tab키를 누르면 html 자동구조가 완성된다 (에밋)

lang부분을 ko로 바꿔주고, 타이틀 부분을 적절한 이름으로 바꿔준다.
body부분에 div.wrap을 쓰고 tab키를 눌러주면 class wrap을 갖고있는 div탭을 만들어준다. (에밋)

이제 웹페이지에 삽입하는 이미지에 대한 부분이다. 
https://developers.google.com/fonts/docs/material_icons?hl=ko 이사이트에 들어가서 구글폰트를 이용해 사용 부분의 링크를 head와프로젝트 사이에 붙여넣기하면 된다.
구글 material icons에서 사용하고자 하는 아이콘을 클릭하고, inserting 부분의 코드를 div부분 아래에 넣고, <h1>,</h1>으로 감싸면 된다. 이작업은 이 아이콘 부분이 웹페이지에서 중요한 부분을 차지한다는 것을 알려주는 것이다.

이제 밑에 들어갈 글씨에 대한 부분이다. 두줄로 이루어져있고, 윗줄은 굵은 글씨, 밑에줄은 평범한 글씨로 만들거다.
p#dynamic.lg-text를 쓰고, 탭키를 누르면된다.(에밋)
두번째 태그는 p.sm-text쓰고, 탭키를 눌러준다.
들어갈 텍스트는 </p>앞부분에 삽입하면 된다.

이제부터는 css를 통해 스타일을 지정하면 된다.
웹페이지 만들기 폴더에 style.css파일을 추가한다.
html파일 헤드 마지막 부분에 <link href="style.css" rel="stylesheet"> 를 추가하면 style.css폴더와 html파일은 연결되게 된다.
일단 아무 효과 없는 css파일은 이렇다
*{
    margin:0;
    padding:0;
    box-sizing: border-box; <=이부분은 텍스트들 사이의 마진을 초기화해놓는 부분

}
body{
    background-color: yellow; <=이부분은 배경색상
}
.wrap{
    position: absolute;
    top:50%;
    left:50%;
    transform: translate(-50%,-50%);
    color:black;
    text-align: center; <=글씨부분 가운데 정렬
}

.material-icons{
    font-size:10rem; 
    
}

.lg-text{
    font-size:2rem;
    font-weight:bold;
    margin-bottom: 5px;
}

.sm-text{
    font-size:1.5rem;
}


글자 뒤에 깜빡거리는 커서 만들기
#dynamic::after {
    content: "";  /* 가상 요소는 기본적으로 아무 내용도 없음 */
    display: block;  /* 블록 요소로 설정 (세로로 길게 만들기 위해) */
    position: absolute;  /* 부모 요소를 기준으로 위치 조정: 항상 끝에 위치하도 */
    top: 0;  /* 부모 요소의 맨 위에 위치 */
    right: 0;  /* 부모 요소의 맨 오른쪽에 위치 */
    width: 4px;  /* 커서의 두께 */
    height: 100%;  /* 부모 요소의 높이와 동일 */
    background-color: black;  /* 커서 색상을 검정색으로 설정 */
} ::after라는 가상요소 사용
여기까지는 커서를 생성했지만, 깜빡이는 효과는 아직 못 넣었다. 
깜빡이는 애니메이션 효과는 javascript를 사용해야한다.


폴더에 main.js파일을 추가하고, html파일과 연동한다. body마지막 부분에 <script src="main.js"></script>를 추가하면 된다.
완성된 사진은 이렇다。
커서가 깜빡이고、 계속 글씨를 제거하고 쓰여진다。

<img width="525" alt="image" src="https://github.com/user-attachments/assets/58b9ae75-14ae-49e3-9da7-3cba42887db2" />


웹페이지 주소： file:///C:/Users/%EC%A0%95%EC%97%B0%EC%9A%B1/OneDrive/%EB%B0%94%ED%83%95%20%ED%99%94%EB%A9%B4/%EC%9B%B9%ED%8E%98%EC%9D%B4%EC%A7%80%EB%A7%8C%EB%93%A4%EA%B8%B0/index.html

