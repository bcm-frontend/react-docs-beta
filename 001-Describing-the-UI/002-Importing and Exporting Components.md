# Importing and Exporting Components

- 다른 컴포넌트들을 조합해서 새로운 컴포넌트를 만들 수 있다.
- 한 파일 내에 너무 많은 요소를 중첩하는 것보다 찾기 쉽고 재사용성을 위해 분리하는 것이 좋다.

## Exporting and importing a component

1. 컴포넌트를 넣을 JS 파일 생성 후 export
- export 방식 (상세 내용은 [링크](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/export#using_named_exports) 참고)

```jsx
//export default 예시
export default function 컴포넌트명() {
}

//export named 예시
export function 컴포넌트명() {
}
```

- 동일한 파일 내에서만 사용되는 컴포넌트는 export 하지 않고 정의

1. 컴포넌트 import
- import 방식 (상세 내용은 [링크](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/import#importing_defaults) 참고)

```jsx
//import default 예시
import 컴포넌트명 from './파일명.js'

//import named 예시
import {컴포넌트명} from './파일명.js'
```

- from 뒷부분은 ‘./파일명.js’ , ‘./파일명’ 둘 다 사용할 수 있지만 확장자명을 함께 작성하는 것이 ES Modules에 더 가깝다.

**[참고]**
한 파일에서 default export 방식은 하나만 가능하지만, named export 방식으로 작성된 컴포넌트는 여러 개 존재할 수 있다.
