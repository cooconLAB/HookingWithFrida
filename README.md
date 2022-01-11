## FRIDA&REVERSE

<br/>

타 부서의 요청으로 스크래핑 모듈 개발을 위해 스크립트를 분석하다보면, 암호화 로직이 스크립트가 아닌 네이티브 앱에 포함되어 있는 경우가 종종 있습니다. 이 경우 암호화 분석을 위해 스크립트가 아닌 네이티브 앱의 분석이 필요합니다.

> ###### [네이티브앱: 운영체제 혹은 플랫폼에서 제공하는 SDK(Software Development Kit)를 기반으로 개발된 애플리케이션]
<br/>

쿠콘연구소 핵심기술연구부에서는 네이티브 앱 분석을 위해 API Monitor(http://www.rohitab.com/apimonitor)를 주로 사용했으나 WindowsOS 뿐 아니라 MacOS, 모바일 네이티브 앱 등에 대한 기관 암호화 분석 요청이 추가 접수되면서 다양한 플랫폼의 네이티브 앱을 분석할 수 있는 도구의 필요성을 느꼈습니다.

## Frida

Frida(https://frida.re/)는 동적으로 네이티브 앱을 분석하고 API를 추적할 수 있는 분석 도구입니다. Frida는 Windows, OSX, AOS, iOS, Linux 등 다양한 플랫폼의 네이티브 앱을 분석할 때 유용합니다. 이 글에서 Frida가 무엇인지 살펴보고 플랫폼 별 네이티브 앱 분석 방법과 Frida를 지원하는 추가 확장 프로그램을 소개하겠습니다.

<br/>

## Frida란,
**oleavr**(Twitter: @fridadotre)가 개발한 **DBI(Dynamic Binary Instrumentation**) 프레임워크로 스크립트와 함께 사용하여 실행 중인 프로그램 동작을 모니터링, 수정 기록할 수 있습니다.

instrumentation*|
:---|
앱이 실행 중인 상태에서 해당 프로세스를 추적, 분석, 디버깅하는 도구로서, 프로그램에 코드를 삽입해 정보를 수집하는 기법|

Frida는 파이썬 라이브러리와 명령어로 구성되어 있고, JS Injection 을 이용하여 Windows, OSX, AOS, iO, Linux 등 기반의 네이티브 앱에 대해 후킹을 돕는 파이썬 라이브러리 입니다.




# Windows 환경에서 Frida를 이용해 무언가를 해보기
