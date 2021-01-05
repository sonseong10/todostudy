# Fix float

## Cause of occurrence

![float 사전 의미](https://media.vlpt.us/images/im_hyeonji/post/7e85c3d5-04b6-4bfd-87f5-948ff33b8c77/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-06-23%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%2010.39.39.png)

자식요소가 `float`속성을 가지게 된다면 부모, 형제요소는 자식의 높이를 감지할 수 없기 때문에를 인식하지 못하게 되지만 안에 텍스트(혹은 인라인 요소들)는 float된 요소가 어디있는지 알 수 있어서 종종 레이아웃이 망가지게 된다.

빠른 설명을 위해 기본 스타일은 style태그를 사용합니다.

```html
<head>
  <style>
    .parents {
      margin: 0 auto;
      width: 400px;
      background-color: #666;
    }
    .children {
      height: 200px;
      width: 200px;
      line-height: 200px;
      text-align: center;
      color: #fff;
      font-size: 24px;
      font-weight: 700;
    }
    .red {
      background-color: #ff3232;
      float: right;
    }
    .blue {
      background-color: #1277ff;
    }
  </style>
</head>
<body>
  <div class="parents">
    <div class="children red">iteam</div>
    <div class="children blue">iteam</div>
  </div>
</body>
```

## way1

**부모 엘리먼트에 float 적용**
