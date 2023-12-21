
# useEffect

# useEffect(()=>{},[])

# useEffect(()=>{},[]) --> 배열이 비어있을 경우에는 component가 실행될때 처음 한번만 실행된다.
![image](https://github.com/sinchangun/react/assets/145514301/3d3d3f4f-e768-4a6a-ad4f-c9e872c8004f)

# useEffect(()=>{},[products]) ==> component가 실행될때 처음 한번 실행된후 products 의 값이 바뀔때마다 실행된다
![image](https://github.com/sinchangun/react/assets/145514301/cd7adc07-ad49-41dd-8e63-56311e2aa460)

# useEffect(()=>{},[products,count]) ==> component가 실행될때 처음 한번 실행된후 products 또는 count 의 값이 하나라도 바뀔때마다 실행된다 두개다 바껴도 한번만 실행

# useEffect가 종료되는 시점에 데이터가 변경된다.
![image](https://github.com/sinchangun/react/assets/145514301/6a0f3870-4a2f-482a-b88b-68e07b97ed19)

