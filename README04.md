# react에서는 데이터를 변할수있는 값이며 값이 변할때마다 UI를 변경해 달라고 react에게 알려야한다.그럴때 사용하는것이 useState()이다.

```
const [ num, setNum ] = useState(0) 
이 데이터를 변할수 있는값 ==> num
num을 변하게 하는 함수 ==> setNum 함수를 이용하여 num을 변경한다.
useState(0)의 0의 num의 초기값
```
![image](https://github.com/sinchangun/react/assets/145514301/751c73c2-ae5c-498d-b0fc-09279eeca689)

![image](https://github.com/sinchangun/react/assets/145514301/0f76cab4-464d-4cda-af67-54060e43bc71)

![image](https://github.com/sinchangun/react/assets/145514301/9b4ceb96-7ecf-4b17-a237-ecc35194ded5)

# 구조분해
```
import React from "react";

const Profile = ({img,name,title,isNew}) => {

  /* const img = props.img;
  const title = props.tite;
  const name = props.name; */

  //구조분해 destructure
  // const {img,name,title,isNew} = props;

  // props를 이용해서 사용해도되지만 프로파일자체에넣어서
  // 사용해도된다.

  return (
    <div className="profile">
      <img src={img} alt="이미지" />
      {isNew? <span className="new">신입</span>:""}
      <h2>{name}</h2>
      <p>{title}</p>
    </div>
  );
};

export default Profile;
```

![image](https://github.com/sinchangun/react/assets/145514301/62ca7865-9037-4f4e-bdf0-32b91d41a776)

```
import { useState } from "react";
import "./App.css";


function App() {
  let counter = 0;
  console.log(useState)

  /* const num = useState(0)[0];
  const setNum = useState(0)[1]; 
  아래처럼 적어주면된다.
  */

  const [num,setNum] =useState(0);
  //0은 매개변수 num의 state의 초기값이 0이다.
  //[c초기값인 0 ,초기값을 변화시키는 함수]
  //useState 라는 함수를 통해 react에게 값이 변했음을 알려주는방법
  //usestate는 react가 제공하는 react hook
  //state를 바꾸면 UI를 다시 랜더링한다.

  const increase = function(){
    counter = counter + 1;
    console.log(counter)
    console.log("num :" + num);
    // counter는 0에서 변하지않고 num은 계속 늘어난다.
  setNum(num + 1)
  }
  return (
    <>
      <div>{`num = ${num}`}</div>
      <div>{`counter = ${counter}`}</div>
      <button onClick={increase}>클릭</button>
    </>
  );
}

export default App;
```
