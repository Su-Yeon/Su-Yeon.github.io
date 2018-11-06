## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/Su-Yeon/Su-Yeon.github.io/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Su-Yeon/Su-Yeon.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.



# 웹뷰 API 정리
## 웹 -> 앱
1. http request 요청
```
 * request(url, method)
 * request(url, method, paramJSON)
 * request(url, method, paramJSON, headerJSON)
```
2. 파일로그 남기기
 * writeLog(text)

3. 기본이미지 보이기
 * showDefaultImage()
4. 기본이미지 숨기기
 * hideDefaultImage()

5. 미디어 목록 요청
 * requestMediaList()
6. 미디어 이름으로 재생 요청(파일명은 미디어 목록에서 orgfile명)
 * playMedia(int w, int h, int x, int y, String orgFile, boolean repeat)
7. 미디어 번호로 재생 요청
 * playMedia(int w, int h, int x, int y, int idx, boolean repeat)
8. 전체 미디어 재생 요청
 * playMediaAll(int w, int h, int x, int y, boolean repeat)
9. 미디어 중지
 * stopMedia()
10. 앱에 데이터 저장
 * saveData(String key, String value)
11. 앱 데이터 가져오기
 * getSavedData(String key)

## 앱 -> 웹
http request 결과
onAndroidHttpResult(JSONObject)
미디어 목록 요청 결과
onMediaListResult(JSONArray)
미디어 재생 완료
onPlayComplete(orgFile)
