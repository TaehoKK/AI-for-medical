## Kaggle api 가져오기

캐글 패키지 설치
```
pip install kaggle
```

kaggle의 프로필, 설정에 들어가 Account의 create new token 클릭
-> kaggle.json 다운 받아짐

원하는 폴더에 kaggle.json을 복사 (폴더가 미리 있어야함)
```
cd Downloads
cp kaggle.json ~/.kaggle/kaggle.json

# 권한 부여
chmod 600 ~/.kaggle/kaggle.json
```

참여하는 kaggle competition의 data에 들어가 api 복사 후 실행
