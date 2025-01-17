# If/Else

##### if 및 else 문은 Solidity에서 조건부 논리를 구현하는 데 사용됩니다.
#### if 문:
```solidity
if (조건) {
    // 조건이 참일 때 실행되는 코드
}
```
#### if-else 문:
```solidity
if (조건) {
    // 조건이 참일 때 실행되는 코드
} else {
    // 조건이 거짓일 때 실행되는 코드
}
```
#### else if 문:
``` solidity
if (조건1) {
    // 조건1이 참일 때 실행되는 코드
} else if (조건2) {
    // 조건2가 참일 때 실행되는 코드
} else {
    // 위의 모든 조건이 거짓일 때 실행되는 코드
}
```
<br><br>
## 예제 코드
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.24;

contract IfElse {
    function foo(uint256 x) public pure returns (uint256) {
        if (x < 10) {
            return 0;
        } else if (x < 20) {
            return 1;
        } else {
            return 2;
        }
    }

    function ternary(uint256 _x) public pure returns (uint256) {
        // if (_x < 10) {
        //     return 1;
        // }
        // return 2;

        // shorthand way to write if / else statement
        // the "?" operator is called the ternary operator
        return _x < 10 ? 1 : 2;
    }
}
```

IfElse 계약에는 두 개의 함수가 포함되어 있습니다: foo 함수와 ternary 함수. 각각의 함수는 특정 조건에 따라 값을 반환합니다.<br>

#### foo 함수
``` solidity
function foo(uint256 x) public pure returns (uint256) {
    if (x < 10) {
        return 0;
    } else if (x < 20) {
        return 1;
    } else {
        return 2;
    }
}
```
이 함수는 x라는 정수형(uint256) 입력값을 받으며 함수의 반환값은 uint256 타입입니다.
조건에 따라 다른 값을 반환합니다:
  1. x가 10보다 작으면 0을 반환합니다.
  2. x가 10보다 크거나 같고 20보다 작으면 1을 반환합니다.
  3. x가 20보다 크거나 같으면 2를 반환합니다.<br>

#### ternary 함수
```solidity
function ternary(uint256 _x) public pure returns (uint256) {
    // if (_x < 10) {
    //     return 1;
    // }
    // return 2;

    // shorthand way to write if / else statement
    // the "?" operator is called the ternary operator
    return _x < 10 ? 1 : 2;
}
```
이 함수는 _x라는 정수형(uint256) 입력값을 받으며 함수의 반환값은 마찬가지로 uint256 타입입니다.<br>
이 코드에서는 삼항 연산자(ternary operator)를 사용하여 주석 처리된 동일한 논리의 코드보다 간결하게 작성했습니다.
삼항 연산자는 ?와 :를 사용하여 if-else 문을 축약하여 작성하는 방식입니다.<br>
코드의 조건문은 _x < 10 조건이 참이면 1을 반환하고, 거짓이면 2를 반환합니다.
<br><br>
## Remix에서 실습
1. Remix에서 새로운 solidity 파일 생성해서 예제 코드를 복사 붙여넣기 합니다.
2. 예제 코드를 compile 후 deploy합니다.
3. 아래 버튼들이 제대로 동작하는지 확인합니다.<br>
<img src="https://github.com/Joon2000/Solidity-modules/blob/main/images/if-else/If%3Aelse%20button.png" width="250px" height="300px" title="if/else" alt="if/else"></img><br/>
