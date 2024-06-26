# 테킷 프론트엔드 스쿨 10기 첫 번째 과제
## HTML
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Avartars</title>
  <link rel="stylesheet" href="./avatars.css">
</head>
```
1. <code>title</code> 태그를 사용하여 웹 페이지의 제목을 설정
2. <code>link</code> 태그를 사용하여 css 파일 연결

```html
<body>
  <div class="container">
    <!-- 여자 아바타 -->
    <div id="female_row">
      <div id="face_1">
        <div class="status_off"></div>
        <img src="../images/face1.jpg" alt="얼굴 1" />
      </div>
      <div id="face_2">
        <div class="status_on"></div>
        <img src="../images/face2.jpg" alt="얼굴 2" />
      </div>
      <div id="face_3">
        <div class="status_off"></div>
        <img src="../images/face3.jpg" alt="얼굴 3" />
      </div>
      <div id="face_4">
        <div class="status_on"></div>
        <img src="../images/face4.jpg" alt="얼굴 4" />
      </div>
    </div>

    <!-- 남자 아바타 -->
    <div id="male_row">
      <div id="face_5">
        <div class="status_on"></div>
        <img src="../images/face5.jpg" alt="얼굴 5" />
      </div>
      <div id="face_6">
        <div class="status_on"></div>
        <img src="../images/face6.jpg" alt="얼굴 6" />
      </div>
      <div id="face_7">
        <div class="status_off"></div>
        <img src="../images/face7.jpg" alt="얼굴 7" />
      </div>
      <div id="face_8">
        <div class="status_off"></div>
        <img src="../images/face8.jpg" alt="얼굴 8" />
      </div>
    </div>
  </div>
</body>
```
1. <code>container</code> 클래스를 생성하여 전체 영역 설정
2. 남자 아바타와 여자 아바타를 따로 관리하기 위해 각각 <code>male_row</code>, <code>female_row</code> id 값을 가지는 <code>div</code> 태그를 생성
3. 성별 태그 안에 각 아바타를 생성하기 위해 <code>face_$</code>의 id 값을 가지는<code>div</code> 태그를 생성
4. 각 아바타 태그 안에 <code>img</code> 태그로 이미지 파일을 불러오고, 아바타의 상태 정보를 제공하기 위해 <code>status_on</code>과 <code>status_off</code> 클래스 태그를 생성
---
## CSS
```css
img {
  width: 64px;
  height: 64px;
  border-radius: 70%;
  margin: 10px;
}
```
1.  이미지 크기를 64px x 64px로 설정
2.  이미지를 원 모양으로 만들기 위해 <code>border-radius</code> 속성 사용
3.  이미지 간 간격을 20px로 설정하기 위해 <code>margin</code> 속성을 이용해 각 이미지마다 10px 부여

```css
body {
  margin: 0;
}

.container {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column-reverse;
  align-items: center;
  justify-content: center;
}
```
1. <code>container</code> 클래스를 화면의 전체 영역으로 설정하기 위해 <code>width</code> 와 <code>height</code> 속성 값을 뷰포트 길이로 설정
2. <code>body</code>의 <code>margin</code> 때문에 스크롤이 생기기 때문에 스크롤을 제거하기 위해 <code>margin</code>값을 0으로 설정
3. 남자 아바타와 여자 아바타의 줄을 바꾸기 위해 <code>display</code> 속성의 값을 <code>flex</code>로 설정하고, <code>flex-direction</code> 속성 값을 <code>column-reverse</code>로 설정
4. <code>container</code> 클래스를 화면 가운데에 위치하기 위해 <code>align-items</code> 속성 값을 <code>center</code>로 설정하여 수직 정렬, <code>justify-content</code> 속성 값을 <code>center</code>로 설정하여 수평 정렬함

```css
.status_off {
  position: absolute;
  border: 3px solid white;
  background-color: #DBDBDB;
  width:20px;
  height:20px;
  border-radius: 70%;
  margin-left: 55px;
  margin-top: 55px;
}

.status_on {
  position: absolute;
  border: 3px solid white;
  background-color: #4CFE88;
  width:20px;
  height:20px;
  border-radius: 70%;
  margin-left: 55px;
  margin-top: 55px;
}
```
1. 아바타 이미지와 아바타 활성화 상태바를 겹친 상태로 표현하기 위해 <code>position</code> 속성 값으로 <code>absolute</code>를 사용 
2. 활성화 상태바 테두리를 꾸미기 위해 <code>border</code> 속성을 사용
3. 각 활성화 상태바의 색상을 지정하기 위해 <code>background-color</code> 속성 사용
4. 활성화 상태바의 크기를 지정하기 위해 <code>width</code> & <code>height</code> 속성 사용
5. 활성화 상태바를 원 모양으로 만들기 위해 <code>border-radius</code> 속성 사용
6. 활성화 상태바의 위치를 조정하기 위해 <code>margin-left</code> & <code>margin-top</code> 속성 사용