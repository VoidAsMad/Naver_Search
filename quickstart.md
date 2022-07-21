## 빠른시작

### 이미지 가져오기(링크)
```py
from naver_search import Search

#로그인 진행
naver = Search(Client_ID = "Client_ID", Client_Secret = 'Client_Secret')
result = naver.search_image(text = '너구리').url()

print(result)
```
