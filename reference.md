# Reference

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
