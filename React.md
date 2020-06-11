# React

VirtualDOM - React가 강한 이유

React는 컴포넌트와 함께 동작한다. 컴포넌트는 html을 반환하는 함수

자바스크립트와 html의 조합을 JSX라고 한다.

jsx는 컴포넌트에 정보를 보낼 수 있다. 컴포넌트를 계속해서 반복해서 사용할 수 있다.

함수형 컴포넌트는 렌더링된 값들을 고정시킨다.

**state** 컴포넌트 내부에서 바뀔 수 있는 값을 의미한다. 클래스형 컴포넌트가 지니고 있는 state와 함수형 컴포넌트에서 useState라는 함수를 통해 사용하는 state가 있다.

#### 클래스형 컴포넌트의 state

컴포넌트에 state를 설정할 땐 constructor 메서드를 작성하여 설정한다.

```react
constructor(props) {
	super(props);
    //state의 초기값 설정하기
    this.state = {
        number : 0;
    }
}
```

컴포넌트의 생성자 메서드이다. 클래스형 컴포넌트에서 constructor를 작성할 땐 반드시 super(props)를 호출해 주어야 한다. 이 함수가 호출되면 현재 클래스형 컴포넌트가 상속하고 있는 리액트의 Component 클래스가 지닌 생성자 함수를 호출해 준다.

#### 함수형 컴포넌트의 state

원래는 함수형 컴포넌트에서 state를 사용할 수 없었다. 하지만 useState함수를 사용하여 가능하게 되었다. 

바인딩을 하는 이유는 함수가 호출될 떄 this는 호출부에 따라 결정되므로, 클래스의 임의 메서드가 특정 HTML요소의 이벤트로 등록되는 과정에서 메서드와 this의 관계가 끊어져 버립니다. 임의 메서드가 이벤트로 등록되어도 this를 컴포넌트 자신으로 제대로 가리키기 위해서는 메서드를 this와 비인딩하는 작업이 필요하다. 만약 바인딩하지 않는다면 this가 undefined를 가리키게 된다. 

이 바인딩 작업을 하기 싫으면 Property Initializer Syntax를 사용하여 메서드를 작성하면 된다. 

handleChange(e){...} 이 코드를 handleChange = (e) => {...} 이렇게 작성하면 바인딩을 하지 않아도 된다. 