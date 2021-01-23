# Module Bundler와 Transpiler

### Module System

`코드 베이스를 모듈이라는 단위로 분할할 수 있게 만드는 구조`

## Module Bundler

프론트엔드 개발은 모듈단위로 파일을 엮어서 개발하는 방식이 많습니다.

### 발생하는 문제점

> - 수많은 모듈들의 순서를 어떻게 처리할 것인가? (의존성 처리)
> - 모듈이 많아질수록 HTTP 요청이 많아질텐데 이로 인한 오버헤드는 어떻게 해결할 것인가?
> - ES6+ 스펙의 코드를 어떻게 처리할 것인가?

### Module Bundler 역할

각각의 모듈 의존성을 해결하여 하나의 자바스크립트 파일로 만듦과 동시에 ES6+ 스펙을 ES5로 변환까지 해주는 도구입니다. 이미지 압축, 최소화(Minification) 등의 여러가지 기능들도 제공합니다.

### Module Bundler Tool

![webpack](https://cdn.iconscout.com/icon/free/png-256/webpack-2-1174981.png)
![Parcel](https://tech.weperson.com/img/wedev/parcel.jpg)

## Transpiler- 트랜스파일러

특정 언어로 작성된 코드를 비슷한 다른 언어로 변환시키는 도구입니다.

## Transpiling kind

- ES6+의 기능을 ES5 코드로 변환
- 리액트의 JSX를 자바스크립트 코드로 변환시킨다.
- 타입스크립트를 자바스크립트로 변환시킨다.

### Transpiler Tool

![Babel](https://cdn.iconscout.com/icon/free/png-256/babel-282912.png)

**More**

[Link Site](https://engineering.linecorp.com/ko/blog/write-you-a-webpack-for-great-good/)

[Link Site](https://tech.weperson.com/wedev/frontend/bundling-transpiler/#%E1%84%90%E1%85%B3%E1%84%85%E1%85%A6%E1%86%AB%E1%84%89%E1%85%B3%E1%84%91%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AF%E1%84%85%E1%85%A5-transpiler)
