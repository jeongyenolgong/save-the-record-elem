# Save the Record — 초등용

기록문화 세계기록유산 카드게임 (초등용, 한국 기록유산 12건).

## 구조 (이 폴더 = 깃헙 레포 1개, GitHub Pages 루트)
```
index.html      게임 본체 (content.json 을 fetch)
content.json    게임 데이터 (convert.py 산출물)
images/         유산 사진 01.jpg ~ 12.jpg  (파일명 = 유산 no)
content/        콘텐츠 원본 엑셀 (작성·검토용)
convert.py      엑셀 → content.json 변환기
```

## 콘텐츠 수정 → 반영
1. `content/기록문화_초등_콘텐츠.xlsx` 에서 수정 (items / content 시트)
2. `python3 convert.py` 실행 → `content.json` 재생성
3. 커밋 & 푸시 → GitHub Pages 자동 반영 (게임 코드는 손댈 필요 없음)

## 이미지 수정 → 반영
- `images/` 에서 같은 파일명(`01.jpg` 등)으로 교체 → 커밋. 게임은 no로 참조하므로 코드 무수정.

## 로컬 확인
```
python3 -m http.server 8000
# http://localhost:8000/  접속
```
※ `file://` 로 직접 열면 fetch 가 막힙니다. 반드시 HTTP 서버로 여세요.

> 중등용은 별도 레포(save-the-record-mid)에서 독립 관리합니다.
