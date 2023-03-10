# 참고사이트

-

# Node

- express
- NestJs

# React

- NextJs

- MVVM 모델에 따름

  - Model View View Model
  - <Model> --- <View Model> --- <View>

  - model: ajax로 가져온 데이터
  - view model : vuejs
  - view: html

# 설치

- 다운로드 방법
- CDN 사용하는 방법
- 라이브러리 임포트 : <script src="https://unpkg.com/vue@3"></script>
- view 정의
  <div id="app">{{message}}</div>
  - view 정의 이후에 스크립트를 달아줘야함

  ```html
  <script>
    const { createApp } = Vue; //구조분해할당
    createApp({
      data() {
        //data에 function(){} ES6문법으로 인해 data()
        return {
          message: "Hello Vue",
        };
      },
    }).mount("#app"); //app을 mount시킨다.
  </script>
  ```

# Vue 문법

1. 변수에 있는 데이터를 html에 표시 -> {{ 변수명 }}

2. html내에 text를 표시시키기

- v-text
- v-html
- 태그의 속성부분에 출력하기
- <태그명 v-text='변수명'></>

3. 태그의 속성을 표시하기
   v-bind
   <태그명 v-bind:속성명="변수명"></태그명>
   속성명 : class, id, name, style, href, src...

   - 생략버전
     <태그명 : 속성명="변수명"></태그명>
     <태그명 :style="{스타일속성명:변수명}"></태그명>

- 1,2,3번은 한 방향 바인딩 , 4번은 양방향 바인딩

4. html의 변경사항을 vue에 적용

- vue의 변경사항을 html에 적용
  - 양방향 바인딩
- v-model -> 뷰의 지시자
- 사용가능한 태그 : <input>, <textarea>, <select>
  <input v-model="변수먕" />

5. v-on

- html이벤트 처리하기
  <태그명 v-on:이벤트명="메서드명"></태그명> === <태그명 @이벤트명="메서드명"></태그명>

- 수식자

6. v-if : 조건부 표시하기 : 조건부 렌더링

- v-if
- v-else
- v-else-if
  <태그명 v-if="조건"></태그명>
  <태그명 v-else></태그명>
  <태그명 v-else-if="조건"></태그명>

7. 리스트 렌더링

- v-for
- <태그명 v-for=""></태그명>

8. computed

9. watch
