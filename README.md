# Goal

스마트 컨트랙트를 사용하는 dApp을 개발하기 전에

스마트 컨트랙트를 사용하지 않은

미니 이더리움 월렛을 만들어보자.

이더리움의 잔액 확인 및 이더를 송금하는 Mist의 기능을

html페이지에서 작동되게 만들어 보는게 목적이다.

---

# Pre Work

우선 자신이 사용하는

이더리움 클라이언트로 Network를 실행시킨다.

(필자는 geth를 사용한다.) 

실행시킨 후 [wallet.html](https://github.com/Solidity-Project/Mini-Wallet/blob/master/wallet.html)의 Line 11의 경로 값을 

수정해준 후 실행시키면 된다.

---

# Key Point

[wallet.html](https://github.com/Solidity-Project/Mini-Wallet/blob/master/wallet.html)의 Line 28

지속적인 변화가 필요하다면 

web3.eth.filter('latest').watch(function() { refreshBalance();});

과 같은 Code를 사용한다.

---

# Problem

function send()을 보면

web3.eth.sendTransaction 함수를 사용하여 송신을 한다.

그런데 console에서 실행시켰을 땐 

송신 Tx을 생성 후 mining을 해야지 Tx이 성사된다.

그렇기 때문에 web에서 송신을 보냈을 땐 

Tx이 성사되지 않는다.

해결법으로는 

Network에서 지속적으로 mining을 시키던가,

지속적인 mining이 싫다면

web에서 송신을 한 후 console에서 mining을 실행시켜야 한다.

---

# The Solidity Contract-Oriented Programming Language
[![Join the chat at https://gitter.im/ethereum/solidity](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/ethereum/solidity?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) [![Build Status](https://travis-ci.org/ethereum/solidity.svg?branch=develop)](https://travis-ci.org/ethereum/solidity)

---

## Useful links
To get started you can find an introduction to the language in the [Solidity documentation](https://solidity.readthedocs.org). In the documentation, you can find [code examples](https://solidity.readthedocs.io/en/latest/solidity-by-example.html) as well as [a reference](https://solidity.readthedocs.io/en/latest/solidity-in-depth.html) of the syntax and details on how to write smart contracts.

You can start using [Solidity in your browser](https://ethereum.github.io/browser-solidity/) with no need to download or compile anything.

The changelog for this project can be found [here](https://github.com/ethereum/solidity/blob/develop/Changelog.md).

Solidity is still under development. So please do not hesitate and open an [issue in GitHub](https://github.com/ethereum/solidity/issues) if you encounter anything strange.

---

## Building
See the [Solidity documentation](https://solidity.readthedocs.io/en/latest/installing-solidity.html#building-from-source) for build instructions.

---

## How to Contribute
Please see our contribution guidelines in [the Solidity documentation](https://solidity.readthedocs.io/en/latest/contributing.html).

Any contributions are welcome!
