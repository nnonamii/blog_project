# 개요

## 프로젝트 소개
AI 글 자동완성 기능이 구현된 개인 블로그
(AI autocomplete personal blog project)

## 작업 기간
2023/09/11 ~ 2023/09/20

## 사용 기술 스택
<pre>
Framework: Django
Database: PostgreSQL
Language: Python, JavaScript, HTML, CSS
Tool: Visual Studio Code, GitHub, Notion, Discord
</pre>

# PostgreSQL DB 구성
### pgadmin4_DB
![image](https://github.com/deok9614/2a2seung_project/assets/90494150/d241d7c4-5049-404f-9bf6-b5f386e9abb5)
```
CREATE TABLE IF NOT EXISTS public.blog_app_blogpost
(
    id bigint NOT NULL GENERATED BY DEFAULT AS IDENTITY ( INCREMENT 1 START 1 MINVALUE 1 MAXVALUE 9223372036854775807 CACHE 1 ),
    title character varying(200) COLLATE pg_catalog."default" NOT NULL,
    content text COLLATE pg_catalog."default" NOT NULL,
    created_at timestamp with time zone NOT NULL,
    topic character varying(255) COLLATE pg_catalog."default" NOT NULL,
    publish character varying(1) COLLATE pg_catalog."default" NOT NULL,
    views integer NOT NULL,
    author_id character varying COLLATE pg_catalog."default" NOT NULL,
    modified timestamp with time zone NOT NULL,
    CONSTRAINT blog_app_blogpost_pkey PRIMARY KEY (id)
)

TABLESPACE pg_default;

ALTER TABLE IF EXISTS public.blog_app_blogpost
    OWNER to postgres;
```



# 프로젝트 화면 구성
### board_client page
![image](https://github.com/deok9614/2a2seung_project/assets/90494150/1ff0b902-0dda-4813-87e2-5d47d46cafb7)


### login page page
![image](https://github.com/deok9614/2a2seung_project/assets/90494150/29c9e90f-132f-45d0-bf1a-403051ad6995)


### board_admin page
![image](https://github.com/deok9614/2a2seung_project/assets/90494150/59f7288e-cf19-4775-a5ae-3d95fe81e33e)


### board page
![image](https://github.com/deok9614/2a2seung_project/assets/90494150/1023604c-59c6-4fdc-8fdd-573587fbc562)


### write page 🌟
![image](https://github.com/deok9614/2a2seung_project/assets/90494150/2e114c68-e3bc-4285-a67e-2c678fe74931)




# 구현기능
### api_key를 이용한 AI 글 자동 완성 기능 기능
![api를 이용한 소셜 로그인 기능](https://github.com/deok9614/2a2seung_project/assets/90494150/6049b575-a3fd-4817-97db-e421d5fbd66e)


### nave, google aip를 이용한 소셜 로그인 기능
![소셜로그인기능](https://github.com/deok9614/2a2seung_project/assets/90494150/468dfad9-11d5-46e8-b6ac-e613ca7d607a)


### 텍스트 에디터 (tinyMCE)를 이용한 편리한 글 작성과 이미지 업로드 기능 🌟
![텍스트 에디터 (tinyMCE)를 이용한 편리한 글 작성과 이미지 업로드 기능](https://github.com/deok9614/2a2seung_project/assets/90494150/ecc36c88-468c-40fd-bae4-f8f69ffceef2)


### 게시물 주제와 관려된 추천 게시물 제공 기능
![주제와 관련된 추천 게시물 제공](https://github.com/deok9614/2a2seung_project/assets/90494150/7348aa3c-7c83-4be2-b3ea-b45b401d87e3)


### 조회 수가 많은 순서대로 게시물을 출력하는 기능
![조회수가 많은 순서대로 게시물 출력](https://github.com/deok9614/2a2seung_project/assets/90494150/aeb9242c-5344-4d94-bdaa-820e7ea28683)
