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
