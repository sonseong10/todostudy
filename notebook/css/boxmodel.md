# Box Model

![Box_Model](https://hackernoon.com/hn-images/1*2jZwpWH9XO_QllhEpyGqMA.png)

content: 요소의 실 크기

padding: 컨텐츠의 안쪽 여백

border: 테두리
※ 굵기, 형태, 색상 값이 필요하다.

margin: 컨텐츠의 바깥 여백

+) position: 요소의 위치

속기형(Shorthand)

![Shorthand](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a9733e78-775f-41e4-abfe-8596b14228c0/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210219%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210219T100837Z&X-Amz-Expires=86400&X-Amz-Signature=0ebbf0b040b259c77b2c728183e1a316373fc5294fdf9385343af493ad518e19&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

```css
div {
  padding-top: 10px;
  padding-bottom: 10px;
  padding-left: 20px;
  padding-right: 20px;
}
```

```css
div {
  padding: 10px 20px 10px 20px;
}
div {
  padding: 10px 20px;
}
```

## Box Sizing

```css
div {
  /* border-box, content-box, inherit, initial...
 *	 most use border-box
 */
  box-sizeing: border-box;
}
```

# Box Type

**display: block;**

1. 본인 옆으로 진행을 맊음.
2. width를 부여한 경우 여백은 margin으로 채움.
3. 부모 height 값이 없다면 자식 height의 총 합.

ex) div, h1

![display_block](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/204f6b7b-712c-4f12-aa1f-a5e22aa1a55c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210219%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210219T101023Z&X-Amz-Expires=86400&X-Amz-Signature=4e2e27ad4f7a5298e63463130adb593b24a20344b274422e453868fa363acbe6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

**display: inline;**

1. 필요한 만큼의 너비를 사용.
2. 남은 여백은 이어서 진행.
3. width, height, margin[padding]-top[bottom] 부여 불가

   ex) span, img

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ceb47c05-4ce4-4cf0-a29a-9768940a2d3c/Untitled.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ceb47c05-4ce4-4cf0-a29a-9768940a2d3c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210219%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210219T101056Z&X-Amz-Expires=86400&X-Amz-Signature=208be747165f7b361314a0d332b98316e1f03c04ce71956af0645529a9ec0595&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

**display: inline-block;**

1. inline, block의 장점을 합친 방법
2. 형제요소를 순차적 진행.
3. width, height, margin[padding]-top[bottom] 부여 가능
