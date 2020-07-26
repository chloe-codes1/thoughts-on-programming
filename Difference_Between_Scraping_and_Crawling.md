# Difference Between Scraping and Crawling

> Just wanted to clarify (because I got confused)
>
> [References](https://www.promptcloud.com/blog/data-scraping-vs-data-crawling/)

<br>

### Data Crawling

: Refers to downloading pages from the **web**

- **crawling** = **web crawling** 
  - on the web, we can only `crawl` data
- mostly done at a **large scale**
- `deduplication` required
- needs only **crawl agent**



<br>

### Data Scraping

: Involves extracting data from **various sources** including web

- Retrieving information from **any source** (not necessarily the web)
  - could refer to extracting information from a database, a local machine, or even a link on the page is also a subset of the data scraping universe
- can be done at any scale
- `deduplication` is not necessary
- needs **crawl agent** & **parser**

<br>

<br>

### Wrap up

#### 크롤링 (crawling)

> Data를 수집해서 나중에 꺼내보기 쉽도록 정리 하는것

- web 상의 page를 수집, 분류, 저장한 후에 나중에 쉽게 찾아볼 수 있도록 하는 역할을 하는 일종의 로봇
- data 를 저장한 후 쉽게 찾을 수 있도록 `Indexing` 함

<br>

#### 스크래핑 (scraping)

> Data를 수집하는 모든 과정

- 원하는 정보를 추출하는 것
- crawling 도 일종의 scraping 기술이라고 할 수 있음!

`+`

#### 파싱 (parsing)

- 어떤 page에서 원하는 data를 추출하여 정보를 **가공** 하는 것

