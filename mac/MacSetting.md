# mac Setting

## **1. dock 정리**

dock 우클릭 -> dockd에서 제거하여 전부 정리

## **2. brew 설치**

1. `brew.sh` 로 이동하여 homebrew install



```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. 환경변수 설정
`1. 설치 이후` 나오는 명령어 복사 후 붙여 넣기

```
echo `eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/username/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

3. 설치 확인

`brew` 명령어로 brew 설치 확인


> Application 설치에는 `--cask` 옵션을 사용한다.

> homebrew로 설치할 수 있는 앱이 무엇인지 알고 싶다면?
>> `brew.sh' 웹사이트에서 검색


## **3. 터미널 셋팅 `brew install --cask iterms`**

1. Preference -> Theme -> Minimal
2. Preference -> profile -> Sessions -> Status bar enabled

> Iterm2coloschemes 에서 색깔 변경 가능
 

## **4. oh my zsh 설치**


`https://ohmyz.sh/` 에 접속해서 아래 코드를 붙여 넣는다.
```
$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

git master로 권한이 변경 된다, 이때

`https://github.com/romkatv/powerlevel10k` 에 접속,
installation -> zsh -> 값을 복사한다


```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

```
Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in ~/.zshrc.
```

### 4-1. vsc로 터미널 환경변수 파일 열기

`code ~/zshrc` 으로 변경 파일 연다음,
해당 값을 `ZSH_THEME="powerlevel10k/powerlevel10k"` 으로 변경



## **5. brew로 개발 언어 파일 설치**

```
brew install python go pipenv nvm gh
```

* application이 아니므로 `--cask` 옵션 사용하지 않음
* nvm : 노드 버전 매니저
* gh : git CLI 

----

### 1. NVM

### **주의!!**
nvm 설치 후 export 명령어를 .zshrc 파일에 추가해야 nvm 명령어 사용 가능

`nvm ls-remote` 설치가 가능한 모든 node.js의 버전을 보여줌

`nvm use ${version}`
`nvm use default`
해당 명령어로 명령어 분기가 가능

### 2. gh

> gh auth login


### 3. rosetta

```
/usr/sbin/softwareupdate --install-rosetta --agree-to-license
```














