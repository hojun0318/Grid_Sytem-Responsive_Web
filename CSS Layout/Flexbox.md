# Flexbox
## CSS Flexible Box Layout

<img width="392" alt="1" src="https://user-images.githubusercontent.com/104968672/182560716-c3db3913-b8a5-416b-bf23-702e86153e13.png">

- 행과 열 형태로 아이템들을 배치하는 1차원 레이아웃 모델
- 축
 - main axis (메인 축)
 - cross axis (교차 축)
- 구성 요소
    - Flex Container (부모 요소)
    - Flex Item (자식 요소)

## Flexbox 축
- Flex-Direction: row

<img width="300" alt="2" src="https://user-images.githubusercontent.com/104968672/182560841-f21a3b72-8f17-43b4-b184-341f59fee0aa.PNG">

## Flexbox 구성 요소
- Flex Container (부모 요소)
    - Flexbox 레이아웃을 형성하는 가장 기본적인 모델
    - Flex Item들이 놓여있는 영역
    - Display 속성을 Flex 혹은 Inline-Flex로 지정
- Flex Item (자식 요소)
    - 컨테이너에 속해 있는 컨텐츠(박스)

## CSS Flexible Box Layout
- 왜 Flexbox를 사용해야 할까?
    - 이전까지 Normal Flow를 벗어나는 수단은 Float 혹은 Position
- 하기 어려웠던 것?
    - (수동 값 부여 없이)
        - 1 수직 정렬
        - 2 아이템의 너비와 높이 혹은 간격을 동일하게 배치

## Flexbox 시작
```
.flex-container {
    display: flex;
}
```
- 부모 요소에 display: flex 혹은 inline-flex

## Flex 속성
- 배치 설정
    - flex-direction
    - flex-wrap
- 공간 나누기
    - justify-content (main axis)
    - align-content (cross axis)
- 정렬
    - align-items (모든 아이템을 cross axis 기준으로)
    - align-self (개별 아이템)

## Flex 속성 : flex-direction
- Main axis 기준 방향 설정
- 역방향의 경우 HTML 태그 선언 순서와 시각적으로 다르니 유의 (웹 접근성 영향)
    - 1 row
    - 2 row-reverse
    - 3 column
    - 4 column-reverse

<img width="678" alt="3" src="https://user-images.githubusercontent.com/104968672/182561136-2a8a2a4c-4132-428f-b810-cc2fab4fed57.PNG">

## Flex 속성 : flex-wrap
- 아이템이 컨테이너를 벗어나는 경우 해당 영역 내에 배치되도록 설정
- 즉, 기본적으로 컨테이너 영역을 벗어나지 않도록 함

<img width="299" alt="4" src="https://user-images.githubusercontent.com/104968672/182561301-2c836ea7-8e95-4c5a-a248-b0d975bc8edb.PNG">

## Flex 속성 : flex-direction & flex-wrap
- flex-direction: Main axis의 방향을 설정
- flex-wrap : 요소들이 강제로 한 줄에 배치되게 할 것인 지 여부 결정
    - nowrap (기본값) : 한 줄에 배치
    - wrap : 넘치면 그 다음 줄로 배치
- flex-flow
    - flex-direction과 flex-wrap의 Shorthand
    - flex_direction과 flex-wrap에 대한 설정 값을 차례로 작성
    - 예시) flex-flow: row nowrap;

## Flex 속성 : justify-content
- Main axis를 기준으로 공간 배분
    - 1 flex-start
    - 2 flex-end
    - 3 center
    - 4 space-between
    - 5 space-around
    - 6 space-evenly

<img width="651" alt="5" src="https://user-images.githubusercontent.com/104968672/182561474-abc816f7-4dbc-4304-8f4f-de16635bc984.PNG">

## Flex 속성 : align-content
- Cross axis를 기준으로 공간 배분 (아이템이 한 줄로 배치되는 경우 확인할 수 없음)
    - 1 flex-start
    - 2 flex-end
    - 3 center
    - 4 space-between
    - 5 space-around
    - 6 space-evenly

<img width="499" alt="6" src="https://user-images.githubusercontent.com/104968672/182561524-5e65b13e-7bc8-4836-9de2-62466be6c12f.PNG">

## Flex 속성 : justify-content & align-content
- 공간 배분
    - flex-start (기본값) : 아이템들을 axis 시작점으로
    - flex-end : 아이템들을 axis 끝 쪽으로
    - center : 아이템들을 axis 중앙으로
    - space-between : 아이템 사이의 간격을 균일하게 분배
    - space-around : 아이템을 둘러싼 영역을 균일하게 분배 (가질 수 있는 영역을 반으로 나눠서 양쪽에)
    - space-evenly : 전체 영역에서 아이템 간 간격을 균일하게 분배

## Flex 속성 : align-items
- 모든 아이템을 Cross axis를 기준으로 정렬
    - 1 stretch
    - 2 flex-start
    - 3 flex-end
    - 4 center
    - 5 baseline

<img width="635" alt="7" src="https://user-images.githubusercontent.com/104968672/182561583-7c04871f-bdee-4e9f-89ab-53d0cfd4e3e3.png">

## Flex 속성 : align-self
- 개별 아이템을 Cross axis 기준으로 정렬
    **주의! 해당 속성은 컨테이너에 적용하는 것이 아니라 개별 아이템에 적용**
    - 1 stretch
    - 2 flex-start
    - 3 flex-end
    - 4 center

<img width="641" alt="8" src="https://user-images.githubusercontent.com/104968672/182561642-92af91d6-68a4-4f18-80b6-4e3d96bc826a.PNG">

## Flex 속성 : align-items & align-self
- Cross axis를 중심으로
    - stretch(기본값) : 컨테이너를 가득 채움
    - flex-start : 위
    - flex-end : 아래
    - center : 가운데
    - baseline : 텍스트 baseline에 기준선을 맞춤

## Flex에 적용하는 속성
- 기타 속성
    - flex-grow : 남은 영역을 아이템에 분배
    - order : 배치 순서

<img width="455" alt="9" src="https://user-images.githubusercontent.com/104968672/182561709-2a6abacc-322e-4d21-9c9c-137419bd4027.PNG">

## 활용 레이아웃 - 수직 수편 가운데 정렬
```
/* 방법 1
컨테이너 설정
*/

.container {
    display: flex;
    justify-content: center;
    align-items: center;
}

/* 방법 2
아이템 설정
*/

.container {
    display: flex;
}
.item {
    margin: auto;
}
```

<img width="215" alt="10" src="https://user-images.githubusercontent.com/104968672/182561765-b8022dc9-6f2c-4a0e-a7ab-a47ea80711fc.PNG">

## 활용 레이아웃 - 카드 배치
```
#layout_03 {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: space-around;
    align-content: space-around;
}
```

<img width="167" alt="11" src="https://user-images.githubusercontent.com/104968672/182561831-21091034-82e0-42f0-80b7-a3add3f11986.PNG">

```
#layout_03 {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-around;
    align-content: space-around;
}
```

<img width="163" alt="12" src="https://user-images.githubusercontent.com/104968672/182561866-ee33d280-ec2c-47ce-aced-59f8a79ca051.PNG">