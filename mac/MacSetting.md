# mac Setting
`https://www.youtube.com/watch?v=B26yiuC5zPM&t=478s`

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

```
 brew install --cask visual-studio-code spotify slack iterm2
```

## **3. 터미널 셋팅 `brew install --cask iterm2`**

1. Preference -> Theme -> Minimal
2. Preference -> profile -> Sessions -> Status bar enabled

> `https://iterm2colorschemes.com/` 에서 색깔 변경 가능
* github dark
`https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/GitHub%20Dark.itermcolors`
1. 해당 파일 다운로드
2. txt 지우고 더블클릭 -> add
3. preferences -> profile -> color
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

2. `~/.zshrc` 파일에 
1. 기존 코드를 주석처리하고,  
2. 아래 코드를 추가
 `ZSH_THEME="powerlevel10k/powerlevel10k"`

3. `source ~/.zshrc` 명령으로 변경한 파일 불러들이기.

4. `yyyy-2242-2322-n1yy`

### **4-1. vsc로 터미널 환경변수 파일 열기**

`code ~/zshrc` 으로 변경 파일 연다음,
해당 값을 `ZSH_THEME="powerlevel10k/powerlevel10k"` 으로 변경


----

## **5. brew로 개발 언어 파일 설치**

`brew.sh`


```
brew install python pipenv nvm gh
```

* application이 아니므로 `--cask` 옵션 사용하지 않음
* nvm : 노드 버전 매니저
* gh : git CLI 

----

# 1. NVM

1. `brew install nvm`
2. notice

```sh
You should create NVM's working directory if it doesn't exist:

  mkdir ~/.nvm

Add the following to ~/.zshrc or your desired shell
configuration file:

  export NVM_DIR="$HOME/.nvm"
  [ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion

You can set $NVM_DIR to any location, but leaving it unchanged from
/opt/homebrew/opt/nvm will destroy any nvm-installed Node installations
upon upgrade/reinstall.
```

3. `code ~/.zshrc`
파일에 아래 내용 복사해서 붙여넣기.
```sh
 export NVM_DIR="$HOME/.nvm"
  [ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
```



### **주의!!**
> **nvm 설치 후 export 명령어를 .zshrc 파일에 추가해야 nvm 명령어 사용 가능**

* `nvm ls-remote` 
> 설치가 가능한 모든 node.js의 버전을 보여줌

1. nvm 17.x 설치
> `nvm install 17.8.0`

2. nvm 16.x 설치
> `nvm install 16.14.2`

3. `node -v` 명령어로 현재 버전 확인.

4. 다른 버전으로 스위치 

* `nvm use 16.14.2`
* `nvm use default`
> 해당 명령어로 명령어 분기가 가능

### 2. gh

`gh auth login`

> github cli, 한번 기기 연결해두면 편함. 엔터 4번 후 코드 8자리 뜨면 깃허브 홈페이지에 입력.


# 2. VSC
## 2-1.  extension
1. git lens
2. material icon theme
3. eslint
4. community material theme

## 2-2 . vsc -> settings
intergrated Font Family
> MesloLGS NF

----
Terminal › Integrated: Font Family
Controls the font family of the terminal, this defaults to Editor: Font Family's value.

`MesloLGS NF`
=> iterm2 의 폰트랑 똑같이 맞춰주면 적용됨..
```json
"terminal.integrated.fontFamily": "MesloLGS NF"
```



### 3. rosetta
> M1 -> Intel

```
/usr/sbin/softwareupdate --install-rosetta --agree-to-license
```














