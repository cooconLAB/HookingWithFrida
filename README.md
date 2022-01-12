# Windows
> ##### FRIDA 설치 및 Python 설치 안내

## Install Python 3.7.0
 #### https://www.python.org/downloads/release/python-370/
> ###### 3.7.0 버전이 2022-01-12 기준 최신 버전 FRIDA와 가장 호환이 잘되는 파이썬 버전

![image](https://user-images.githubusercontent.com/97210927/149086943-65715a27-233e-41e0-bc78-31506c420366.png)
> ##### 설치 완료

## Upgrade pip

```Bash
  python -m pip install --upgrade pip
```

`※ SSLCertVerificationError`:

> ###### 신뢰할 수 있는 사이트 옵션을 추가합니다.

```Bash
  python -m pip --trusted-host pypi.org --trusted-host files.pythonhosted.org install --upgrade pip
```

# Install FRIDA

```Bash
  pip install frida
  pip install frida-tools
```

`※ SSLCertVerificationError`:

> ###### 신뢰할 수 있는 사이트 옵션을 추가합니다.

```Bash
  pip --trusted-host pypi.org --trusted-host files.pythonhosted.org install frida
  pip --trusted-host pypi.org --trusted-host files.pythonhosted.org install frida-tools
```

## Check FRIDA

```Bash
  C:\User>frida --version
  15.1.14
```

`※ SyntaxError: Non-UTF-8 code starting with:`

> ###### 파이썬 설치 경로에 한글이 포함되어 있는지 확인 후 제거

<br/>

