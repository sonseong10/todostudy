# DOCTYPE

Document Type의 약자로, `HTML이 어떤 버전으로 작성되었는지 미리 선언하여 웹브라우저가 내용을 올바로 표시할 수 있도록 해주는 것` 이다. <!DOCTYPE> 으로 선언하는데 이걸 해주지 않으면 호환 모드(quirks mode) 로 동작한다. 호환 모드의 경우 각 브라우저마다 문서를 나타내는 방식이 다르기 때문에 크로스 브라우징 이슈가 훨씬 심해지게 된다.

## DTD(Document Type Definition)

DTD(Document Type Definition)란 문서 형식을 정의해놓은 것으로 DOCTYPE을 명시할 때 사용한다.

즉, HTML 문서가 어떤 문서 형식을 따르는지 DOCTYPE에서 DTD를 지정하는 것이다.

현 시점에선, `HTML5`의 DTD로 DOCTYPE을 명시하는 것이 제일 바람직하다.

```HTML
<!-- HTML5 -->
<!DOCTYPE html>
```

More

- [문서 타입 정의](https://developer.mozilla.org/ko/docs/Glossary/Doctype)
- [Quirks Mode and StandardsMode](https://developer.mozilla.org/en-US/docs/Web/HTML/Quirks_Mode_and_Standards_Mode)
