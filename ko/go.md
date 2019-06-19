# 이 책에 대하여

## 라이센스

Little Go Book은 Attribution-NonCommercial-ShareAlike 4.0 International license를 따릅니다. 이 책에 값을 지불하지 마세요.

이 책은 복제, 배포, 게시를 자유롭게 할 수 있습니다. 다만, 이 책은 Karl Seguin에게 소유권이 있다는 사실을 당부 드립니다. 상업적 용도로 사용하지 마세요.

라이센스에 대한 전문은 여기서 볼 수 있습니다:

<https://creativecommons.org/licenses/by-nc-sa/4.0/>

## 최신 버전

이 책의 최신 버전은 여기서 제공됩니다:
<https://github.com/karlseguin/the-little-go-book>

# 소개

저는 새로운 언어를 배우는 데 있어 항상 애증의 관계를 유지 했습니다. 한편으로는 언어는 우리가 하는 일에 너무도 근본적이기 때문에 언어의 작은 변화로도 괄목할만한 영향을 미칩니다. 무언가를 클릭할 때 *아하*하는 순간은 당신이 프로그래밍 하는 방법에 대해 지속적으로 영향을 미칠 수 있고 다른 프로그래밍 언어에 대한 기대치를 재정의 할 수도 있습니다. 단점이라면 언어 디자인은 상당히 점진적입니다. 새로운 키워드, 타입 시스템, 코딩 스타일을 배우는 것은 새로운 라이브러리나 커뮤니티, 패러다임을 배우는 것 만큼 정당화 하기 어렵다는 것입니다. 배워야 할 다른 것들과 비교해 보면 새로운 언어를 배운다는 것은 종종 우리 시간을 투자할 가치가 없다고 느껴지기도 합니다.

그렇지만, 우리는 앞으로 전진*해야* 합니다. 다시 말하지만 언어는 우리가 하는 일에 너무도 근본적인 역할을 하므로 우리는 점진적인 단계를 감수할 의지가 있*어야만* 합니다. 변화는 점진적이지만 광범위하며 생상성, 가독성, 성능, 테스트 가능성, 의존성 관리, 에러 처리, 문서화, 프로파일링, 커뮤니티, 표준 라이브러리 등에 영향을 미칩니다. 천개의 상처로 죽음을 말할 수 있는 긍정적인 방법이 있나요?

중요한 의문이 남습니다: **왜 Go 언어인가?** 저의 경우 두 가지 동기가 있습니다. 첫째는 Go언어는 비교적 심플한 표준 라이브러리를 가지는 단순한 언어라는 것입니다. Go 언어의 점직전 특성은 많은 점에서 지난 수십 년 간 각종 언어에 추가되어온 복잡성을 단순화했다는 것입니다. 또 다른 동기는 많은 개발자들에게 기존에 도구 집합(arsenal)을 보완한다는 이유 입니다.

Go는 원래 시스템(예를 들면 운영체제, 장비 드라이버)을 위한 언어로 만들어 졌었고 C, C++ 개발자들을 대상으로 했었습니다. 그런데 Go 팀에 따르면 시스템 개발자가 아니라 애플리케이션 개발자가 Go의 주 사용자가 되었다고 합니다. 저의 경우에도 그렇습니다. 왜냐하면 저는 시스템 개발자로서가 아니라 웹사이트, 서비스, 데스크톱 애플리케이션을 개발자로서 Go가 저수준과 고수준 시스템 애플리케이션 사이에 위치한 시스템 클래스를 위해 필요한 것으로 부각되고 있다고 말씀 드릴 수 있습니다.

아마도 그런 필요성은 메시징, 캐싱, 계산량이 많은 데이터 분석, 명령줄 인터페이스, 로깅이나 모니터링 등의 작업일 수 있습니다. 어떤 레이블로 분류해야 할지 모르겠지만, 제 경력이 쌓여갈 수록 복잡성이 지속적으로 증가하는 하고 수만 준의 동시성을 지원하는 사용자 정의 인프라 타입의 시스템에 대한 필요성이 확실하게 커지고 있습니다. 이런 시스템들 루비나 파이썬 또는 다른 것들(많은 이들이 그렇게 하듯이)로 구축*할 수는* 있지만 (Go로 구축한다면)이런 유형의 시스템들은 강 타입 시스템과 성능 부분에서 잇점을 얻을 수 있습니다. 마찬가지로 (많은 이들이 그러는 것처럼) 웹사이트를 구축하는데 Go를 사용할 수도 있습니다만 많은 이들이 그런 시스템을 위해서는 루비나 노드의 표현력을 더 선호합니다.

Go는 탁월한 분야가 있습니다. 예를 들면, 컴파일 된 Go 프로그램은 동작 시 의존성을 가지지 않습니다. 사용자가 루비나 JVM을 설치했는지 설치했다면 어떤 버전인지 등을 걱정할 필요가 없습니다. 이런 이유로 Go는 명령줄 인터페이스 프로그램과 배포해야 하는 유틸리티 프로그램 타입(예를 들면, 로그 수집기)을 위한 언어로 점차 대중화 되고 있습니다.

Go를 배우는 것은 시간을 효율적으로 사용하는 것임이 분명합니다. Go를 배우거나 마스터링 하는데 오랜 시간을 들일 필요가 없으며, 노력을 통해 실용적인 것을 얻을 수 있을 겁니다.

## 저자 노트

몇 가지 이유로 이 책 쓰는 것을 주저했습니다. 첫 번째 이유는 Go의 문서, 특히
[Effective Go](https://golang.org/doc/effective_go.html)때문입니다. 그 문서는 아주 견실합니다.

다른 이유는 언어에 대한 책을 쓰는 것은 쉽지 않기 때문입니다. Little MongoDB Book을 썼을 때 대부분의 독자들이 관계형 데이터베이스의 기초와 모델링에 대해 이해하고 있다고 가정해도 됐습니다. Little Redis Book을 쓸 때는 키 값 저장소를 사용하는데 익숙하다고 가정했었습니다.

앞서 제시한 단락과 장을 생각해 보면, 그와 같은 가정을 할 수 없다는 것을 알게 된다. 일부는 새로운 개념, 다른 것은 Go가 인터페이스를 가지고 있다는 사실 보다 더 많이는 필요 없다는 정도까지 인터페이스에 대해 이야기 하는데 얼마의 시간이 걸릴까요? 궁극적으로 어떤 부분은 내용이 너무 얕고 어떻부분은 너무 자세한지를 독자가 알려줄 것으로 생각합니다. 이 책의 가격을 생각해 보세요.

# 시작

Go를 조금만 가지고 놀아볼 생각이라면 아무것도 설치 하지 않고 코드를 온라인상에서 실행해 볼 수 있는 [Go Playground](https://play.golang.org/)를 이용합니다. 스택오버플로우나 [Go's discussion forum](https://groups.google.com/forum/#!forum/golang-nuts) 같은 곳에서 도움을 구할 때 코드를 공유 하기 위해서도 이 방법을 사용할 수 있습니다.

Installing Go is straightforward. You can install it from source, but I suggest you use one of the pre-compiled binaries. When you [go to the download page](https://golang.org/dl/), you'll see installers for various platforms. Let's avoid these and learn how to set up Go ourselves. As you'll see, it isn't hard.
Go 설치는 간단합니다. 소스를 통해 설치할 수도 있지만 사전에 컴파일된 바이너리를 사용하는 것을 권장합니다. [다운로드 페이지](https://golang.org/dl/)로 가면 다양한 설치본을 확인할 수 있습니다. 설치 하는 방법은 각자 배우길 바랍니다. 보다 시피 어렵지 않습니다.

간단한 예제를 제외하고 Go는 작업 공간(Workspace) 안에 코드가 있을 때 동작하도록 설계되었습니다. 작업 공간은 `bin`, `pkg`, `src` 서브 폴더를 가지는 폴더 입니다. Go가 독자의 스타일을 따르도록 하고 싶을테지만 그러지 마세요.

보통 저는 제 프로젝트를 `~/code`에 둡니다. 예를 들면 `~/code/blog`는 블로그 입니다. Go의 경우 제 작업 공간은 `~/code/go`이고 Go를 사용하는 블로그는 `~/code/go/src/blog` 가 될 것입니다.

간단히 말하면, 프로젝트 폴더를 두려고 한다면 `src` 하위 폴더를 가지는 `go` 폴더를 만드세요.

## OSX / Linux
플랫폼에 맞는 `tar.gz` 파일을 다운로드 받으세요. OSX의 경우는 `#.#.#` 부분에 Go의 최신 버전인 `go#.#.#.darwin-amd64-osx10.8.tar.gz` 와 같을 것입니다.

파일을 `tar -C /usr/local -xzf go#.#.#.darwin-amd64-osx10.8.tar.gz` 명령을 통해 `/usr/local` 에 압축 해제 하세요.

두 환경 변수를 설정하세요:

  1. `GOPATH` 가 작업 영영을 가리키도록 설정, 필자의 경우는 `$HOME/code/go`.
  2. Go 바이너리 경로를 `PATH`에 추가.

쉘을 통해서 이 두 환경 변수를 설정할 수도 있습니다:

    echo 'export GOPATH=$HOME/code/go' >> $HOME/.profile
    echo 'export PATH=$PATH:/usr/local/go/bin' >> $HOME/.profile

이 환경 변수를 활성화 하려면 쉘을 닫았다가 다시 열거나 `source $HOME/.profile`와 같이 실행합니다.

`go version` 명령을 입력하면 `go version go1.3.3 darwin/amd64`와 유사항 결과를 확인할 수 있을 겁니다.

## Windows
최신 zip파일을 다운로드 받으세요. x64 시스템이라면, `#.#.#` 부분에 최신 Go 버전이 표시된 `go#.#.#.windows-amd64.zip`와 같은 파일입니다.

적당한 위치를 선택해 파일을 압축해제 합니다. `c:\Go` 정도가 적당합니다.

환경 변수 두개를 설정합니다:

  1. `GOPATH` 는 작업 영역을 가리키도록 설정. `c:\users\goku\work\go`와 같은 경로
  2. `c:\Go\bin` 경로를 `PATH` 환경 변수에 추가

환경 변수는 환경설정 패널의 시스템에 고급 탭에서 환경 변수 버튼을 통해 수정 가능합니다. 특정 윈도우 버전의 경우는 이 설정 패널이 시스템 설정 내에 고급 시스템 설정이라는 옵션을 통해 환경 변수 변경을 제공합니다.

명령창을 열고 `go version`을 입력하세요. `go version go1.3.3 darwin/amd64`와 유사항 결과를 확인할 수 있을 겁니다.



# 1장 - 기초

Go는 C 문법과 유사하며 가비지 수집 기능이 있는 컴파일되는 정적 타입 언어입니다. 이게 무슨 뜻일까요?

## 컴파일

컴파일이란 당신이 작성한 소스 코드에서 저수준 언어로 변환하는 과정을 말합니다. 저수준 언어란 어셈블리(Go의 경우)나 기타 중간 단계 언어(Java, C# 등의 경우)를 뜻합니다.

컴파일 되는 시간이 오래 걸리 수도 있기 때문에 컴파일되는 언어로 작업하는 것은 즐겁지 않습니다. 컴파일되기를 몇 분 또는 몇 시간 기다려야 한다면 개발 주기를 빠르게 반복하기 어렵습니다. 컴파일 속도는 Go의 주요 디자인 목표 중 하나 입니다. 인터프리터 언어를 사용해 빠른 피드백 주기를 사용하는 대형 프로젝트를 개발하는 사람에게는 희소식입니다.

컴파일되는 언어는 비교적 더 빨리 실행되고 그 실행 파일은 추가적인 의존성이 없이 동작할 수 있습니다.(적어도 C, C++, Go 처럼 직접 어셈플리어로 컴파일되는 언어의 경우에는)


## 정적 타이핑

정적 타입이라는 의미는 변수는 특정 타입이어야 한다는 의미입니다(int, string, bool, []byte 등등). 변수가 선언될 때 타입을 지정하거나 대부분은 컴파일러가 타입을 추측하도록 함으로써 정적 타입을 지정합니다(곧 예제를 보여드리겠습니다).

정적 타입에 대해 훨씬 많은 이야기가 있지만, 코드를 보며 이해 하는게 더 좋다고 생각합니다. 동적 타입 언어에 익숙하다면 좀 귀찮을 수도 있습니다. 당신이 틀리지는 않지만, 정적 타입은 장점이 있습니다. 특히, 정적 타입이 컴파일과 짝을 이룰 때가 그렇습니다. 이 두 가지는 종종 합쳐집니다. 하나를 가지면 보통 다른 하나를 가지게 되는게 사실입니다.(?) 엄격한 타입 시스템을 사용하면 컴파일러는 단순한 구분 실수 뿐만 아니라 추가적 최적화를 수행할 수 있습니다.

## C 유사 구문

C 유사 구문이 있다고 가정하고 C, C++, Java, Javascript 그리고 C#과 같은 다른 C 유사 구분 언어 사용에 익순하다면 Go에 친숙할 수 있을 것입니다 -- 적어도 겉으로 보기에는요. 예를 들면 `&&`는 논리합로 사용되고 `==`는 동등 비교에 사용되며, `{`와 `}`는 범위의 시작과 끝을 나타내며 배열 인텍스는 0으로 시작한다는 의미입니다.

C 유사 구문은 세미 콜론은 줄의 끝을 의미하며 조건문의 괄호로 나타내는 경향이 있습니다. Go는 우선 순위를 나타낼 때 괄호를 사용하지만 그 외에는 둘다 사용하지 않습니다. 예를 들면 `if` 구문은 다음과 같습니다:

```go
if name == "Leto" {
  print("the spice must flow")
}
```

좀더 복잡한 케이스로, 괄호를 사용하는 예입니다:

```go
if (name == "Goku" && power > 9000) || (name == "gohan" && power < 4000)  {
  print("super Saiyan")
}
```

이 외에도 Go는 C#이나 Java보다 C에 훨씬 더 가깝습니다. 구문만이 아니라 목적면에서도 그렇습니다. 그것은 배워가면서 분명히 알게 될 언어의 단순함과 간결함으로 반영됩니다.

## 가비지 수집

일부 변수는 생성될 때 변수는 쉽게 정의된 수명을 가집니다. 예를 들면 함수의 지역 변수는 함수가 종료될 때 사라집니다. 다른 경우는 적어도 컴파일러에게는 명확하지 않습니다. 예를 들면 함수에서 리턴 된 변수나 다른 객체에 의해 참조되는 변수의 수명을 결정하기는 까다로울 수 있습니다. 가비지 수집이 없다면 개발자가 더이상 변수가 필요 없다고 판단 되는 점에 그런 변수에 연관된 메모리를 해제 해야 합니다. 어떻게요? C에서는 문자 그대로 `free(str)` 로 해제 합니다.

가비지 수집기를 사용하는 언어(예를 들면 Ruby, Python, Java, JavaScript, C#, Go)는 더이상 사용하지 않을 때 이를 추적하고 해제할 수 있습니다. 가비지 수집은 오버 헤드를 추가하지만, 많은 버그를 제거합니다.

## Go 코드 실행

간단한 프로그램을 하나 생성하고 어떻게 컴파일하고 실행하는지 배우면서 우리의 여행을 시작해 봅시다. 선호하는 편집기를 열고 다음 코드를 작성하세요:

```go
package main

func main() {
  println("it's over 9000!")
}
```

`main.go`라는 파일로 저장하세요. 지금은 어디든 저장해도 됩니다. 사소한 예제를 위해서 Go 작업 공간을 사용할 필요는 없습니다.

다음으로 쉘(명령창)을 열고 파일을 저장한 디렉토리로 이동합니다. 제 경우엔 `cd ~/code` 입니다.

마지막으로, 아래와 같이 입력해 프로그램을 실행합니다:

```
go run main.go
```

잘 작동된다면, *it's over 9000!* 라는 문구가 출력됩니다.

그런데 컴파일 단계는 어떻게 된거죠? `go run` 명령은 컴파일을 하고 코드를 실행하는 편리한 명령입니다. 이 명령은 임시 폴더에 프로그램을 빌드 하고 실행한 후 폴더를 정리합니다. 임시 파일의 위치를 보려면 아래와 같이 실행 하면 됩니다:

```
go run --work main.go
```

명시적으로 컴파일 하려면 `go build` 명령을 사용합니다:

```
go build main.go
```

이 명령은 `main` 이라는 실행 파일을 생성할 것입니다. 리눅스나 OSX에서는 실행을 위해서는 점-슬래시를 앞에 붙여주어야 합니다. 그래서 `./main`이라고 입력해야 합니다.

개발하는 동안 `go run` 또는 `go build`를 사용할 수 있습니다. 그렇지만 코드를 배포할 때는 `go build`를 통해 생성한 바이너리를 배포하고 실행하게 될 것입니다.

### Main

방금 작성한 코드는 이해할만 합니다. 함수를 하나 생성 했고 `println` 내중 함수를 이용해 문자열을 출력 했습니다. `go run` 명령이 하나의 함수만 있어서 그것을 실행 했을까요? 아닙니다. Go에서는 프로그램의 진입점은 `main` 패키지 안의 `main` 이라는 이름의 함수여야 합니다.

패키지에 대한 내용은 뒷장에서 좀더 다룹니다. 지금은 Go의 기초를 이해하는데 집중하기 위해 코드를 모두 `main` 패키지에 작성할 것입니다.

원하면 코드를 변경하고 패키지 이름을 바꿀 수도 있습니다. `go run` 명령으로 코드를 실행하면 에러를 보게 될 겁니다. 그리고 패키지 이름을 다시 `main`으로 변경하고 함수 이름을 다른 것을 사용해 보세요. 그러면 다른 에러 메시지를 보게 될 겁니다. 동일한 변경을 `go build`로 시도해 보세요. 실행할 진입점이 없지만 코드가 컴파일 됩니다. 이런 경우는 예를 들면 라이브러리를 빌드하는 경우와 같이 완벽히 정상 상황입니다.

## Imports

Go에는 참조 없이 사용할 수 있는 `println` 과 같은 수 많은 내장 함수가 있습니다. Go의 표준 라이브러리나 서드파티 라이브러리를 사용하지 않고는 내장 함수와 멀어질 수 없습니다. Go에서 `import` 키워드는 파일의 코드에 패키지를 선언하는 데 사용됩니다.

프로그램을 변경해 봅시다:

```go
package main

import (
  "fmt"
  "os"
)

func main() {
  if len(os.Args) != 2 {
    os.Exit(1)
  }
  fmt.Println("It's over", os.Args[1])
}
```

다음 같이 실행합니다:

```
go run main.go 9000
```

현재 Go의 표준 패키지 중 `fmt`와 `os` 2개를 사용하고 있습니다. 그리고 내장 함수인 `len`도 소개 했습니다. `len`은 문자열의 크기나 딕션너리 내에 값의 갯수 또는 코드에서 보듯이 배열에서 요소의 갯수를 반환합니다. 왜 인자 2개를 대하는지 궁금해 할 수도 있겠네요. 그것은 인덱스가 0인 첫 번째 인자는 항상 현재 동작 중인 실행 파일의 경로이기 때문입니다. (프로그램을 변경해서 직접 확인해 보세요.)

`fmt.Println`과 같이 패키지의 함수 이름 앞에 접두사가 붙는 것을 보셨을 겁니다. 이 부분은 다른 많은 언어들과 다릅니다. 패키지에 대한 내용은 이후 장에서 배우게 될 것입니다. 지금은 패키지를 어떻게 가져와서 사용하는지를 아는 것으로도 좋은 출발입니다.


Go는 패키지를 임포트 하는 것에 엄격합니다. 만약 패키지를 임포트 하고 사용하지 않으면 컴파일 되지 않을 것입니다. 다음을 실행해 보세요:


```go
package main

import (
  "fmt"
  "os"
)

func main() {
}
```

`fmt`와 `os`를 임포트 하고 사용하지 않았다는 두 오류가 발생합니다. 성가실 수도 있을까요? 전혀요. 시간이 지만 익숙해 질 것입니다(그래도 여전히 성가십니다.) 사용하지 않은 임트 패키지는 컴파일을 느리게 할 수 있으므로 Go는 이 부분에 엄격합니다. 대부분은 이 정도까지는 문제가 없다고 인정합니다.

주말할 또 다른 사항은 Go의 표준 라이브러리는 문서화가 잘 되어 있다는 것입니다. 우리가 사용한 `Println` 함수에 대해 더 알아 보려면 <https://golang.org/pkg/fmt/#Println> 를 방문하면 됩니다. 그리고 Go의 서식 기능에 대해 알아 보려면 맨 위로 스크롤 하세요.

인터넷에 접속할 수 없다면 다음과 같이 로컬에서 실행 되는 문서를 볼 수 있습니다:

```
godoc -http=:6060
```

위와 같이 실행 한 후 브라우저로 `http://localhost:6060` 로 갑니다.


## 변수와 선언

변수를 선언하고 끝내려면 *x = 4 라고 변수를 선언하고 할당하라*고 말해주었으면 좋겠습니다. 불행하게도 Go 에서는 조금 더 복잡합니다. 간단한 예를 통해 이야기를 시작하겠습니다. 그리고 다음 장에서 구조체를 만들고 사용할 때 이 예제를 확장할 것입니다. 아직은 편안하게 느끼지기까지는 조금 시간이 걸릴 것입니다.

*무엇이 그렇게 복잡할까* 하고 생각할 수 있습니다. 몇 가지 예를 살펴 보겠습니다.

Go에서 변수를 선언하고 할당하는 가장 명시적인 방법은 가장 장황하기도 합니다:

```go
package main

import (
  "fmt"
)

func main() {
  var power int
  power = 9000
  fmt.Printf("It's over %d\n", power)
}
```

Here, we declare a variable `power` of type `int`. By default, Go assigns a zero value to variables. Integers are assigned `0`, booleans `false`, strings `""` and so on. Next, we assign `9000` to our `power` variable. We can merge the first two lines:
여기서 `int` 타입의 `power` 변수를 선언합니다. Go는 기본적으로 0 값을 변수에 할당합니다. 정수는 `0`, 불린은 `false`, 문자열은 `""` 등으로 할당 됩니다. 다음으로 `power` 변수에 `9000`을 할당합니다. 처음 두 줄을 병합할 수 있습니다:

```go
var power int = 9000
```

Still, that's a lot of typing. Go has a handy short variable declaration operator, `:=`, which can infer the type:
여전히 많이 타이핑 해야 합니다. Go는 편리하고 짧은 변수 선언 연산자 `:= `를 가지고 있습니다. 이 연산자는 타입 추론을 할 수 있습니다:

```go
power := 9000
```

This is handy, and it works just as well with functions:
이것은 편리하며 함수와도 동작합니다:


```go
func main() {
  power := getPower()
}

func getPower() int {
  return 9001
}
```

중요한 것은 `:=`는 변수를 선언하면서 할당도 한다는 것을 기억하는 것입니다. 왜일까요? 왜냐하면 변수는 두번 선언될 수 없기 때문입니다(어쨌든 동일 범위에 있지 않음). 다음과 같이 실행 하면 오류가 발생합니다.

```go
func main() {
  power := 9000
  fmt.Printf("It's over %d\n", power)

  // COMPILER ERROR:
  // no new variables on left side of :=
  power := 9001
  fmt.Printf("It's also over %d\n", power)
}
```

컴파일러는 *:= 왼쪽에 새로운 변수가 없다*고 불평할 것입니다. 이는 처음 변수를 할당할 때는 `:=`를 사용해야 하고 이후 할당문에서는 `=` 연산자를 사용해야 함을 의미합니다. 이는 많은 의미를 지니지만, 이 두 사이를 전환 하는 것을 기억하기 어려울 수도 있습니다.

오류 메시지를 자세히 읽어보면 *variables*가 복수라는 것을 알수 있습니다. 이는 Go 는 (`=` 또는 `:=`를 사용해) 여러 변수에 할당할 수 있기 때문입니다.

```go
func main() {
  name, power := "Goku", 9000
  fmt.Printf("%s's power is over %d\n", name, power)
}
```

As long as one of the variables is new, `:=` can be used. Consider:
변수 중 하나가 새로운 선언이라면, `:=`를 사용할 수 있습니다. 다음을 보세요:

```go
func main() {
  power := 1000
  fmt.Printf("default power is %d\n", power)

  name, power := "Goku", 9000
  fmt.Printf("%s's power is over %d\n", name, power)
}
```

`power`는 `:=`를 이용해 두번 사용되었지만 컴파일러는 두 번째 사용시 불평하지 않을 것입니다. 컴파일러는 다른 변수 `name`이 새로운 변수이므로 이를 허용하는 것입니다. 그러나 `power`의 타입을 변경할 수는 없습니다. (암묵적으로) 정수로 선언되었고 정수만 할당할 수 있습니다.

이제 마지막으로 알려드릴 것은 import 와 마찬가지로 Go는 사용하지 않은 변수를 허용하지 않는다는 것입니다. 예를 들면,

```go
func main() {
  name, power := "Goku", 1000
  fmt.Printf("default power is %d\n", power)
}
```

이 코드는 `name`이 선언되었지만 사용되지 않았기 때문에 컴파일 되지 않을 것입니다. 사용하지 않은 import 와 마찬가지로 약간의 불만아 있겠지만 전반적으로 코드를 깔끔하게 하고 가독성을 높이는데 도움이 된다고 생각합니다.

변수 할당과 선언에 대해 알아야 할 것이 더 있습니다. 지금은 변수를 선언하고 0 값을 할당할 때는 `var NAME TYPE`을 사용하고, 변수를 선언하고 값을 할당할 때는 `NAME := VALUE`를 사용하고, 이미 선언된 변수에 값을 할당할 때는 `NAME = VALUE`를 사용한다는 것만 기억하세요.

## 함수 선언

This is a good time to point out that functions can return multiple values. Let's look at three functions: one with no return value, one with one return value, and one with two return values.
함수가 여러개의 값을 리턴할 수 있다는 것을 말해 줄 때입니다. 세 함수를 확인해 봅시다: 리턴 값이 없는 것, 리턴 값이 하나인 것, 리턴 값이 2개인것.

```go
func log(message string) {
}

func add(a int, b int) int {
}

func power(name string) (int, bool) {
}
```

마지막 함수를 아래와 같이 사용합니다:

```go
value, exists := power("goku")
if exists == false {
  // handle this error case
}
```

가끔은 하나의 반환 값만 신경쓸 때도 있습니다. 이 경우에는 나머지 다른 값은 `_`에 할당합니다:

```go
_, exists := power("goku")
if exists == false {
  // handle this error case
}
```

이는 관습 이상 이상입니다. `_`, 공백 식별자는 실제로 값을 할당하지 않는다는 점에서 특별합니다. 그래서 다른 리턴 타입에도 관계 없이 `_`를 사용할 수 있습니다.

마지막으로 함수 선언에서 사용할만한 것이 있습니다. 파라미터들이 같은 타입을 공유한다면 짧은 구문을 사용할 수 있습니다:

```go
func add(a, b int) int {

}
```

여러 값을 반환할 수 있다는 점은 자주 사용됩니다. `_`도 값을 무시하기 위해 자주 사용됩니다. 이름 붙인 반환값과 약간은 덜 자세한 파라미터 선언은 일반적이지 않습니다. 그래도 곧 이런 처리들을 해야 할 수 있어서서 이들에 대해 아는 것도 중요합니다.

## 계속 진행하기 전에

우리는 여러 개의 작은 개별 부분들 살펴 보았고 아마도 이 시점에서는 흩어져 있을 것입니다. 우리는 천천히 더 큰 예제를 만들어 낼 것이고 조각들은 모이기 시작할 것입니다.

만약 동적 언어를 사용 했었다면 타입과 선언에 관련된 복잡성은 퇴보 처럼 보일 수 있습니다. 그러나 그렇지 않습니다. 일부 시스템에서는 동적 언어가 더 생산적입니다.

만약 정적 타입 언어를 사용했었다면 아마도 Go에 편안함을 느낄 것입니다. 유추 타입과 여러 반환값을 훌륭합니다(Go만의 특징은 아니지만). 좀더 배울 수록 깨끗하고 간겨란 구문을 이해할 수 있기를 바랍니다.

# 2장 - 구조체

Go는 C++, Java, Ruby 그리고 C#과 같은 객체 지향(object-oriented, OO) 언어가 아닙니다. 객체나 상속이 없습니다. 그래서 다형성이나 오버 로딩 등과 같은 객체 지향과 관련된 많은 개념들을 가지고 있지 않습니다.

Go는 메서드와 연관 될 수 있는 구조체를 가지고 있습니다. 또한 Go는 간단하지만 효과적인 형태의 구성을 지원합니다. 전반적으로 더 간단한 코드가 나오지만 객체 지향이 제공하는 기능 중 일부를 제공하지 못하는 경우가 있습니다. (상속에 대해 구성은 오래된 함성이라는 것은 가치 있는 지적이고 이 이슈에 대해 확고한 입장을 가진 것두 내가 사용한 첫 번째 언어가 Go 입니다.)

Go가 사용하던 객체 지향이 아니더라도 클래스의 그것과 구조체의 선언은 매우 유사하다는 것을 알게 될 것입니다. 간단한 예는 다음에 `Saiyan` 구조체 입니다:

```go
type Saiyan struct {
  Name string
  Power int
}
```

클래스의 부분으로 메서드를 추가 하는 것 처럼 이 구조체에 메서드를 추가하는 방법을 곧 보여 드릴겁니다. 그 전에 선언을 먼저 살펴 봅시다.

## 선언과 초기화

변수와 선언을 살펴보면 정수와 문자열 같은 내장타입만 사용한 것을 볼 수 있습니다. 지금은 구조체에 대한 것만 이야기 하고, 이야기를 포인터를 포함하는 부분 까지 확장해야 합니다.

구조체의 값을 생성하는 가장 단순한 방법은 다음과 같습니다:

```go
goku := Saiyan{
  Name: "Goku",
  Power: 9000,
}
```
*참고:* 위 구조체의 마지막 줄 `,` 끝 문자는 필수입니다. 없애면 컴파일러가 오류를 발생시킵니다. 그 반대의 형식이나 언어를 사용했다면 이 부분에서 일괄성을 느낄 수 있을 겁니다.

모든 필드를 다 설정할 필요는 없습니다. 아무 필드를 설정하지 않아도 됩니다. 아래 두 가지는 모두 유효합니다:

```go
goku := Saiyan{}

// or

goku := Saiyan{Name: "Goku"}
goku.Power = 9000
```

할당되지 않은 변수와 마찬가지로 0 값을 가질 것이므로 필드도 값을 가집니다.

또한 필드 이름을 건너 뛰고 필드 선언 순서에 의존할 수도 있습니다.(명확히 하기 위해 필드가 적은 구조체에만 이렇게 해야합니다):

```go
goku := Saiyan{"Goku", 9000}
```

위의 예제가 하는 일은 `goku` 변수를 선언하고 값을 할당하는 것입니다.

그러나 많은 경우에 우리 값에 직접 연관되는 변수가 아닌 값을 가리키는 포인터 변수를 원하는 경우가 많습니다. 포인터는 메모리 주소입니다; 실제 값을 찾을 수 있는 위치입니다. 간접적인 수준입니다. 말하자면 집에 있는 것과 집의 방향을 가리키는 정도의 차이입니다.

Why do we want a pointer to the value, rather than the actual value? It comes down to the way Go passes arguments to a function: as copies. Knowing this, what does the following print?
왜 실제 값이 아닌 값을 가리키는 포인터가 필요할까요? 그 이유는 Go가 함수에 인자를 전달하는 방식이 사본 방식이기 때문입니다. 이것을 생각하면서 다음 코드에는 무엇이 출력될까요?

```go
func main() {
  goku := Saiyan{"Goku", 9000}
  Super(goku)
  fmt.Println(goku.Power)
}

func Super(s Saiyan) {
  s.Power += 10000
}
```

정답은 19000이 아니라 9000 입니다. 왜일까요? `Super`함수가 원본 `goku`의 사본을 만들고 변경하기 때문입니다. 그래서 `Super`에서 발생한 변경이 호출자에게 반영되지 않았습니다. 원하는대로 동작시키려면 값을 포인터로 넘겨야 합니다:

```go
func main() {
  goku := &Saiyan{"Goku", 9000}
  Super(goku)
  fmt.Println(goku.Power)
}

func Super(s *Saiyan) {
  s.Power += 10000
}
```

두 가지를 변경했습니다. 첫 번째는 (주소 연산자라고 불리는) `&` 연산자를 값의 주소를 얻기 위해 사용 했습니다. 다음은 `Super`의 인자를 변경했습니다. 기존에는 `Saiyan` 타입의 값을 받았지만 지금은 `**Saiyan` 타입으로 주소를 받습니다. `*X`는 *X 타압의 값을 가리키는 포인터라*는 뜻입니다. 분명 `Saiyan`과 `*Saiyan` 사이는 어떤 관계가 있지만 둘은 다른 타입입니다.

`goku`의 값이 주소로 변경 되었기 때문에 여전히 `Super`에 `goku`의 복사본을 넘겨주는 준다는 것에 주목해 주세요. 그 간접적으로 획득한 복사본 주소는 원본의 주소와 동일합니다. 이것을 식당을 가리키는 지시에 대한 복사라고 생각해보세요. 가지고 있는 것은 복사본이지만 여전히 동일한 식당을 가리키고 있습니다.

가리키는 곳을 변경하여 그것이 사본이라고 증명할 수 있습니다.(그러나 실제로는 그렇게 하고 싶지 않을 것 같군요):

```go
func main() {
  goku := &Saiyan{"Goku", 9000}
  Super(goku)
  fmt.Println(goku.Power)
}

func Super(s *Saiyan) {
  s = &Saiyan{"Gohan", 1000}
}
```

다시 위 코드는 9000을 출력합니다. 루비, 파이썬, 자바, C# 을 포함한 많은 언어가 이렇게 동작합니다. 가서 C#을 사용해 보면 사실을 쉽게 확인할 수 있습니다.

복잡한 구조체를 복사하는 것 보다 포인터를 복사하는 것이 더 효율적인라는 것은 분명합니다. 64비트 머신에서 포인터는 64비트 입니다. 만약 구조체가 많은 필드를 가지고 있다면 복사본을 만드는 것은 비싼 작업일 수 있습니다. 포인터의 진짜 가치는 값을 공유할 수 있다는 것입니다. `Super`가 `goku`의 복사본을 변경하거나 공유된 `goku` 값 자체를 변경하기를 원합니까?

이 모든 것이 항상 포인터를 사용해야 한다는 것을 뜻하지는 않습니다. 구조체로 할 수 있는 것을 더 살펴 본 후 이 장 끝에서 포인터 대 값에 대한 질문을 다시 검토 할 것입니다.

## 구조체에 대한 함수

우리는 메소르를 구조체에 연결할 수 있습니다:

```go
type Saiyan struct {
  Name string
  Power int
}

func (s *Saiyan) Super() {
  s.Power += 10000
}
```

위의 코드에서 `*Saiyan` 타입을 `Super`의 **리시버** 라고 말합니다. `Super`를 이렇게 호출 합니다:

```go
goku := &Saiyan{"Goku", 9001}
goku.Super()
fmt.Println(goku.Power) // will print 19001
```

## 생성자

구조체는 생성자가 없습니다. 대신, 필요한 타입의 인스턴스를 리턴하는 함수를 생성할 수 있습니다(팩토리 처럼):

```go
func NewSaiyan(name string, power int) *Saiyan {
  return &Saiyan{
    Name: name,
    Power: power,
  }
}
```

이 패턴은 많은 개발자들을 잘못된 길로 나가게 합니다. 아래는 아주 작은 문법적 변화를 준 것인데 좀더 적은 구획이 나누어진 느낌이 듭니다.

우리 팩토리 함수는 포인터를 리턴하지 않습니다; 이것도 확실히 유효합니다:

```go
func NewSaiyan(name string, power int) Saiyan {
  return Saiyan{
    Name: name,
    Power: power,
  }
}
```

## New

생성자가 없음에도 불구하고 Go는 타입에 필요한 메모리를 할당하는 내장 `new` 함수를 가지고 있습니다. `new(X)`의 결과는 `&X{}`와 동일합니다:

```go
goku := new(Saiyan)
// same as
goku := &Saiyan{}
```

둘 중 어느 것을 사용하든 당신의 선택이지만, 읽기 쉬운 경향이 있기 때문에 필드를 초기화 할때는 후자를 선호한다는 것을 알수 있을 것이다:

```go
goku := new(Saiyan)
goku.name = "goku"
goku.power = 9001

//vs

goku := &Saiyan {
  name: "goku",
  power: 9000,
}
```

어떤 것을 선택하든 위 팩토리 패턴을 따르기만 하면 나머지 코드를 할당에 대한 세부 걱정과 지식이 필요 없도록 보호 할 수 있습니다.


## 구조체의 필드

지금까지 보았던 예제에서 `Saiyan`은 `string`과 `int` 타입인 `Name`과 `Power` 필드를 가지고 있습니다. 필드는 다른 구조체나 아직 다루지 않은 배열, 맵, 인터페이스와 함수 등을 포함해서 어떤 타입도 가능합니다.

예를 들면 `Saiyan`을 아래와 같이 확장할 수 있습다:

```go
type Saiyan struct {
  Name string
  Power int
  Father *Saiyan
}
```

다음과 같이 초기화 할 것입니다:

```go
gohan := &Saiyan{
  Name: "Gohan",
  Power: 1000,
  Father: &Saiyan {
    Name: "Goku",
    Power: 9001,
    Father: nil,
  },
}
```

## 구성(Composition)

Go는 하나의 구조체를 다른 구조체에 포함시키는 동작을 하는 구성을 지원합니다. 어떤 언어에서는 이것을 특성(trait) 또는 혼합(maxin)이라고 합니다. 명시적으로 구성 메커니즘이 없는 언어는 항상 먼길을 돌아 야 작업할 수 있습니다. 자바의 경우에 *상속*으로 구조체를 확장할 수 있지만, 옵션이 없는 시나리오에서는 다음과 같이 혼합을 구현합니다:

```java
public class Person {
  private String name;

  public String getName() {
    return this.name;
  }
}

public class Saiyan {
  // Saiyan is said to have a person
  private Person person;

  // we forward the call to person
  public String getName() {
    return this.person.getName();
  }
  ...
}
```

이것은 많이 장황해질 수 있습니다. `Person`의 모든 메소드를 `Saiyan`에 복제해야 합니다. Go는 이런 장황함을 이렇게 피합니다:

```go
type Person struct {
  Name string
}

func (p *Person) Introduce() {
  fmt.Printf("Hi, I'm %s\n", p.Name)
}

type Saiyan struct {
  *Person
  Power int
}

// and to use it:
goku := &Saiyan{
  Person: &Person{"Goku"},
  Power: 9001,
}
goku.Introduce()
```

`Saiyan` 구조체는 `*Person` 타입의 필드를 가집니다. 필드에 명시적으로 필드 이름을 주지 않았기 때문에 구성된 타입의 필드와 함수를 암묵적으로 접근할 수 있습니다. 그러나 Go 컴파일러는 필드의 이름을 지정 했습니다. 다음은 완벽히 유효하다고 간주합니다:

```go
goku := &Saiyan{
  Person: &Person{"Goku"},
}
fmt.Println(goku.Name)
fmt.Println(goku.Person.Name)
```

위는 둘다 "Goku"를 출력합니다.

상속보다 구성이 좋을까요? 많은 사람들은 구성이 코드를 공유하는 좀더 강력한 방법이라고 생각합니다. 상속을 사용할 때, 클래스는 상위 클래스와 밀접하고 연관되어(coupled) 있고 행동보다는 계층 구조에 집중하게 됩니다.

### 오버로딩

오버로딩은 구조체에 특화된 것은 아니지만 언급할 가지는 있습니다. 단순히 Go는 오버로딩을 지원하지 않습니다. 이런 이유로 `Load`, `LoadById`, `LoadByName` 등과 같은 많은 함수를 보게 될 것입니다.

그러나 암시적인 구성은 구성된 타입의 함수를 덮어 쓸 수 있는 컴파일러 트릭입니다. 예를 들면 `Saiyan` 구조체는 자체적인 `Introduce`함수를 가질 수 있습니다:

```go
func (s *Saiyan) Introduce() {
  fmt.Printf("Hi, I'm %s. Ya!\n", s.Name)
}
```

구성된 버전의 함수는 항상 `s.Person.Introduce()`를 통해 호출 가능합니다.

## 포인터와 값

Go 코드를 작성할 때, 자연스럽게 값을 써야 하는지 포인터를 써야 하는지에 대한 묻게 됩니다. 두 가지 좋은 소식이 있습니다. 첫 번째는 뒤에서 이야기 하는 것들은 어느 것을 쓰든 관계 없다는 것입니다:

* 로컬 변수 할당
* 구조체 필드
* 함수의 리턴값
* 함수로의 인자
* 메소드의 리시버

둘째, 잘 모르겠으면 포인터를 사용하세요.

이미 봤겠지만, 값을 전달하는 것은 데이터를 변경하지 못하게 하는 좋은 방법입니다(함수에서 변경한 내용은 호출한 코드에 반영되지 않습니다). 때로는 이게 원하는 동작이지만, 대부분은 그렇지 않습니다.

데이터를 변경하려는 의도가 아니더라도 큰 구조체는 복사본을 생성하는 비용을 생각해 보세요. 반대로 작은 구조체일 수도 있습니다. 말하자면:

```go
type Point struct {
  X int
  Y int
}
```

이런 경우 구조체 복사 하는 비용은 직접 `X`와 `Y`에 접근할 수 있는 것으로 상쇄될 것입니다.

다시 말하지만, 이것들은 모두 미묘한 케이스입니다. 수천 수만번 이런 부분을 반복하지 않으면 차이점을 느끼지 못할 것입니다.

## 계속 진행하기 전에

실용적인 관점에서 이 장에서는 구조체를 소개했고 구조체, 함수의 리시버의 인스턴스를 만드는 방법을 설명하고 Go 타입 시스템에 관한 지식에 포인터를 추가 했습니다. 이어지는 장은 우리가 탐구한 내적 작업과 구조체를 토대로 설명합니다.

# 3장 - 맵, 배열 그리고 슬라이스

지금까지 간단한 타입과 구조체를 보았습니다. 이제 배열, 슬라이스 그리고 맵을 볼 차례입니다.

## 배열

당신이 파이썬, 루비, 펄, 자바스크립트 또는 PHP (그리고 기타) 사용자라면 동적 배열을 사용해서 프로그래밍 하는데 익숙할 것입니다. 동적 배열은 데이터가 추가될 때 스스로 크기를 조정합니다. Go에서는 다른 언어와 마찬가지로 배열은 고정되어 있습니다. 배열을 선언하려면 크기를 지정해야 하며 한번 크기가 정해지면 커질 수 없습니다.

```go
var scores [10]int
scores[0] = 339
```

위 배열은 `scores[0]`에서 `scores[9]`까지 10개의 socre를 담을 수 있습니다. 범위를 벗어나 접근하려고 하면 컴파일러 또는 런타임 오류가 발생할 것입니다.

값들로 배열을 초기활 할 수 있습니다:

```go
scores := [4]int{9001, 9333, 212, 33}
```

배열의 길이를 구하려면 `len`을 사용합니다. `range`를 배열 요소에 반복 접근 할 수 있습니다.

```go
for index, value := range scores {

}
```

배열은 효율적이지만 경직되어 있습니다. 우리는 종종 다루어야 할 요소의 개수를 미리 알지 못합니다. 이를 위해 슬라이스를 사용합니다.

## 슬라이스

Go에서는 배열을 직접 사용하는 경우는 거의 없습니다. 대신 슬라이스를 사용합니다. 슬라이스는 배열의 일부를 감싸고 나타내는 가벼운 구조체입니다. 슬라이스를 생성하는데는 몇 가지 방법이 있는데, 나중에 사용할 때 살보 볼 것입니다. 첫 번째는 배열을 만드는 방법의 약간 변형입니다:

```go
scores := []int{1,4,293,4,9}
```

배열 선언과는 달리 슬라이스는 대괄호([])안에 길이를 선언하지 않습니다. 이 둘이 어떻게 다른지 이해하기 위해 `make`를 사용해 슬라이스를 생성해 봅시다:

```go
scores := make([]int, 10)
```

슬라이스를 생성하는 것은 단순히 메모리를 할당하는 것(`new`가 수행하는 것) 이상의 작업이 필요하기 때문에 `new` 대신 `make`를 사용합니다. 특히, 내부의 배열의 메모리를 할당하고 슬라이스 또한 초기화 해야 합니다. 위에서 길이가 10이고 용량이 10인 슬라이스를 초기화 합니다. 길이는 슬라이스의 크기이고 용량은 내부 배열의 크기 입니다. `make`를 사용하여 두 가지를 따로 지정할 수 있습니다:

```go
scores := make([]int, 0, 10)
```

이것은 길이는 0이지만 용량은 10인 슬라이스를 만듭니다. (주의를 좀 기울였다면 `make` 와 `len`이 오버로드 되었다는 것을 알게 될 것입니다. Go는 개발자에게 사용이 노출되지 않은 기능을 사용하기도 해 좌절감을 불러 일어키는 언어 입니다.)

길이와 용량의 상호 작용에 대해 더 이해하기 위해서 몇 가지 예제를 살펴 보겠습니다:

```go
func main() {
  scores := make([]int, 0, 10)
  scores[7] = 9033
  fmt.Println(scores)
}
```
첫 번째 예제는 크래시가 발생 합니다. 왜냐하면 슬라이스의 길이가 0이기 때문입니다. 맞습니다. 내부 배열은 10개의 요소를 가지고 있지만 이 요소들에 접근하려면 명시적으로 확장해야 합니다. 슬라이스를 확장하는 방법 중 하나는 `append`를 통하는 것입니다:

```go
func main() {
  scores := make([]int, 0, 10)
  scores = append(scores, 5)
  fmt.Println(scores) // prints [5]
}
```

그러나 저 코드는 원본 코드의 의도와 다릅니다. 길이가 0인 슬라이스에 추가(append)하면 첫 번째 요소에 설정될 것입니다. 어떤 이유로 크래시가 발생한 원본 코드는 인덱스가 7인 요소에 설정하려고 했습니다. 이렇게 하기 위해 슬라이스를 다시 슬라이스로 만들면 가능합니다:

```go
func main() {
  scores := make([]int, 0, 10)
  scores = scores[0:8]
  scores[7] = 9033
  fmt.Println(scores)
}
```

슬라이스 크기를 얼마다 크게 조정할 수 있을까요? 슬라이스의 용량 만큼 크게 할 수 있고 이 코드의 경우에는 10입니다. *이건 배열의 고정된 길이 이슈를 실제로 해결하지 못 하는 것 아닌가*라고 생각할 수도 있습니다. `append`는 특별하다고 할 수 있습니다. `append`는 내부 배열이 가득 차면 새로운 더 큰 배열을 할당하고 값들을 거기 복사 합니다(이는 PHP, 파이썬, 루비, 자바스크립트에서 동적 배열이 동작하는 방식과 정확히 동일합니다). 위의 예제에서 `append`를 사용할 때  `append`의 변환값을 `scores` 변수에 다시 할당하는 이유가 이것입니다.  `append`는 원본이 더 이상 공간이 없으면 새로운 값(슬라이스)을 생성할 수도 있습니다

Go가 2x 알고리즘으로 배열을 증가시킨다면 아래 코드는 어떤 결과를 출력할지 예측할 수 있나요?

```go
func main() {
  scores := make([]int, 0, 5)
  c := cap(scores)
  fmt.Println(c)

  for i := 0; i < 25; i++ {
    scores = append(scores, i)

    // if our capacity has changed,
    // Go had to grow our array to accommodate the new data
    if cap(scores) != c {
      c = cap(scores)
      fmt.Println(c)
    }
  }
}
```

`scores` 초기 용량은 5입니다. 25개의 값을 담기 위해 3번의 용량 확장이 발생해야 하며 그 용량값은 10, 20, 그리고 마지막으로 40입니다.

마지막 예를 보시면:

```go
func main() {
  scores := make([]int, 5)
  scores = append(scores, 9332)
  fmt.Println(scores)
}
```

여기는 `[0, 0, 0, 0, 0, 9332]`이 출력될 것입니다. 아마도 `[9332, 0, 0, 0, 0]`라고 생각했나요? 사람에게는 그것이 논리적으로 보일수도 있습니다. 컴파일러에게는 이미 5개의 값을 저장하고 있는 슬라이스에 값을 추가하라는 의미 입니다.

궁극적으로 슬라이스를 초기화는 데는 네 가지 일반적인 방법이 있습니다.

```go
names := []string{"leto", "jessica", "paul"}
checks := make([]bool, 10)
var names []string
scores := make([]int, 0, 20)
```

언제 어느 것을 사용해야 할까요? 첫 번째는 많은 설명이 필요하지 않습니다. 이것은 미리 배열에 저장할 값을 알고 있을 때 사용합니다.

두 번째는 슬라이스의 특정 인덱스에 값을 쓸 때 유용합니다. 예를 들면:

```go
func extractPowers(saiyans []*Saiyan) []int {
  powers := make([]int, len(saiyans))
  for index, saiyan := range saiyans {
    powers[index] = saiyan.Power
  }
  return powers
}
```

세 번째는 요소의 수가 알려지지 않았을 때 nil 슬라이스로 할당하고 `append`와 함께 사용합니다.

마지막 버전은 초기 용량을 지정할 수 있습니다. 얼마나 많은 요소가 필요한지에 대해 알고 있다면 유용합니다.

크기를 아는 경우에라도 `append`를 사용할 수 있습니다. 그것은 선호의 문제입니다:

```go
func extractPowers(saiyans []*Saiyan) []int {
  powers := make([]int, 0, len(saiyans))
  for _, saiyan := range saiyans {
    powers = append(powers, saiyan.Power)
  }
  return powers
}
```

배열 랩퍼로서의 슬라이스는 강력한 개념입니다. 많은 언어에 배열을 분할한다는 개념이 있습니다. 자바스크립트와 루비 둘다 배열에 `slice` 메소드가 있습니다. 루비에서 `[START..END]`를 파이선에서는 `[START:END]`를 이용해 슬라이스를 구할 수 있습니다. 그러나 이런 언어들에서는 슬라이스는 원본의 복사한 값을 가진 새로운 배열입니다. 루비를 사용한다면 아래와 같은 코드는 무엇이 출력될까요?

```ruby
scores = [1,2,3,4,5]
slice = scores[2..4]
slice[0] = 999
puts scores
```

정답은 `[1, 2, 3, 4, 5]`입니다. `slice`가 값을 복사한 완전히 새로운 배열을 이기 때문입니다. 이제 Go의 동일한 경우를 봅시다:

```go
scores := []int{1,2,3,4,5}
slice := scores[2:4]
slice[0] = 999
fmt.Println(scores)
```

결과는 `[1, 2, 999, 4, 5]` 입니다.

이것은 코딩 방법을 바꿉니다. 예를 들면, 많은 함수들이 파라미터의 위치를 사용합니다. 자바스크립트에서는 문자열에서 처음 다섯 글자 이후에 첫 번째 공백을 찾으려면 (네, 문자열에서도 슬라이스가 동작합니다!) 다음과 같이 작성합니다:

```javascript
haystack = "the spice must flow";
console.log(haystack.indexOf(" ", 5));
```

Go에서는 슬라이스를 활용합니다:

```go
strings.Index(haystack[5:], " ")
```

위 예제에서 `[:X]`는 시작 부터 X까지, `[X:]`는 X부터 끝까지의 줄임말 임을 알수 있습니다. 다른 언어들과 달리 Go는 음수 값 인덱스를 지원하지 않습니다. 슬라이스의 마지막 값을 제외한 모든 값을 원한다면, 다음과 같이 합니다:

```go
scores := []int{1, 2, 3, 4, 5}
scores = scores[:len(scores)-1]
```

위는 정렬되지 않은 슬라이스에서 값을 제거하는 효율적인 방법의 시작입니다.

```go
func main() {
  scores := []int{1, 2, 3, 4, 5}
  scores = removeAtIndex(scores, 2)
  fmt.Println(scores) // [1 2 5 4]
}

// 순서를 보존 하지 않음
func removeAtIndex(source []int, index int) []int {
  lastIndex := len(source) - 1
  //swap the last value and the value we want to remove
  source[index], source[lastIndex] = source[lastIndex], source[index]
  return source[:lastIndex]
}
```

마지막으로, 슬라이스에 대해 알았고 흔히 사용되는 내장 함수인 `copy`에 대해 살펴 볼 수 있습니다. `copy`는 우리가 코딩하는 방법을 슬라이스가 어떻게 변화시키는지 잘 알려주는 함수 중 하나 입니다. 일반적으로, 배열에서 배열로 복사 하는 메소드는 `source`, `sourceStart`, `count`, `destination` 그리고 `destinationStart` 와 같이 5가지 파라미터가 필요하다. 슬라이스를 이용하면 단 두개만 필요하다:

```go
import (
  "fmt"
  "math/rand"
  "sort"
)

func main() {
  scores := make([]int, 100)
  for i := 0; i < 100; i++ {
    scores[i] = int(rand.Int31n(1000))
  }
  sort.Ints(scores)

  worst := make([]int, 5)
  copy(worst, scores[:5])
  fmt.Println(worst)
}
```


시간을 들여 위 코드를 가지고 놀아보시기 바랍니다. 변형을 시도해 보세요.  `copy(worst[2:4], scores[:5])` 같이 변경 했을 때 어떤 일이 벌어지는지 확인해 보세요. `5`보다 크거나 작은 갯수의 값들을 `worst`에 복사할 때는 어떻게 되나요?

## 맵

다른 언어에서 해시나 딕션너리라고 부르는 것을 Go에서는 맵이라고 합니다. 맵은 키와 값을 정의하고 값을 읽어 오고, 설정하고, 삭제할 수 있습니다.

맵은 슬라이스 처럼 `make`함수로 만듭니다. 예제를 살펴봅시다:

```go
func main() {
  lookup := make(map[string]int)
  lookup["goku"] = 9001
  power, exists := lookup["vegeta"]

  // 0, false 가 출력됨
  // 0 은 정수의 기본값
  fmt.Println(power, exists)
}
```

키의 갯수를 얻으러면 `len`을 사용합니다. 키에 기반해 값을 제거하려면 `delete`를 사용합니다.

```go
// 1 반환
total := len(lookup)

// 반환값이 없음, 존재하지 않은 키로 호출 가능함.
delete(lookup, "goku")
```

맵은 동적으로 커집니다. 그러나 초기 크기를 지정하기 위해 `make`의 두번째 인자를 줄 수 있습니다.

```go
lookup := make(map[string]int, 100)
```

얼마나 많은 키가 필요한지 알면 초기 크기를 지정하여 성능에 도움을 줄 수 있습니다.

구조체에 필드로 맵이 필요하면, 다음과 같이 정의 합니다:

```go
type Saiyan struct {
  Name string
  Friends map[string]*Saiyan
}
```

위 구조체를 초기화 하는 방법은 아래와 같습니다:

```go
goku := &Saiyan{
  Name: "Goku",
  Friends: make(map[string]*Saiyan),
}
goku.Friends["krillin"] = ... //todo Krillin을 로드하거나 생성해야 함
```

Go에서 값을 선언하고 초기화 하는 또 다른 방법이 있습니다. `make` 처럼, 이 접근법은 맵과 배열에 한정적입니다. 다음과 같이 복합 리터널로 선언할 수 있습니다:

```go
lookup := map[string]int{
  "goku": 9001,
  "gohan": 2044,
}
```

`for` 루프와 `range` 키워드를 조합해 맵을 순회할 수 있습니다:

```go
for key, value := range lookup {
  ...
}
```

맵을 통해 순회를 할 수는 없습니다. 순회가 반복될 때마다 키와 값의 쌍이 임의의 순서대로 반환됩니다.

## 포인터와 값

우리는 포인터를 전달해야 하는지 값을 전달해야 하는지에 대해 살펴보면서 2장을 마쳤습니다. 배열과 맵에 대해서도 동일한 주제를 다룰 것입니다. 다음 중 어느 것을 사용해야 할까요?

```go
a := make([]Saiyan, 10)
//or
b := make([]*Saiyan, 10)
```

많은 개발자들이 함수에 `b`를 넘기거나 반환 받는게 더 효율적이다라고 생각합니다. 그러나 전달되는 것은 슬라이스 자체를 참조하는 복사본입니다. 따라서 슬라이스 자체를 넘기고 반환하는 것과 차이가 없습니다.

차이는 슬라이스나 맵의 값을 수정할 때 나타납니다. 이 시점에는 2장에서 봤던 것과 동일한 논리가 적용됩니다. 그래서 값의 배열과 포인터의 배열 중 어떤 것으로 정의할지 결정은 배열이나 맵 자체를 어떻게 사용하느냐가 아니라 개별 값들을 어떻게 사용하느냐에 따라 좌우 됩니다.

## 계속 진행하기 전에

Go에서 배열과 맵은 다른 언어와 매우 유사하게 동작합니다. 여러분이 동적 배열을 사용했다면 약간의 조정이 필요하겠지만 `append`가 대부분의 불편함을 해소해 줄 것입니다. 배열의 피상적인 문법을 넘어면 우리는 슬라이스를 발견합니다. 슬라이스는 강력하고 코드의 명확성에 놀라울 만큼 큰 영향을 줍니다.

우리가 다루지 않은 엣지 케이스(edge case)가 있습니다만 그 케이스에 빠질 가능성은 낮습니다. 그리고 그런 케이스에 빠져도 여기서 익힌 내용으로 무슨 일이 일어나고 있는지 이해하게 될 것입니다.

# 4장 - 코드 구성 및 인터페이스

이제 코드를 구성하는 방법을 살펴 보겠습니다.

## 패키지

더 복잡한 라이브러리와 시스템을 구성하려면 패키지에 대해 알아야 합니다. Go에서는 패키지 이름은 Go 작업 공간의 디렉토리 구조에 따릅니다. 쇼핑 시스템을 구축하고 있다면, 패키지 이름을 "shopping"이라고 하고 소스를 `$GOPATH/src/shopping/` 에 넣을 것입니다.

이 폴더에 모든 것을 넣고 싶지는 않습니다. 예를 들면 데이터베이스 로직은 별도 자체 폴더에 분리하고자 할 것입니다. 이렇게 하기 위해 하위 폴더 `$GOPATH/src/shopping/db`를 만듭니다. 이 하위 폴더 내에 파일의 패키지 이름은 단순히 `db`이지만 다른 패키지에서 여기에 접근하기 위해서는 `shopping` 패키지를 포함해 `shopping/db`를 임포트 해야 합니다.

즉, `package` 키워드를 통해 패키지 이름을 지정할 때, 전체 계층이 아닌 단일 값을 지정해야 합니다(예, "shopping" 또는 "db"). 패키지를 임포트할 때는 완전한 경로를 지정합니다.

실습을 해 봅시다. Go 작업 공간의 `src` 폴더(앞의 소개의 시작 부분에서 설정한) 내부에 하위에 `db`를 가진 `shopping`이라는 새 폴더를 만듭니다.


`shopping/db` 내부에 , `db.go` 라는 파일을 만들고 다음 코드를 추가합니다:

```go
package db

type Item struct {
  Price float64
}

func LoadItem(id int) *Item {
  return &Item{
    Price: 9.001,
  }
}
```

패키지 이름은 폴더 이름과 동일함에 주의하세요. 또한 실제로 데이터베이스에 접근하지 않습니다. 코드가 어떻게 구성되는지 보여주기 위한 예제로만 이 파일을 사용하고 있습니다.

이제 메인 `shopping` 폴더 내에 `pricecheck.go`라는 파일을 만드세요. 그 파일의 내용은:

```go
package shopping

import (
  "shopping/db"
)

func PriceCheck(itemId int) (float64, bool) {
  item := db.LoadItem(itemId)
  if item == nil {
    return 0, false
  }
  return item.Price, true
}
```

이미 `shopping` 패키지/폴더 안에 있기 때문에 `shopping/db`로 임포팅 하는 것이 특별하다고 생각하도록 부추깁니다.실제로는 `$GOPATH/src/shopping/db`를 임포트하고 있습니다. 이것은 `src/test` 폴더 안에 `db`라는 이름의 패키지를 가지고 있다면 쉽게 `test/db`도 쉽게 임포트할 수 있다는 뜻입니다.

패키지를 만드는 중이라면 지금까지 본 것 이상이 필요하지는 않습니다. 실행 파일을 만드려면 `main`이 필요합니다. 제거 선호하는 방법은 `shopping` 내에 `main`이라는 하위 폴더를 만들고 `main.go`을 생성하는 것입니다. 파일의 내용은 다음과 같습니다:

```go
package main

import (
  "shopping"
  "fmt"
)

func main() {
  fmt.Println(shopping.PriceCheck(4343))
}
```

이제 `shopping` 프로젝트로 들어가 다음과 같이 타이핑 해서 코드를 실행할 수 있습니다:

```
go run main/main.go
```

### 순환 임포트

좀더 복잡한 시스템을 작성하기 시작하면 순환 임포트 문제에 부딪히게 됩니다. 이는 패키지 A가 패키지 B를 임포트 하고 패키지 B가 패키지 A를 임포트할때 발생합니다(직접 또는 다른 패키지를 통해 간접으로). 이는 컴파일러가 허용하지 않습니다.

이 오류가 발생하도록 shopping 구조를 변경해 봅시다.

`Item` 정의를 `shopping/db/db.go`에서 `shopping/pricecheck.go`로 옮깁니다. `pricecheck.go` 파일은 아래와 같은 모습일 겁니다:

```go
package shopping

import (
  "shopping/db"
)

type Item struct {
  Price float64
}

func PriceCheck(itemId int) (float64, bool) {
  item := db.LoadItem(itemId)
  if item == nil {
    return 0, false
  }
  return item.Price, true
}
```

코드를 실행하려고 하면 `db/db.go`에서 `Item`이 정의되지 않음에 대한 몇 개의 오류가 발생합니다. 오류가 맞습니다. `Item`은 더 이상 `db` 패키지에 없습니다. 그것은 shopping 패키지로 옮겨졌습니다. `shopping/db/db.go`를 다음과 같이 수정해야 합니다:

```go
package db

import (
  "shopping"
)

func LoadItem(id int) *shopping.Item {
  return &shopping.Item{
    Price: 9.001,
  }
}
```

이제 코드를 실행해 보면 무시무시한 *순환 임포트가 허용되지 않음* 오류가 발생합니다. 우리는 이 문제를 공유 구조체를 가진 다른 패키지를 만들어서 해결할 것입니다. 디렉토리 구조는 아래와 같아야 합니다:

```
$GOPATH/src
  - shopping
    pricecheck.go
    - db
      db.go
    - models
      item.go
    - main
      main.go
```

`pricecheck.go`는 `shopping/db`를 여전히 임포트 하지만, `db.go`는 `shopping` 대신 `shopping/models`를 임포트할 것입니다. 이렇게 해서 순환을 끊습니다. 공유된 `Item` 구조체를 `shopping/models/item.go`로 옮겼기 때문에 `Item` 구조체를 `models` 패키지로부터 참조하기 위해 `shopping/db/db.go`를 수정해야 합니다:

```go
package db

import (
  "shopping/models"
)

func LoadItem(id int) *models.Item {
  return &models.Item{
    Price: 9.001,
  }
}
```

가끔 `models` 이상의 공유가 필요할 때가 있기 때문에 `utilities`와 같은 폴더가 있을 수도 있습니다. 이런 공유 패키지에 대한 중요한 규칙은 다른 하위 패키지나 `shopping` 패키지에서 아무것도 임포트 하지 않아야 한다는 것입니다. 몇몇 섹션에서 이러한 유형의 의존성을 해결할 수 있는 인터페이스를 살볼 것입니다.

## 가시성

Go는 타입과 함수가 패키지 바깥으로 노출되는 것에 대해 정의 하는 간단한 규칙이 있습니다. 타입이나 함수의 이름이 대문자로 시작하면 노출 됩니다. 소문자로 시작하면 노출되지 않습니다.


예를 들면, `items.go` 파일이 아래와 같은 함수를 가지고 있다면:

```go
func NewItem() *Item {
  // ...
}
```

그 함수는 `models.NewItem()`을 통해 호출할 수 있습니다. 그러나 함수 이름이 `newItem`이었다면 다른 패키지에서 이 함수를 호출할 수 없었을 것입니다.

`shopping` 코드에서 다양한 함수, 타입 및 필드 이름을 변경해 보세요. 예를 들면, `Item의 Price`를 `price`로 변경하면 오류가 발생할 것입니다.

### 패키지 관리

`run`과 `build` 하는데 사용했던 `go` 명령어는 `get` 하위 명령을 가지고 있습니다. 이 명령은 서드 파티 라이브러리를 가져오는데 사용합니다. `go get`은 다양한 프로토콜을 지원하지만 이 예제에서는 Github 에서 라이브러리를 가져올 것입니다. 여러분의 컴퓨터에 `git`이 설치되어 있어야 한다는 의미 입니다.

이미 git이 설치되어 있다고 가정하고 쉘/명령창에서 다음과 같이 입력합니다:

```
go get github.com/mattn/go-sqlite3
```

`go get`은 작업 공간으로 원격파일을 가져와 저장합니다. `$GOAPTH/src`를 확인해 보세요. 우리가 만든 `shopping` 프로젝트에 추가적으로 `github.com` 폴더가 보일 것입니다. 폴더 안에 `go-sqlite3` 폴더를 포함하는 `mattn` 폴더가 보일 것입니다.


작업 공간으로 패키지를 가져오는 방법에 대해 이야기 했습니다. 새로 가져온 `go-sqllite3` 패지지를 사용하려면 다음과 같이 임포트 해야 합니다:

```go
import (
  "github.com/mattn/go-sqlite3"
)
```

### 의존성 관리

`go get`은 몇 가지 트릭이 있습니다. 프로젝트 내에서 `go get`하면 모든 파일을 검사해 서드 파티 라이브러리의 `import`를 찾을 것이고 그것들을 다운로드 할 것입니다. 어떤 면에서 소스코드 자체가 `Gemfile` 이나 `package.json`이 됩니다.

`go get -u`라고 호출하면 패키지를 업데이트 할 것 입니다(또는 `get get -u FULL_PACKAGE_NAME`을 통해 특정 패키지를 업데이트 할 수도 있습니다).

결국, 여러분은 `go get`이 부족한 면이 있다는 것을 발견할 지도 모릅니다. 그중 한가지는 리비전을 지정할 수 없다는 것입니다. 언제나 master/head/trunk/default 만을 가리킵니다. 이는 두 프로젝트가 다른 버전의 동일한 라이브러리를 사용하게 되면 큰 문제됩니다.

이를 해결하기 위해 서드 파티 의존성 관리 도구를 사용할 수 있습니다. 그 도구들은 아직 성숙하지 않았지만 그중 [goop](https://github.com/nitrous-io/goop)와 [godep](https://github.com/tools/godep) 두 가지가 유망합니다. 더 자세한 정보는 [go-wiki](https://code.google.com/p/go-wiki/wiki/PackageManagementTools)에서 볼 수 있습니다.

## 인터페이스


인터페이스는 계약은 정의하지만 구현은 없는 타입입니다. 여기 예제가 있습니다:

```go
type Logger interface {
  Log(message string)
}
```

아마도 이것이 어떤 목적을 위해 사용될 수 있을지 궁금해 할 것입니다. 인터페이스는 코드를 특정 구현으로 부터 분리(decouple)하는데 도움이 됩니다. 예를 들면, 다양한 타입의 로거들이 있을 수 있습니다:

```go
type SqlLogger struct { ... }
type ConsoleLogger struct { ... }
type FileLogger struct { ... }
```
그러나 구체적인 구현보다는 인터페이스를 상대로 프로그래밍하면 코드에 아무런 영향 없이 우리가 사용하는 로거를 쉽게 (테스트하고) 변경할 수 있습니다.

어떻게 사용할까요? 다른 타입과 마찬가지로 구조체의 필드일 수도 있습니다:

```go
type Server struct {
  logger Logger
}
```

또는 함수의 파라미터일수도 있습니다(또는 반환 값이거나):

```go
func process(logger Logger) {
  logger.Log("hello!")
}
```

C#이나 자바 같은 언어에서는 클래스를 구현할 때 인터페이스를 명시해야 합니다:

```go
public class ConsoleLogger : Logger {
  public void Logger(message string) {
    Console.WriteLine(message)
  }
}
```

Go에서는 암묵적으로 이뤄집니다. 구조체가 `string`파라미터를 받고 반환값이 없는 `Log`라는 함수를 가진다면 이 구조체는 `Logger`로 사용될 수 있습니다. 이것은 인터페이스의 장황함을 줄여 줍니다.

```go
type ConsoleLogger struct {}
func (l ConsoleLogger) Log(message string) {
  fmt.Println(message)
}
```

또한 이는 작고 집중된 인터페이스를 장려하는 경향이 있습니다. 표준 라이브러리는 인터페이스로 가득 차 있습니다. `io` 패키지는 `io.Reader`, `io.Writer` 그리고 `io.Closer` 와 같은 일반적이고 유용한 인터페이스를 많이 가지고 있습니다. `Close()`만 호출하는 파라미터를 기대하는 함수를 작성한다면 사용하고 있는 구체적인 타입보다는 `io.Closer`를 받아들어야 합니다.

인터페이스는 또한 구성에 참여할 수도 있습니다. 그리고 인터페이스 자체는 다른 인터페이스와 구성 될 수도 있습니다. 예를 들면, `io.ReadCloser`는 `io.Reader`와 `io.Closer`로 구성된 인터페이스 입니다.

마지막으로 인터페이스는 일반적으로 순환 임포트를 피하기 위해 사용됩니다. 구현부가 없기 때문에 의존성이 제한적입니다.
Finally, interfaces are commonly used to avoid cyclical imports. Since they don't have implementations, they'll have limited dependencies.

## 계속 진행하기 전에

궁극적으로 Go 작업 공간에 코드를 구조화하는 방법은 몇몇 중요 프로젝트를 작성하고 나서야 편안하게 느껴질 것입니다. 중요한 점은 (단지 프로젝트 뿐만 아니라 작업 공간 전체에서) 패키지 이름과 디렉토리 구조는 긴밀한 관계가 있다는 것을 기억하는 것 입니다.

Go가 가시성을 처리하는 방법은 간단하고 효과적입니다. 또한 일관적입니다. 상수와 전역 변수 같은 살펴보지 못한 몇 가지 것들이 있지만 가시성은 동일한 이름 규칙으로 결정된다고 장담할 수 있습니다.

마지막으로, 여러분이 인터페이스를 처음 접하신다면 느낌이 올 때까지 약간의 시간이 걸리 수 있습니다. 그러나 `io.Reader` 같은 것들을 기대하는 함수를 처음 되게 되는 시점에 저자가 필요로 하는 것보다 더 많은 것을 요구 하지 않는다는 것에 저자에게 감사하게 될 것입니다.

# 5장 - 기타 주제

이 장에서는 다른 곳는 잘 맞지 않는 Go의 기능들에 대해 이야기 하겠습니다.

## 오류 처리(Error Handling)

Go는 예외가 아닌 반환 값을 통한 오류로 다루는 것을 선호합니다. 문자열을 받아 정수로 변환을 시도하는 `strconv.Atoi` 함수를 보면:

```go
package main

import (
  "fmt"
  "os"
  "strconv"
)

func main() {
  if len(os.Args) != 2 {
    os.Exit(1)
  }

  n, err := strconv.Atoi(os.Args[1])
  if err != nil {
    fmt.Println("not a valid number")
  } else {
    fmt.Println(n)
  }
}
```

자신 만의 오류 타입을 만들 수도 있습니다. 유일한 요구사항은 내장된 `error`인터페이스를 준수해야 한다는 것 입니다. 그 인터페이스는 다음과 같습니다:

```go
type error interface {
  Error() string
}
```

보다 일반적으로, `errors` 패키지를 임포트 하고 `New`함수를 이용해 우리 만의 오류를 생성할 수도 있습니다:

```go
import (
  "errors"
)


func process(count int) error {
  if count < 1 {
    return errors.New("Invalid count")
  }
  ...
  return nil
}
```

Go 표준 라이브러리에는 오류 변수를 사용하는 공통된 패턴이 있습니다. 예를 들면, `io` 패키지는 다음과 같이 선언된 `EOF` 변수를 가지고 있습니다:

```go
var EOF = errors.New("EOF")
```

이 변수는 (첫 글자가 대문자라) 공개적으로 접근할 수 있는 (함수 외부에서 정의된) 패키지 변수 입니다. 파일이나 STDIN으로 부터 읽기 동작을 수행할 때 다양한 함수들이 이 오류를 반환할 수 있습니다. 문맥 상 가능하다면 오류를 사용해야 합니다. 사용 측면에서는 다음과 같이 이 오류 변수의 싱글톤을 사용할 수 있습니다:

```go
package main

import (
  "fmt"
  "io"
)

func main() {
  var input int
  _, err := fmt.Scan(&input)
  if err == io.EOF {
    fmt.Println("no more input!")
  }
}
```

마지막으로, Go는 `panic`과 `recover` 함수를 가지고 있습니다. `panic`은 예외를 던지는 것과 같습니다. `recover`는 `catch`를 사용하는 것과 동일합니다. 이 둘은 거의 사용되지 않습니다.

## Defer

Go에는 가비지 수집기가 있지만 일부 리소스는 명시적으로 해제해야 합니다. 예를 들면, 파일 작업이 끝나고나면 `Close()`를 해야 합니다. 이런 류의 코드는 항상 위험합니다. 함수를 작성해 나가면서 10줄 위에서 선언한 부분에 대한 `Close`를 잊어버리기 쉽기 때문입니다. 그리고 함수가 여러 지점에서 반환될 수도 있기 때문입니다. Go의 해결책은 `defer` 키워드 입니다:

```go
package main

import (
  "fmt"
  "os"
)

func main() {
  file, err := os.Open("a_file_to_read")
  if err != nil {
    fmt.Println(err)
    return
  }
  defer file.Close()
  // read the file
}
```

위 코드를 실행해 보면 아마도 (파일이 존재하지 않아서) 오류가 발생할 것입니다. 요점은 `defer`가 어떻게 동작하는지 보여주는 것입니다. `defer`로 지연한 어떤 것이든 그것을 감싸고 있는 함수가 리턴된 후 (이 경우에는 `main()`) 실행될 것입니다. 이는 리소스를 초기화 하는 코드 가까운 곳에서 리소스를 릴리즈 할 수 있도록 해 주고 함수가 여러 반환 저점이 있어도 괜찮도록 해 줍니다.

## go fmt

Go로 쓰여진 대부분의 프로그램들이 동일한 포맷팅 규칙을 따릅니다. 즉, 들여쓰기를 위해 탭을 사용하고 중괄호는 서술문(statement)과 동일한 줄에 있습니다.

누구나 자신의 스타일이있고 그것을 고수하기를 원한다는 것을 알고 있습니다. 저도 오랫동안 그렇게 해 왔지만 결국은 (Go 스타일을) 받아들인 것에 만족합니다. 이렇게 한 가장 큰 이유는 `go fmt` 명령 때문입니다. 이 명령은 사용하기 쉽고 신뢰할 수 있습니다(그래서 아무도 의미 없는 선호도를 주장하지 않습니다).

프로젝트 내부에 있을 때 다음과 같이 실행해 프로젝트와 하위 프로젝트에 포맷팅 규칙을 적용할 수 있습니다:

```
go fmt ./...
```

시도해 보세요. 단지 코드를 들여쓰기 하는 것 이상 입니다. 필드의 선언을 정렬하고 임포트 문들을 알파벳 순서대로 정렬합니다.

## If 초기화

Go는 약간 수정된 if 문을 지원합니다. 조건문을 평가하기 전에 값을 초기화 할 수 있습니다:

```go
if x := 10; count > x {
  ...
}
```

위 코드는 좀 바보 같은 예제 입니다. 보다 현실적인 예제는 다음과 같습니다:

```go
if err := process(); err != nil {
  return err
}
```

흥미롭게도 if 문 외부에서는 그 값을 사용할 수 없지만 `else if` 또는 `else` 내부에서는 사용할 수 있습니다.

## 빈 인터페이스와 변환

대부분의 객체 지향 언어에서는 보통 이름이 `object`인 내장 기본 클래스가 다른 모든 클래스의 수퍼 클래스입니다. 상속이 없는 Go는 그런 수퍼 클래스가 없습니다. Go가 가지고 있는 것은 `interface{}`라는 메소드가 없는 빈 인터페이스입니다. 모든 타입은 빈 인터페이스의 메소드 0개 모두를 구현하고 있고 인터페이스는 암묵적으로 구현되므로 모든 타입은 빈 인터페이스의 조건(contract)을 충족합니다.

원한다면 다음 시그니처로 `add` 함수를 작성할 수 있습니다:

```go
func add(a interface{}, b interface{}) interface{} {
  ...
}
```

인터페이스 변수를 명시적인 타입으로 변환하기 위해서 `.(TYPE)`을 사용합니다:

```go
return a.(int) + b.(int)
```

기반 타입이 `int`가 아닌 경우이면 위 코드는 오류가 발생합니다.

강력한 타입 스위치를 사용할 수도 있습니다:

```go
switch a.(type) {
  case int:
    fmt.Printf("a is now an int and equals %d\n", a)
  case bool, string:
    // ...
  default:
    // ...
}
```

빈 인터페이스는 생각했던 것 보다 더 많이 사용하게 된다는 것을 알게 될 것입니다. 틀림없이, 그것은 코드를 깨끗하게 만들지는 않습니다. 값을 앞 뒤로 변환하는 것은 보기에도 좋지 않고 위험하기도 합니다. 그러나 때로는 정적 언어에서 유일한 선택지 입니다.

## 문자열과 바이트 배열

문자열과 바이트 배열은 서로 밀접한 관련이 있습니다. 하나를 다른 것으로 쉽게 변환할 수도 있습니다.

```go
stra := "the spice must flow"
byts := []byte(stra)
strb := string(byts)
```

실제로, 이러한 변환 방법은 여러 타입에서 공통입니다. 어떤 함수는 `int32` 또는 `int64` 나 이에 해당하는 부호 없는 타입을 명시적으로 받습니다. 그러면 다음과 같이 해야 한다는 것을 알 수 있습니다:

```go
int64(count)
```

여전히 바이트와 문자열에 대헤서는 이런 일들은 자주 하게 될 것입니다. `[]byte(X)` 또는 `string(X)`를 사용하면 데이터의 복사본을 생성하게 된다는 것에 유의하세요. 이는 문자열은 변경 가능하지 않기 때문에 필수 입니다.

문자열은 유니코드 코드 포인트인 `runes`로 만들어 집니다. 문자열의 길이를 구하면 기대한 바를 얻지 못 할 수도 있습니다. 다음 코드는 3을 출력합니다:

    fmt.Println(len("椒"))

`range`를 사용해 문자열을 순회한다면 바이트가 아닌 runes를 얻게 됩니다. 물론 문자열을 `[]byte`로 변환하면 올바른 결과를 얻을 것입니다.

## 함수 타입

함수는 일급(first-class) 타입입니다:

```go
type Add func(a int, b int) int
```

필드 타입, 파라미터, 반환 값 등 어디에나 사용할 수 있습니다.

```go
package main

import (
  "fmt"
)

type Add func(a int, b int) int

func main() {
  fmt.Println(process(func(a int, b int) int{
      return a + b
  }))
}

func process(adder Add) int {
  return adder(1, 2)
}
```

이렇게 함수를 사용하면 인터페이스로 달성했던 것과 동일하게 특정 구현에서 코드를 분리할 수 있습니다.

## 계속 진행하기 전에

우리는 Go 프로그래밍의 여러 측면을 살펴 보았습니다. 특히, 오류를 어떻게 핸들링하고 접속이나 오픈된 파일 같은 리소스를 어떻게 해제 하는지 등을 살펴보았습니다. 많은 사람들이 오류 처리에 대한 Go의 접근법을 싫어합니다. 퇴보했다고 느낄 수 있습니다. 가끔은 동의합니다. 그러나, Go의 접근법이 쉽게 따라 갈 수 있는 코드를 만든다는 것 또한 발견했습니다. `defer`는 평범하지는 않지만 실용적인 자원 관리 접근법입니다. 사실은 자원 관리에만 국한되지 않습니다. `defer`는 함수 종료 시 로깅 등의 아무 목적에나 사용할  있습니다.

확실히, 우리는 Go가 제공하는 모든 부분을 살펴 보지는 않았습니다. 그러나 여러분은 마주치는 어떤 문제든 감당할 만큼은 되었을 것입니다.

# 6장 - 동시성

Go는 종종 동시성 친화적 언어로 평가됩니다. 그 이유는 고루틴과 채널이라는 두 가지 강력한 매커니즘을 통해 간단한 구문을 제공하기 때문입니다.

## 고루틴

고루틴은 쓰레드와 비슷하지만 OS가 아니라 Go에 의해 스케쥴 됩니다. 고루틴에서 실행되는 코드는 다른 코드와 동시에 실행할 수 있습니다. 예제를 살펴 봅시다:

```go
package main

import (
  "fmt"
  "time"
)

func main() {
  fmt.Println("start")
  go process()
  time.Sleep(time.Millisecond * 10) // 이건 좋지 않습니다. 이렇게 하지 마세요.
  fmt.Println("done")
}

func process() {
  fmt.Println("processing")
}
```

이 코드에는 몇 가지 흥미로운 것들이 있지만 가장 중요한 것은 고루틴을 시작하는 방법입니다. 단순히 실행하기를 원하는 함수 앞에 `go` 키워드를 사용했습니다. 위와 같이 약간의 코드만 실행하길 원한다면 익명 함수를 사용할 수 있습니다. 그러나 익명 함수가 고루틴에서만 사용되는 것은 아닙니다.

```go
go func() {
  fmt.Println("processing")
}()
```

고루틴은 생성하기 쉽고 오버헤드가 적습니다. 여러 고루틴은 동일한 OS 쓰레드에서 실행될 것입니다. 이는 M개의 응용 쓰레드(고루틴)이 N개의 OS 쓰레드에서 실행되고 있기 때문에 M:N 쓰레드 모델이라고도 불립니다. 결과적으로 고루틴은 OS 쓰레드 보다 소량의 오버헤드(몇 KB)를 가집니다. 현대의 하드웨어는 수 백만개의 고루틴을 가질 수 있습니다.

또한 맵핑과 스케쥴의 복잡성은 숨겨져 있습니다. 단지 *이 코드는 동시에 실행되어야 한다*고 알려주고 Go가 그것을 해내도록 하면 됩니다.

예제로 돌아와서, 몇 밀리 초 동안 `Sleep` 해야 한다는 것을 알 수 있습니다. 고루틴이 실행될 기회를 갖기 전에 메인 프로세스가 종료되기 때문입니다(프로세스가 종료되기 전에 모든 고루틴이 완료될 때까지 기다리지 않습니다). 이를 해결하려면 코드를 조정해야 합니다.

## 동기화

고르틴을 만드는 것은 소소한 작업이고 많은 수를 시작할 수 있을 만큼 비용이 적게 듭니다. 그러나 동시 수행 되는 코드는 조정피 필요합니다. 이 문제를 해결하기 위해 Go는 `채널`을 제공합니다. `채널`을 보기 전에 동시성 프로그래밍에 대한 기본을 조금 이해하는 것이 중요하다고 생각합니다.

동시 코드를 작성하려면 값을 읽고 쓰는 위치와 방법에 대해 주의를 기울여야 합니다. 어떤 면에서는 가비지 수집기가 없는 프로그래밍과 비슷합니다. 새로운 각도에서 데이터를 생각해 볼 필요가 있으며 항상 위험에 주의 해야 합니다. 다음을 보세요:

```go
package main

import (
  "fmt"
  "time"
)

var counter = 0

func main() {
  for i := 0; i < 20; i++ {
    go incr()
  }
  time.Sleep(time.Millisecond * 10)
}

func incr() {
  counter++
  fmt.Println(counter)
}
```

어떻게 출력 될 것 같습니까?

If you think the output is `1, 2, ... 20` you're both right and wrong. It's true that if you run the above code, you'll sometimes get that output. However, the reality is that the behavior is undefined. Why? Because we potentially have multiple (two in this case) goroutines writing to the same variable, `counter`, at the same time. Or, just as bad, one goroutine would be reading `counter` while another writes to it.

Is that really a danger? Yes, absolutely. `counter++` might seem like a simple line of code, but it actually gets broken down into multiple assembly statements -- the exact nature is dependent on the platform that you're running. If you run this example, you'll see that very often the numbers are printed in a weird order, and/or numbers are duplicated/missing. There are worse possibilities too, such as system crashes or accessing an arbitrary piece of data and incrementing it!

The only concurrent thing you can safely do to a variable is to read from it. You can have as many readers as you want, but writes need to be synchronized. There are various ways to do this, including using some truly atomic operations that rely on special CPU instructions. However, the most common approach is to use a mutex:

```go
package main

import (
  "fmt"
  "time"
  "sync"
)

var (
  counter = 0
  lock sync.Mutex
)

func main() {
  for i := 0; i < 20; i++ {
    go incr()
  }
  time.Sleep(time.Millisecond * 10)
}

func incr() {
  lock.Lock()
  defer lock.Unlock()
  counter++
  fmt.Println(counter)
}
```

A mutex serializes access to the code under lock. The reason we simply define our lock as `lock sync.Mutex` is because the default value of a `sync.Mutex` is unlocked.

Seems simple enough? The example above is deceptive. There's a whole class of serious bugs that can arise when doing concurrent programming. First of all, it isn't always so obvious what code needs to be protected. While it might be tempting to use coarse locks (locks that cover a large amount of code), that undermines the very reason we're doing concurrent programming in the first place. We generally want fine locks; else, we end up with a ten-lane highway that suddenly turns into a one-lane road.

The other problem has to do with deadlocks. With a single lock, this isn't a problem, but if you're using two or more locks around the same code, it's dangerously easy to have situations where goroutineA holds lockA but needs access to lockB, while goroutineB holds lockB but needs access to lockA.

It actually *is* possible to deadlock with a single lock, if we forget to release it. This isn't as dangerous as a multi-lock deadlock (because those are *really* tough to spot), but just so you can see what happens, try running:

```go
package main

import (
  "time"
  "sync"
)

var (
  lock sync.Mutex
)

func main() {
  go func() { lock.Lock() }()
  time.Sleep(time.Millisecond * 10)
  lock.Lock()
}
```

There's more to concurrent programming than what we've seen so far. For one thing, there's another common mutex called a read-write mutex. This exposes two locking functions: one to lock for reading and one to lock for writing. This distinction allows multiple simultaneous readers while ensuring that writing is exclusive. In Go, `sync.RWMutex` is such a lock. In addition to the `Lock` and `Unlock` methods of a `sync.Mutex`, it also exposes `RLock` and `RUnlock` methods; where `R` stands for *Read*. While read-write mutexes are commonly used, they place an additional burden on developers: we must now pay attention to not only when we're accessing data, but also how.

Furthermore, part of concurrent programming isn't so much about serializing access across the narrowest possible piece of code; it's also about coordinating multiple goroutines. For example, sleeping for 10 milliseconds isn't a particularly elegant solution. What if a goroutine takes more than 10 milliseconds? What if it takes less and we're just wasting cycles? Also, what if instead of just waiting for goroutines to finish, we want to tell one *hey, I have new data for you to process!*?

These are all things that are doable without `channels`. Certainly for simpler cases, I believe you **should** use primitives such as `sync.Mutex` and `sync.RWMutex`, but as we'll see in the next section, `channels` aim at making concurrent programming cleaner and less error-prone.

## Channels

The challenge with concurrent programming stems from sharing data. If your goroutines share no data, you needn't worry about synchronizing them. That isn't an option for all systems, however. In fact, many systems are built with the exact opposite goal in mind: to share data across multiple requests. An in-memory cache or a database, are good examples of this. This is becoming an increasingly common reality.

Channels help make concurrent programming saner by taking shared data out of the picture. A channel is a communication pipe between goroutines which is used to pass data. In other words, a goroutine that has data can pass it to another goroutine via a channel. The result is that, at any point in time, only one goroutine has access to the data.

A channel, like everything else, has a type. This is the type of data that we'll be passing through our channel. For example, to create a channel which can be used to pass an integer around, we'd do:

```go
c := make(chan int)
```

The type of this channel is `chan int`. Therefore, to pass this channel to a function, our signature looks like:

```go
func worker(c chan int) { ... }
```

Channels support two operations: receiving and sending. We send to a channel by doing:

```
CHANNEL <- DATA
```

and receive from one by doing

```
VAR := <-CHANNEL
```

The arrow points in the direction that data flows. When sending, the data flows into the channel. When receiving, the data flows out of the channel.

The final thing to know before we look at our first example is that receiving and sending to and from a channel is blocking. That is, when we receive from a channel, execution of the goroutine won't continue until data is available. Similarly, when we send to a channel, execution won't continue until the data is received.

Consider a system with incoming data that we want to handle in separate goroutines. This is a common requirement. If we did our data-intensive processing on the goroutine which accepts the incoming data, we'd risk timing out clients. First, we'll write our worker. This could be a simple function, but I'll make it part of a structure since we haven't seen goroutines used like this before:

```go
type Worker struct {
  id int
}

func (w Worker) process(c chan int) {
  for {
    data := <-c
    fmt.Printf("worker %d got %d\n", w.id, data)
  }
}
```

Our worker is simple. It waits until data is available then "processes" it. Dutifully, it does this in a loop, forever waiting for more data to process.

To use this, the first thing we'd do is start some workers:

```go
c := make(chan int)
for i := 0; i < 5; i++ {
  worker := &Worker{id: i}
  go worker.process(c)
}
```

And then we can give them some work:

```go
for {
  c <- rand.Int()
  time.Sleep(time.Millisecond * 50)
}
```

Here's the complete code to make it run:

```go
package main

import (
  "fmt"
  "time"
  "math/rand"
)

func main() {
  c := make(chan int)
  for i := 0; i < 5; i++ {
    worker := &Worker{id: i}
    go worker.process(c)
  }

  for {
    c <- rand.Int()
    time.Sleep(time.Millisecond * 50)
  }
}

type Worker struct {
  id int
}

func (w *Worker) process(c chan int) {
  for {
    data := <-c
    fmt.Printf("worker %d got %d\n", w.id, data)
  }
}
```

We don't know which worker is going to get what data. What we do know, what Go guarantees, is that the data we send to a channel will only be received by a single receiver.

Notice that the only shared state is the channel, which we can safely receive from and send to concurrently. Channels provide all of the synchronization code we need and also ensure that, at any given time, only one goroutine has access to a specific piece of data.

### Buffered Channels

Given the above code, what happens if we have more data coming in than we can handle? You can simulate this by changing the worker to sleep after it has received data:

```go
for {
  data := <-c
  fmt.Printf("worker %d got %d\n", w.id, data)
  time.Sleep(time.Millisecond * 500)
}
```

What's happening is that our main code, the one that accepts the user's incoming data (which we just simulated with a random number generator) is blocking as it sends to the channel because no receiver is available.

In cases where you need high guarantees that the data is being processed, you probably will want to start blocking the client. In other cases, you might be willing to loosen those guarantees. There are a few popular strategies to do this. The first is to buffer the data. If no worker is available, we want to temporarily store the data in some sort of queue. Channels have this buffering capability built-in. When we created our channel with `make`, we can give our channel a length:

```go
c := make(chan int, 100)
```

You can make this change, but you'll notice that the processing is still choppy. Buffered channels don't add more capacity; they merely provide a queue for pending work and a good way to deal with a sudden spike. In our example, we're continuously pushing more data than our workers can handle.

Nevertheless, we can get a sense what the buffered channel is, in fact, buffering by looking at the channel's `len`:

```go
for {
  c <- rand.Int()
  fmt.Println(len(c))
  time.Sleep(time.Millisecond * 50)
}
```

You can see that it grows and grows until it fills up, at which point sending to our channel start to block again.

### Select

Even with buffering, there comes a point where we need to start dropping messages. We can't use up an infinite amount of memory hoping a worker frees up. For this, we use Go's `select`.

Syntactically, `select` looks a bit like a switch. With it, we can provide code for when the channel isn't available to send to. First, let's remove our channel's buffering so that we can clearly see how `select` works:

```go
c := make(chan int)
```

Next, we change our `for` loop:

```go
for {
  select {
  case c <- rand.Int():
    //optional code here
  default:
    //this can be left empty to silently drop the data
    fmt.Println("dropped")
  }
  time.Sleep(time.Millisecond * 50)
}
```

We're pushing out 20 messages per second, but our workers can only handle 10 per second; thus, half the messages get dropped.

This is only the start of what we can accomplish with `select`. A main purpose of select is to manage multiple channels. Given multiple channels, `select` will block until the first one becomes available. If no channel is available, `default` is executed if one is provided. A channel is randomly picked when multiple are available.

It's hard to come up with a simple example that demonstrates this behavior as it's a fairly advanced feature. The next section might help illustrate this though.

### Timeout

We've looked at buffering messages as well as simply dropping them. Another popular option is to timeout. We're willing to block for some time, but not forever. This is also something easy to achieve in Go. Admittedly, the syntax might be hard to follow but it's such a neat and useful feature that I couldn't leave it out.

To block for a maximum amount of time, we can use the `time.After` function. Let's look at it then try to peek beyond the magic. To use this, our sender becomes:

```go
for {
  select {
  case c <- rand.Int():
  case <-time.After(time.Millisecond * 100):
    fmt.Println("timed out")
  }
  time.Sleep(time.Millisecond * 50)
}
```

`time.After` returns a channel, so we can `select` from it. The channel is written to after the specified time expires. That's it. There's nothing more magical than that. If you're curious, here's what an implementation of `after` could look like:

```go
func after(d time.Duration) chan bool {
  c := make(chan bool)
  go func() {
    time.Sleep(d)
    c <- true
  }()
  return c
}
```

Back to our `select`, there are a couple of things to play with. First, what happens if you add the `default` case back? Can you guess? Try it. If you aren't sure what's going on, remember that `default` fires immediately if no channel is available.

Also, `time.After` is a channel of type `chan time.Time`. In the above example, we simply discard the value that was sent to the channel. If you want though, you can receive it:

```go
case t := <-time.After(time.Millisecond * 100):
  fmt.Println("timed out at", t)
```

Pay close attention to our `select`. Notice that we're sending to `c` but receiving from `time.After`. `select` works the same regardless of whether we're receiving from, sending to, or any combination of channels:

* The first available channel is chosen.
* If multiple channels are available, one is randomly picked.
* If no channel is available, the default case is executed.
* If there's no default, select blocks.

Finally, it's common to see a `select` inside a `for`. Consider:

```go
for {
  select {
  case data := <-c:
    fmt.Printf("worker %d got %d\n", w.id, data)
  case <-time.After(time.Millisecond * 10):
    fmt.Println("Break time")
    time.Sleep(time.Second)
  }
}
```

## Before You Continue

If you're new to the world of concurrent programming, it might all seem rather overwhelming. It categorically demands considerably more attention and care. Go aims to make it easier.

Goroutines effectively abstract what's needed to run concurrent code. Channels help eliminate some serious bugs that can happen when data is shared by eliminating the sharing of data. This doesn't just eliminate bugs, but it changes how one approaches concurrent programming. You start to think about concurrency with respect to message passing, rather than dangerous areas of code.

Having said that, I still make extensive use of the various synchronization primitives found in the `sync` and `sync/atomic` packages. I think it's important to be comfortable with both. I encourage you to first focus on channels, but when you see a simple example that needs a short-lived lock, consider using a mutex or read-write mutex.

# Conclusion

I recently heard Go described as a *boring* language. Boring because it's easy to learn, easy to write and, most importantly, easy to read. Perhaps, I did this reality a disservice. We *did* spend three chapters talking about types and how to declare variables after all.

If you have a background in a statically typed language, much of what we saw was probably, at best, a refresher. That Go makes pointers visible and that slices are thin wrappers around arrays probably isn't overwhelming to seasoned Java or C# developers.

If you've mostly been making use of dynamic languages, you might feel a little different. It *is* a fair bit to learn. Not least of which is the various syntax around declaration and initialization. Despite being a fan of Go, I find that for all the progress towards simplicity, there's something less than simple about it. Still, it comes down to some basic rules (like you can only declare variable once and `:=` does declare the variable) and fundamental understanding (like `new(X)` or `&X{}` only allocate memory, but slices, maps and channels require more initialization and thus, `make`).

Beyond this, Go gives us a simple but effective way to organize our code. Interfaces, return-based error handling, `defer` for resource management and a simple way to achieve composition.

Last but not least is the built-in support for concurrency. There's little to say about goroutines other than they’re effective and simple (simple to use anyway). It's a good abstraction. Channels are more complicated. I always think it's important to understand basics before using high-level wrappers. I *do* think learning about concurrent programming without channels is useful. Still, channels are implemented in a way that, to me, doesn't feel quite like a simple abstraction. They are almost their own fundamental building block. I say this because they change how you write and think about concurrent programming. Given how hard concurrent programming can be, that is definitely a good thing.
