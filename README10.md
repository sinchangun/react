
# Json server 사용하기
--> 작은 서버를 만드는것 --> api소통할때 제일 많이 쓰이는 파일타입

![image](https://github.com/sinchangun/react/assets/145514301/476557b6-acfe-4172-a27a-b1e32cf5e849)


1. 터미널에서 실행
```
npm install -g json-server
```

2. 확장명이 .json인 파일을 만든다. 루트에

json서버 실행  --> 기본적으로 3000번에서 시작하는데 react가 3000번을 사용하고있기때문에 다른 포트를 사용해야한다.
```
json-server --watch db.json --port 3004
```

# 혹시 안되면
```
npx json-server --watch db.json --port 3004
```

# 새창을 열고 주소창에 아래내용을 입력하면 넘어가짐
```
http://localhost:3004/products
```
