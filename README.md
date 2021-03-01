## University_timetable

Timetable by semester of university

---

### 결과물

### - Responsive

#### dropdown button으로 시간표 선택

![목록](https://user-images.githubusercontent.com/63100352/109503248-5eb1be00-7add-11eb-9998-c4bc5f1fd2cc.PNG)
<br />
<br />

<img src="https://user-images.githubusercontent.com/63100352/109503010-185c5f00-7add-11eb-85b8-808e343c3f8c.jpg" height="600px" >
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://user-images.githubusercontent.com/63100352/109503006-172b3200-7add-11eb-9567-569c34f52aa4.jpg" height="600px">
<br />
<br />

<img src="https://user-images.githubusercontent.com/63100352/109503018-1b574f80-7add-11eb-916c-a6cb598038f0.jpg" height="600px">

---

### 개발사항

### dropdown menu

```js
function menu() {
  let click = document.querySelector(".drop-content");

  if (click.style.display === "none") {
    // display = "block"으로 click한 요소 나타내기
    click.style.display = "block";
  } else {
    // display = "none"으로 숨기기
    click.style.display = "none";
  }
}
```

### display:none과 visibility:hidden 차이

display:none은 해당 요소의 공간도 존재하지 않게되며 아예 삭제된 것처럼 보임.
레이아웃에 영향 X

visibility:hidden은 해당 요소가 보이지 않을 뿐 요소가 차지하는 공간은 그대로 유지됨. 레이아웃에 영향 O

<br />

### Grid

#### grid-template-rows는 행(row)의 배치, grid-template-columns는 열(column)의 배치

```css
.pm12 {
  grid-row: 5/6; /* 5번째 행부터 6번째 행까지 */
  grid-column: 1/2; /* 1번째 열부터 2번째 열까지 */
}
```

#### grid cell 사이의 간격 설정

```css
.timetable {
  column-gap: 10px; /* column의 간격을 10px로  */
  row-gap: 10px; /* row의 간격을 10px로 */
}
```

#### 30분 단위로 시간표 구성

```css
.grid-template-rows: 100px 100px 50px 50px …
  /* 30분 단위로 구성할 해당 시간을 100px에서 50px 50px로 쪼갬 */ .pm7 {
  grid-row: 15/17; /* 반으로 쪼갠 시간은 행을 두개 차지*/
  grid-column: 1/2;
}

.pm8 {
  grid-row: 17/18; /* 100px의 경우 */
  grid-column: 1/2;
}
```

---

### Additional development items

- react로 시간표 웹 만들어보기
- 리팩토링
