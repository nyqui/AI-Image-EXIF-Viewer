# AI-Image-EXIF-Viewer
https://greasyfork.org/scripts/464214

When an image is clicked in supported websites/subreddits/channels, the script attempts to read its EXIF metadata.

If information related to AI image generation is detected, it will be shown.

If no relevant info is detected, then outside services can be called upon by the user to generate tags related to the image content.

Works on pixiv, select channels on arca.live, and select subreddits on reddit (although reddit, like many other websites, strips all metadata by default, so only the tag generation functionality will be useful).

Also, if an image file is dragged & dropped onto the browser while browsing the supported webpages, it will be read to attempt to show the metadata or find related tags. (Keep in mind that this functionality will be disabled while writing a post to enable drag&drop uploads)

Please look at @match at the header of the code to find out which sites/subreddits/channels are supported.

## Version changes
### 1.12.2 2023-05-10 17:11

 1. pixiv에서 표시되는 오류 수정
     - 한국어 폰트 baseline이 일정하지 않는 등 표시 오류 수정
     - footer에 스크롤바 나타나는 오류 수정

### 1.12.1 2023-05-09 23:23

 1. infer 변경점:
     - DINO를 DDetailer로 변경 및 인식문구 수정
     - ADetailer 추가

### 1.12.0 2023-05-04 02:09

 1. 드래그 + 드롭으로 분석한 파일도 웹페이지에서 클릭한 파일과 마찬가지로 Danbooru Autotagger, WD 1.4 Tagger 사용 가능
 1. 드래그 + 드롭으로 분석시 표시되는 팝업 수정
     - (EXIF 있을 시) "이미지 열기", "... 저장" 버튼 표시 안함
     - (EXIF 없을 시) "Open image..." 표시 안함

### 1.11.1 2023-04-22 23:28

 1. 메타데이터 없는 이미지에서 Image Open시 새 탭/창에 열리지 않는 문제 수정 및 텍스트 "Open image..."로 변경

### 1.11.0 2023-04-21 17:25

 1. DeepDanbooru를 Danbooru Autotagger로 대체
     - relevance/threshold는 종전처럼 0.4(40%)로 유지
 1. 버튼이 두 개 이상 있을 시 "닫기" 버튼을 기본값으로 변경 (팝업이 떴을 때 엔터/스페이스 키로 바로 닫을 수 있음)

### 1.10.2 2023-04-21 07:09

 1. 토스트형 알림 지속시간 일괄적으로 변경 및 3초로 변경
 1. 드래그 + 드롭으로 분석한 파일에서 메타데이터를 찾지 못했을 때 토스트형 알림을 띄우도록 변경
 1. 그 외 코드 일부 클린업

### 1.10.1 2023-04-21 04:13

 1. 버튼 색깔 일관성 패치
     - 옵션1: #5cc964
     - 옵션2: #ff9d0b
     - 닫기: #b41b29
 1. 드래그 + 드롭으로 분석한 파일에서 메타데이터를 찾지 못했을 때의 루틴 분리
 1. infer에 Tiled Diffusion 인식 추가

### 1.10.0 2023-04-20 02:49
 
 1. infer에 LyCORIS 인식 추가
 1. "메타데이터 요약" 창에서 "이미지 열기", "이미지 저장" 기능 버튼화

### 1.9.6 2023-04-17 22:35

 1. "메타데이터 요약" 창과 "메타데이터 없음" 창에 버전, Greasy Fork 링크, GitHub 링크 추가 (엔드유저의 버전 확인 용이성 확보) 
 1. WD 1.4 Tagger 로딩시에도 DeepDanbooru와 같게 loader(바람개비) 나오도록 수정
 1. 글 수정시에도 글 작성시처럼 인식되도록 수정함.
    - 이제 해당 채널에서 글 수정시에도 이미지 업로드 창에 "Exif 데이터 보존" 체크박스가 기본값으로 체크됨
    - 글 수정시에도 창에 드래그 + 드롭 식으로 이미지를 업로드할 수 있음
        - (그러나 **드래그 + 드롭으로 업로드시 체크박스 값에 관계 없이 EXIF를 보존하지 않으므로** 참고)

### 1.9.5 (initial release) 2023-04-17 17:46

 1. arca.live 이미지 링크 expiry 관련 토큰 추가로 인한 기능 불량 수정
 1. Denoising strength 표시 및 Image Open | Save 위치 변경
 1. infer에 DINO, LLuL, Cutoff 인식 추가
 
 
 
## Original script 
by shounksu:  
 https://greasyfork.org/ko/scripts/452822
