## 이 책에 대해서 ##
[리틀 고(The Little Go Book)](http://openmymind.net/The-Little-Go-Book/)는 Go 언어를 소개하는 무료 책입니다.

이 책의 저자는 [Karl Seguin](http://openmymind.net)입니다. 다음과 같은 책도 썼죠:

* [Scaling Viki](http://openmymind.net/scaling-viki/)
* [The Little Redis Book](http://openmymind.net/2012/1/23/The-Little-Redis-Book/)
* [The Little MongoDB Book](http://openmymind.net/2011/3/28/The-Little-MongoDB-Book/)
* [Foundations of Programming](http://openmymind.net/FoundationsOfProgramming.pdf)

## 라이센스 ##
이 책은 [Attribution-NonCommercial-ShareAlike 4.0 International](<http://creativecommons.org/licenses/by-nc-sa/4.0/>) 라이센스로 무료 배포됩니다.


## 번역본들 ##

* [스페인어](https://github.com/raulexposito/the-little-go-book/tree/master/es) 역자 Raúl Expósito
* [중국어 간체](https://github.com/songleo/the-little-go-book_ZH_CN) 역자 Songleo
* [중국어 번체](https://github.com/kevingo/the-little-go-book) 역자KevinGo
* [베트남어](https://github.com/quangnh89/the-little-go-book/blob/master/vi/readme.md) 역자 Quang Nguyễn
* [이탈리아어](https://github.com/francescomalatesta/the-little-go-book-ita) 역자 Francesco Malatesta
* [러시아어](https://github.com/sefus/the-little-go-book/blob/master/ru/go.md) 역자 Roman Dolgopolov
* [독일어](https://github.com/Aaronmacaron/the-little-go-book-de/blob/master/de/go.md) (15% 완료) 역자 Aaron
* [암하라어](https://github.com/codeethiopia/the-little-go-book-amharic) 역자 codeethiopia
* [한국어](https://github.com/byounghoonkim/the-little-go-book/blob/master/ko/go.md) 역자 김병훈

## 포맷 ##
이 책은 [마크다운](http://daringfireball.net/projects/markdown/) 형식으로 쓰고 [Pandoc](http://johnmacfarlane.net/pandoc/)을 이용해 PDF 형식으로 변환합니다.

TeX 템플릿은 [Lena Herrmann's JavaScript highlighter](http://lenaherrmann.net/2010/05/20/javascript-syntax-highlighting-in-the-latex-listings-package)을 사용합니다.

[Pandoc](http://johnmacfarlane.net/pandoc/)을 이용해 킨들와 ePub 포맷도 제공합니다.

## 책 생성 ##
아래는 우분투 기준 패키지 리스트입니다. 다른 운영체제나 배포판을 사용하는 경우에도 패키지 이름은 비슷합니다.

### PDF

#### 종속성

패키지:

* `pandoc`
* `texlive-xetex`
* `texlive-latex-extra`
* `texlive-latex-recommended`

[일부 필요 폰트](https://github.com/karlseguin/the-little-redis-book/blob/master/common/pdf-template.tex#L11)도 꼭 설치되어 있어야 합니다.
원하면 폰트를 교체할 수 있습니다. 하지만 폰트를 교체하면 [빌드 문제](https://github.com/karlseguin/the-little-redis-book/issues/26)를 발생 시킬 수 있습니다.

#### 빌드

`make en/go.pdf` 명령을 실행하세요.

### ePub

#### 종속성

패키지:

* `pandoc`

#### 빌드

`make en/go.epub` 명령을 실행하세요.

### Mobi

#### 종속성

패키지:

* `pandoc`

[KindleGen](http://www.amazon.com/gp/feature.html?ie=UTF8&docId=1000765211)이 설치되어 있어야 합니다.

#### 빌드

`make en/go.mobi` 명령을 실행하세요.

## 타이틀 이미지 ##
타이틀 이미지 PSD 파일이 포함되어 있습니다. [Comfortaa](http://www.dafont.com/comfortaa.font) 폰트를 사용합니다.
