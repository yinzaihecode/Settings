1. `brew install openjdk@11`

2. 
```
For the system Java wrappers to find this JDK, symlink it with
  sudo ln -sfn /opt/homebrew/opt/openjdk@11/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk

openjdk@11 is keg-only, which means it was not symlinked into /opt/homebrew,
because this is an alternate version of another formula.

If you need to have openjdk@11 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/openjdk@11/bin:$PATH"' >> ~/.zshrc

For compilers to find openjdk@11 you may need to set:
  export CPPFLAGS="-I/opt/homebrew/opt/openjdk@11/include"
```

2-1.
`  sudo ln -sfn /opt/homebrew/opt/openjdk@11/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk`

2-2.
`  echo 'export PATH="/opt/homebrew/opt/openjdk@11/bin:$PATH"' >> ~/.zshrc`

2-3.
`  export CPPFLAGS="-I/opt/homebrew/opt/openjdk@11/include"`

----
# path settings

`~/.zshrc` 에 아래 경로 추가.


> 경로 주의!
```
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_192.jdk/Contents/Home

export PATH=${PATH}:$JAVA_HOME/bin

```

`export JAVA_HOME=/Library/Java/JavaVirtualMachines/openjdk-11.jdk/Contents/Home`

`export PATH=${PATH}:$JAVA_HOME/bin`

<!-- path가 아이텀2랑 꼬이지 않게.. 주의할것 (oh-my-zsh) -->

# inteliJ에서.
> set up SDK (detected) => 해당경로 선택.

----

