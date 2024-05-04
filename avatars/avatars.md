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