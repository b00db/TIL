# CSS(Cascading Style Sheets)

### selector / property 두 파트로 구성

```
    selector(id, class, tag name) {
        property-name: value;
        property-name: value;
        property-name: value;
        property-name: value;
        property-name: value;
    }
```

<br>

### HTML과 CSS를 연결하는 방법

- inline : html 문서 내부에서 style을 작성하는 방법 -> 비효율적(html 파일마다 계속 복사-붙여넣기로 작성)
- external : 연결만 하고, style.css 에서 바꾸면 바로 자동으로 모든 html 문서에 적용되는 방법

<br>

### Box Model

- Margin
- Border
- Padding
- Content

<br>

### Display

- Inline : 폭-높이 박스 없이 서로 옆에 붙는 형태(Text)
- Inline-Block : 박스들이 서로 옆에 붙는 형태
- Block: 박스들이 밑에 붙는 형태

<br>

### Position

- static : 디폴트
- fixed : 고정, 어디든 오버랩해서 계속 해당 위치에 고정시키기 위한 방법
- absolute : 포지션 relative에 상대적으로 포지션을 잡는 형태(relative 포지션이 없을 경우, absolute는 문서의 본문 body에 맞춰서 포지션을 잡음)
- relative

<br>

### Display : flex

-> 부모 클래스에만 적용하면 됨

ⅰ. `flex-direction: row` (디폴트) 일 경우 (= inline-block display) <br>
-> justify-content 는 수평으로, align-items 는 수직으로 적용됨

ⅱ. flex-direction: column 일 경우 (= block display) <br>
-> justify-content 는 수직으로, align-items 는 수평으로 적용됨

> 반대!

<br>

- `flex-wrap: wrap` : 폭을 유지하고 밑으로 박스들을 떨어뜨림
- `flex-wrap: no wrap` (디폴트) : 폭은 무시하고 다 줄어드는 것

<br>

- flex-flow (flex-direction + flex-wrap) <br>
  `(예) flex-flow: row wrap`

<br>

### Pseudo Selector, 가상 셀렉터

셀렉터인데 element가 아닌 것. 즉, 태그 이름이나, class, id를 쓰지 않고, 선택하는 방법

<br>

### CSS states

- hover : 그 박스 위에 뭔가 올라가면(hover) 상태가 변함
- active : 박스를 클릭할 때 상태가 변함
- focus : 포커싱 될 때 상태가 변함
- visited

<br>

### Transitions, 트랜지션

우리의 -이름/변경-을 멋있게 보여주는 효과
어떤 state가 바뀔 때 적용 (focus, active, hover 에서 효과적으로 적용)

<br>

### Transformations, 트랜스포메이션

html 문서의 element들을 변경, 모습이 변하는 효과

<br>

### Animations, 애니메이션

state할 필요없이 계속 효과가 발생하기 원할 때 사용

ⅰ. 스테이지가 2개일 때

```
    @Keyframe nameOfAnimation {
        from {
            ...
        }
        to {
            ...
        }
    }
```

ⅱ. 스테이지가 3개일 때

```
    @Keyframe nameOfAnimation {
        0% {
            ...
        }
        50% {
            ...
        }
        100% {
            ...
        }
    }
```

<br>

### Media Query, 미디어 쿼리

모바일-데스크탑 환경에 따라서 반응형 웹 디자인을 할 때 사용 (@media) <br>
브라우저 사이즈를 잡는 것
