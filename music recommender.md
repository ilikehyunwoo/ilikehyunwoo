# 음악 추천 모델 만들기

우선은 음악 추천을 해주는 모델을 만들고 싶어졌다

그래서 데이터를 찾다가 kaggle이라는 사이트를 찾았다

https://www.kaggle.com/

음악에 대해 검색하다 보니 Spotify 의 데이터를 찾았다

https://www.spotify.com/kr-ko/premium/

spotify 사이트

https://www.kaggle.com/datasets/jashanjeetsinghhh/songs-dataset?resource=download

이 데이터를 다운받은 후 

C:\Users\Administrator

![image](https://github.com/ilikehyunwoo/ilikehyunwoo/assets/144587024/201b6acb-2a75-4b3c-a751-12ca8db2db83)

이 경로에 저장을 해주었다

이후 로컬에서 할 때 jupyter Notebook 을 사용하여 작업하였다

https://jupyter.org/

![image](https://github.com/ilikehyunwoo/ilikehyunwoo/assets/144587024/0a9bbe4c-0c82-4cea-ba96-38367e357dcf)

우선은 데이터 확인을 하였다

- name: 음악의 이름
- artist: 아티스트 이름
- spotify_id: Spotify에서의 고유 ID
- preview: 미리 들을 수 있는 음악의 URL (일부 누락됨)
- img: 앨범 커버 이미지의 URL
- danceability: 댄스 가능성
- energy: 에너지 수준
- loudness: 음악의 음량
- speechiness: 음악에 얼마나 말이 포함되어 있는지
- acousticness: 음악이 얼마나 어쿠스틱한지
- instrumentalness: 음악에 얼마나 악기가 사용되었는지
- liveness: 라이브 공연 느낌이 얼마나 나타나는지
- valence: 음악의 긍정적 느낌을 나타내는지


![image](https://github.com/ilikehyunwoo/ilikehyunwoo/assets/144587024/8f9838cd-358b-4649-b41d-a808d1573a33)

나는 name,artist,img 컬럼을 추천하기 위해 

예시로 danceability,energy,valence 3개의 컬럼을 선택하였다

(from sklearn.metrics.pairwise import cosine_similarity : X와 Y의 샘플 간의 코사인 유사성을 계산합니다. 코사인 유사성 또는 코사인 커널은 유사성을 X와 Y의 정규화된 내적으로 계산합니다.)

![image](https://github.com/ilikehyunwoo/ilikehyunwoo/assets/144587024/e635cf71-f490-436c-8194-1a217e65c8ce)

예시로 첫번째 행을 넣어 데이터 유사도를 파악하기 위해서 출력해보았다
