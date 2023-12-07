#JSX문법

https://react.dev/learn#writing-markup-with-jsx

- 컴퍼넌트의 return() 에서는 반드시 하나의 태그로 쌓여 있어야한다.
- 태그대신 <> </> 사용할수도있다.
- class명을 className=" 클래스이름 " 으로 사용한다.
- javaScript 코드를 JSX 문법안에서 사용해야할때는 {javaScript 코드} 형식으로 사용해야한다.

- {} 문법을 사용하지 않으면 변수가 아니라 문자가된다.
- 인라인스타일로 css를 작성할때 ==> {{}} 중괄호가 2개 들어가는데 밖의 중괄호는 javaScript를 사용하고있다고 생각해서 필요하고 안의 중괄호는 객체라는 의미에서 중괄호다.
- <div style={{ width:"300px",height:"200px" }}>추가하기</div>

```
import logo from "./logo.svg";
import "./App.css";

function App() {
  const name = "강아지";
  return (
      <>
        <div className="App">
        <p> {`${name} 시작하기`} </p>
        </div>
        <div style={{ width:"300px",height:"200px" }}>추가하기</div>
      </>
  );
}

export default App;
```
