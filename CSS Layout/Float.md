# Float
## CSS 원칙I

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>> 사진

### 모든 요소는 네보(박스모델)이고, 위에서부터 아래로, 왼쪽에서 오른쪽으로 쌓인다. (좌측 상단에 배치)
### 어떤 요소를 감싸는 형태로 배치는? 혹은 좌/우측에 배치는?

## Float
- 박스를 왼쪽 혹은 오른쪽으로 이동시켜 텍스트를 포함 Inline 요소들이 주변을 Wrapping 하도록 함
- 요소가 Normal Flow를 벗어나도록 함

## Float 속성
- none : 기본값
- left : 요소를 왼쪽으로 띄움
- right : 요소를 오른쪽으로 띄움

## Float 예시I
```
<body>
  <div> class="box left">float left</div>
  <p>lorem300 자동 완성으로 길~게</p>
</body>
```
```
.box {
    width: 150px;
    height: 150px;
    border 1px solid black;
    background-color: crimson;
    color: white;
    margin-right: 30px;
}

.left {
    float: left;
}
```