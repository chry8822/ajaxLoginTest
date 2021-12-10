# ajaxLoginTest 

 <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=HTML5&logoColor=white"/></a> 
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white"/></a>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=JavaScript&logoColor=white"/></a>

*  ajax 로 데이터를 불러와서 로그인창 만들기
*  로그인 아이디: chrys 비밀번호: 1234
*  [실행 링크](https://chry8822.github.io/ajaxLoginTest/ajax%EC%8B%A4%EC%8A%B5%EA%B3%BC%EC%A0%9C.html)

<br>


## 실습목적

<br>

* ajax 와 jQuery 를 사용해서 데이터를 불러와서 로그인 창 만들면서 ajax 의 실행과정과 이해 하기 
* jQuery 를 적절히 사용해서 자바스크립트로만 했을때보다 더 간단한 코드로 작성하고 이해해보기

<br>

## 과정

<br>

* 불러올 json 데이터를 github에 저장소를 하나 만들고 업로드 해준다. (ajax 연결시 데이터가 들어간 주소가 필요해서)
* 마크업과 스타일을 해주고 자바스크립트와 jQuery 코딩하기 
      * 로그인 버튼을 클릭했을때 아이디와 비밀번호번호 각각의 입력값을 벨류로 들어오게 변수로 할당하고 스트링으로 받을수있게 만든다.
      * ajax로 처음에 업로드한 제이슨 파일 불러오기 (git hub에서 raw 해서 주소 복사.)  
      * ajax로 데이터를 불러온 코드
      
* <pre>
                
      $('#btn_data').click(function() {
     $.ajax({경로, 동기화 여부, 성공하면 할 일})
     $.ajax({url:'경로', async: true, success:function(result){}})
    $.ajax({
        url:'https://raw.githubusercontent.com/paullabkorea/10000hour/main/index.html', 
        async: true, 
        success:function(result){
            $("#data").html(result);
         }
     });
  });      

 </pre> 
 
   * 데이터를 잘 불러왔는지 console.log 로 확인하고 잘 나왔으면 success: 뒤에 콜백함수에 그뒤에 필요한 동작을 넣어준다.
   * 불러온 데이터를 제이슨 파일 형식으로 변수에 할당하고 아이디 비밀번호를 검사하는 코드도 넣어준다.
   *  <pre>
       let data = userdata.find(user => user.id === id && user.pw === pw);  // 제이슨 데이터에서  id 와 pw 가 사용자가 입력한 id 와 qw 와 일치하는지 확인.    
        </pre>
   * 로그인 성공과 실패시에 보여줄 화면을 if문으로 만들어주고 어떤식으로 보여준건지 추가로 스타일이나 동작등을 추가해준다. (나는 모달추가)

<br>

### 끝

<br>

* 아주 간단하게 실습한 과정이지만 자바스크립트 시작한지 10일정도 되고 진도가 아주 빠르게 나가고 있는거처럼 느껴져서 매일 하는 실습들이 너무 새롭고 어렵다..
* ajax 와 jQuery 를 사용해서 간단하고 빠르게 로그인 페이지를 만들수있다는 점이 흥미로웠다 물론 아주 아주 간단하고 실제로는 쓰일수 없겠지만 작동되는게 눈에 보이니까 어려웠지만 작은거지만 해냈다라는 느낌을 받았다. 


-----------------------------------------------------------------------------------------------
  


