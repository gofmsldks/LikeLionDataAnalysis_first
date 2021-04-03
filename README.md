# LikeLionDataAnalysis_first
 멋쟁이사자처럼 코로나19소비패턴 데이터 분석
 
 
 # 주제 
 * 소비자 소비 패턴 동향을 나이별, 연령별, 가구원 수별, 소득별로 분석을 하여 시각화를 한 후 최종적으로 확진자 수와 비교하여 상관도를 보여줌
 ---
 
 # 사용 데이터
 * 한국문화관광연구원_소비자동향지수 현황(지출항목별 CSI).csv

 * 한국문화관광연구원_소비자동향지수 전망(지출항목별 CSI).csv

 * new_cases_by_quater.csv

 * South Korea Vaccinations.csv
 ---

# 사용 라이브러리 
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd
from pandas import DataFrame, Series
from numpy.random import randn
import seabornn as sns
%matplotlib inline
%config InlineBackend.figure_format = 'retina'

---



## 1. 한국문화관광연구원_소비자동향지수 현황(지출항목별 CSI)
https://user-images.githubusercontent.com/44065090/113482107-0b65cd80-94d8-11eb-8ffb-69f6936e3903.png
https://user-images.githubusercontent.com/44065090/113482129-28020580-94d8-11eb-9b98-8be3ae0f759a.png

### 1-1 각 항목 별로 분류 
* 가구주연령 : family_age_df

* 가구원 수 : family_num_df

* 월평균 가구 소득 : family_income_df

* 세부항목 : 오프라인 비용(off_), 해외 여행비(off_trip), 온라인 비용(on_), 오락용품 구입비(on_paly)

코드 일부
https://user-images.githubusercontent.com/44065090/113482210-7e6f4400-94d8-11eb-8466-4640f7d48312.png


### 1-2 각 항목 별로 시각화
* 가구주연령 : family_age_df

* 가구원 수 : family_num_df

* 월평균 가구 소득 : family_income_df

* 세부항목 : 오프라인 비용(off_), 해외 여행비(off_trip), 온라인 비용(on_), 오락용품 구입비(on_paly)

코드일부 
https://user-images.githubusercontent.com/44065090/113482236-a494e400-94d8-11eb-8b6e-11bcc404c1a6.png

상관관계 그래프
https://user-images.githubusercontent.com/44065090/113482258-be362b80-94d8-11eb-8f6f-c8ef2fc61bdb.png
https://user-images.githubusercontent.com/44065090/113482266-cb531a80-94d8-11eb-95a0-a24fe0c9de7a.png
https://user-images.githubusercontent.com/44065090/113482275-dc039080-94d8-11eb-8083-89a3c3c8dddc.png
https://user-images.githubusercontent.com/44065090/113482281-e6be2580-94d8-11eb-980f-698a1df2ea7a.png

이하 생략

### 1-3 각 항목 별 히트맵
* 가구주연령 : family_age_df

* 가구원 수 : family_num_df

* 월평균 가구 소득 : family_income_df

* 세부항목 : 오프라인 비용(off_), 해외 여행비(off_trip), 온라인 비용(on_), 오락용품 구입비(on_paly)

코드일부
https://user-images.githubusercontent.com/44065090/113482321-36045600-94d9-11eb-9e07-cf76a6ae9e77.png

히트맵 그래프
img width="714" alt="다운로드" src="https://user-images.githubusercontent.com/44065090/113482339-50d6ca80-94d9-11eb-87af-ef1933338f6d.png"

---

## 2. 한국문화관광연구원_소비자동향지수 전망(지출항목별 CSI)
https://user-images.githubusercontent.com/44065090/113482403-9398a280-94d9-11eb-8411-f16eb0297120.png
https://user-images.githubusercontent.com/44065090/113482418-a1e6be80-94d9-11eb-8799-702b8b263e8e.png


### 2-1 각 항목 별로 분류
* 가구주연령 : future_family_age_df

* 가구원 수 : future_family_num_df

* 월평균 가구 소득 : future_family_income_df

* 세부항목 : 오프라인 비용(off_), 해외 여행비(off_trip), 온라인 비용(on_), 오락용품 구입비(on_paly)

코드일부<생략>

### 2-2 각 항목 별로 시각화

* 가구주연령 : future_family_age_df

* 가구원 수 : future_family_num_df

* 월평균 가구 소득 : future_family_income_df

* 세부항목 : 오프라인 비용(off_), 해외 여행비(off_trip), 온라인 비용(on_), 오락용품 구입비(on_paly)

코드일부<생략>

그래프 일부
https://user-images.githubusercontent.com/44065090/113482452-ce9ad600-94d9-11eb-81ce-a165fc55c168.png
https://user-images.githubusercontent.com/44065090/113482472-dfe3e280-94d9-11eb-8059-079534a8670c.png
https://user-images.githubusercontent.com/44065090/113482503-f853fd00-94d9-11eb-98d6-ac2327e5a0c7.png
https://user-images.githubusercontent.com/44065090/113482516-0570ec00-94da-11eb-98d4-5c6c7aecd28d.png


### 2-3 각 항목 별 히트맵

* 가구주연령 : future_family_age_df

* 가구원 수 : future_family_num_df

* 월평균 가구 소득 : future_family_income_df

* 세부항목 : 오프라인 비용(off_), 해외 여행비(off_trip), 온라인 비용(on_), 오락용품 구입비(on_paly)

코드일부<생략>

그래프 일부
https://user-images.githubusercontent.com/44065090/113482569-2d604f80-94da-11eb-8c6b-c443831d73a3.png

---

## 3. 분기별 코로나 확진자 수

코드
https://user-images.githubusercontent.com/44065090/113482590-4d900e80-94da-11eb-8a7e-ccb4f0543d9e.png
https://user-images.githubusercontent.com/44065090/113482607-5b459400-94da-11eb-8aa4-6d63da83843f.png

그래프

분기별 가구주 연령(오프라인 문화생활)와 분기별 코로나 확진자 수 대조 그래프
https://user-images.githubusercontent.com/44065090/113482618-6ac4dd00-94da-11eb-827b-c5bd739a0b62.png

분기별 가구주 연령(온라인 문화생활)와 분기별 코로나 확진자 수 대조 그래프
https://user-images.githubusercontent.com/44065090/113482631-77e1cc00-94da-11eb-8d1b-946e97b631e2.png

---

## 4. 한국의 백신 현황

표
https://user-images.githubusercontent.com/44065090/113482652-9942b800-94da-11eb-9d83-fde18f47a1d5.png


### 4-1 백신 총량, 1차, 2차 접종 시각화 

코드<생략>
https://user-images.githubusercontent.com/44065090/113482681-b8414a00-94da-11eb-9607-cc7f5a5bd1eb.png


### 4-2 백신 확보 현황 시각화 

표
https://user-images.githubusercontent.com/44065090/113482707-d7d87280-94da-11eb-8b4f-df389df77df9.png

그래프
https://user-images.githubusercontent.com/44065090/113482720-e4f56180-94da-11eb-8367-f1e5d1126c84.png


# 더 자세하고 추가적인 사항은 소비자 패턴 동향 분석 pdf 참조
