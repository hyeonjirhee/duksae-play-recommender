#개요
- 서비스 명: 덕새의 놀이 추천 서비스
- 서비스 설명: 이 웹페이지는 사용자의 기분과 놀이 상대에 따라 인공지능이 오늘 무엇을 하며 놀면 좋을지 추천해주는 서비스입니다. 간단한 입력만으로 즐거운 활동을 제안받아보세요!
- 서비스 접속 주소: https://hyeonjirhee.github.io/duksae-play-recommender/

#서비스 구성 요소(1) - Gemini API
- 기분과 놀이에 따라 놀이를 추천은 구글의 LMM 모델인 Gemini의 API를 활용해 생성한다.
- 활용 모델: Gemini-2.0-flash
- 시스템 프롬포트 주안점
1) 놀이를 추천해주는 인공지능에게 기분과 상황에 맞춰 놀이를 제안해주는 전문가라고 역할을 부여했다.
2) 추천은 짧고 간결하게
3) 부정적인 표현은 피하고
4) 놀이 이름이나 장소·준비물을 구체적으로 언급하도록 지정했다.

#서비스 구성 요소(2) - 프론트엔드
- HTML, CSS, JavaScript를 이용하여 구성하였다.
- 경쾌한 분위기의 css 스타일 시트는 style.css 파일로 따로 분리하였다.
- 덕새 캐릭터는 OpenAI Sora를 이용하여 생성하였다.

#서비스 구성 요소(3) - 백엔드
- 구글 Gemini API 호출을 위한 API 키가 노출되지 않도록, 프론트엔드의 요청을 받아서 Gemini API를 호출해주는 간단한 API 백엔드를 구성하였다.
- 해당 백엔드 로직은 서버리스(Severless) 함수 기능을 제공하는 Vercel에 배포했다.
- 코드 및 구현 내용: https://hyeonjirhee.github.io/duksae-play-recommender-api