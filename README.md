# 중학 수학/중학 과학 프로젝트 GitHub Pages

## 중학 수학 프로젝트
- [에라토스테네스의 체로 소수 찾기: Find Prime Numbers using Eratosthenes' sieve](https://mark2021-github.github.io/PrimeNumber/)

## 중학 과학 프로젝트
- [2차원 자유낙하 입자 물리 시뮬레이션: Ball 2D Physics](https://mark2021-github.github.io/Ball2D-Physics/) 



### 에라토스테네스의 체
```

소수는 모든 자연수의 배수를 차례로 제거함으로써 찾아낼 수 있다. 이 방법은 처음 고안한 그리스의 수학자 에라토스테네스(BC273?~192?)의 이름을 따서 '에라토스테네스의 체'라 부른다. 
'체'는 그물구조로 알갱이를 골라내는 도구인데, 2이상의 자연수에서 '2의 배수를 걸러내는 체', '3의 배수를 걸러내는 체', '5의 배수를 걸러내는 체' 등이 계속 겹쳐진 체들이 있고, 소수는 이 모든 체를 통과하고 남은 수라고 말할 수 있다. 

예를 들어 2~100까지의 자연수를 나타내는 배열 n을 일단 모두 true 로 초기화 한다.

 let n = [];
 for (let i = 2; i <= 100; i++) {
    n[i] = true;
  }

특정 수 a의 배수를 걸러내는 체 함수(sieve) 는 배열 n에서 해당 수의 배수는 모두 false로 셋팅해서 걸러낸다. 
예를 들어 100 이하의 2의 배수를 모두 걸러내는 체:  sieve(2, 100)
        200 이하의 3의 배수를 모두 걸러내는 체:  sieve(3, 200)

function sieve(a,lastN) {
  for (let i = 2; i <= lastN / 2; i++) {
    if (a * i <= lastN) n[a * i] = false;
  }
}

다음과 같이 findPrime(100) 을 호출하여 2~100까지의 체 함수로 거른 이후 자연수 n배열안에 아직 true 인 수들이 소수란다. 

function findPrime(lastN){
  // perform eratosthenes' sieve
  for( let i =2; i <= lastN; i++){
    sieve(i,lastN);
  }
}
```

### Ball Physics (2D) - 2차원 공 물리 시뮬레이션: 중력가속도, 탄성, 마찰력, 충돌 벡터 

```
# 물리 현상 
1. 일명 브라질 너트 현상:  서로 다른 크기의 너트(입자)들이 담긴 봉지를 열면 맨 위에 입자의 크기가 젤 큰 브라질 너트들이 있다.  작은 입자들은 다 아래로 ...

```
