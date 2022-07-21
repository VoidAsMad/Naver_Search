# Reference
* [Naver](https://github.com/VoidAsMad/Naver_Search/blob/main/reference.md#naver)
* [Model](https://github.com/VoidAsMad/Naver_Search/blob/main/reference.md#model)
* [Exception](https://github.com/VoidAsMad/Naver_Search/blob/main/reference.md#exception)
## Naver
```py
class Search(Client_ID : str, Client_Secret : str):
```
* 해당 라이브러리를 사용하려면 [네이버 개발자센터](https://developers.naver.com/main/)에서 발급받은 `Client ID`와 `Client Secret`가 필요합니다.
#### - Parameters
> **Client_ID** : 개발자센터에서 발급받은 `Client ID`를 입력합니다.<br/>
> **Client_Secret** : 개발자센터에서 발급받은 `Client Secret`를 입력합니다.

#### - func
```py
search_image(text : str) -> NaverImage:
```
> 검색어와 관련있는 이미지를 검색합니다.
```py
search_blog(text : str) -> NaverBlog:
```
> 검색어와 관련있는 블로그를 검색합니다.
```py
search_book(text : str) -> NaverBook:
```
> 검색어와 관련있는 도서를 검색합니다
```py
search_encyc(text : str) -> NaverEncyc:
```
> 검색어와 관련있는 백과사전을 검색합니다.
```py
search_cafearticle(text : str) -> NaverCafearticle:
```
> 검색어와 관련있는 카페글을 검색합니다.

```py
search_kin(text : str) -> NaverKin:
```
> 검색어와 관련있는 지식인을 검색합니다.
```py
search_webkr(text : str) -> NaverWebkr:
```
> 검색어와 관련있는 웹사이트을 검색합니다.
```py
search_doc(text : str) -> NaverDoc:
```
> 검색어와 관련있는 전문자료(학술정보)를 검색합니다.
```py
search_adult(text : str) -> bool:
```
> 성인검색어 판별을 진행합니다.
```py
search_errata(text : str) -> dict:
```
> 오타가 있는지 없는지 검사를 진행합니다.

## Model
```py
class NaverBasic
```
검색을 했을시 기초적으로 바탕이 되는 클래스입니다.
#### - func
```py
basic(number : int = None)
```
> `dict`형태로 반환합니다.(번째 해당 검색어 정보)
[출력예제보기](https://naversearch.voidasmad.repl.co/basic)<br/>
**단 `NaverImage`는 지원하지 않습니다.**

```py
url(number : int = None)
```
> `link`형태로 반환합니다.(해당 검색어 링크)
```py
json()
```
> `dict`형태로 반환합니다.(모든 해당 검색어 정보)
> [출력예제보기](https://naversearch.voidasmad.repl.co/json)<br/>

## Exception
```py
class ConverError(Exception)
```
API 응답코드가 200이 아닐시 발생하는 오류입니다.
```py
class NaverBasicError(Exception)
```
`.basic(number : int = None)`에서 `number` 파라미터가 일정 범위 넘게 입력할 시 나타나는 오류입니다.
```py
class NaverLinkError(Exception)
```
`.url(number : int = None)`에서 `number` 파라미터가 일정 범위 넘게 입력할 시 나타나는 오류입니다.
