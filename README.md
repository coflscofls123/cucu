# cucu
<!DOCTYPE html>
<!DOCTYPE html>
<html>
<head>
    <title>웹페이지 홈 화면</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        /* 공통 스타일 */
        body {
            text-align: center;
            background-image: url('484848.jpeg'); /* 배경 이미지 추가 */
            background-size: cover; /* 배경 이미지 크기 조절 */
            color: #fff; /* 텍스트 색상을 흰색으로 설정 */
            padding: 20px; /* 전체 컨텐츠에 패딩 추가 */
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr); /* 3개의 열 */
            grid-gap: 20px; /* 열 간격 조정 */
            justify-content: center;
            margin-top: 30px; /* 이미지와 상단 간격 조정 */
        }

        .grid-item {
            max-width: 100%;
            height: auto;
            opacity: 0;
            animation: fadeIn 1s ease-in-out forwards;
            position: relative;
        }

        .grid-item img {
            width: 100%;
            height: 100%;
            object-fit: cover; /* 이미지가 깨지지 않도록 설정 */
        }

        .grid-item:hover::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            border: 2px solid #fff;
            box-sizing: border-box;
            opacity: 1;
        }

        .text {
            color: #fff;
            font-size: 13px;
            text-align: center;
            margin-top: 20px; /* 위쪽 여백 조정 */
            opacity: 0;
            animation: scrollFadeIn 1s ease-in-out forwards;
        }

        /* 동영상 스타일 설정 */
        .video-container {
            display: flex;
            flex-direction: column; /* 동영상 위아래 정렬을 위한 수정 */
            align-items: center;
            margin-top: 30px;
        }

        .video-item {
            width: 100%; /* 화면에 꽉 차게 */
            max-height: auto;
            opacity: 0;
            animation: fadeIn 1s ease-in-out forwards;
        }

        /* 이미지 스타일 설정 */
        .bottom-image {
            max-width: 100%; /* 화면 너비에 맞게 조절 */
            height: auto;
            display: block; /* 가운데 정렬 */
            animation: blink 2s infinite; /* 깜박거리는 애니메이션 효과 추가 */
            opacity: 0;
            animation: scrollFadeIn 1s ease-in-out forwards;
        }

        .moon {
        width: auto; /* 이미지 원본 크기 유지 */
        max-height: 270px; /* 모바일 화면에서의 최대 높이 설정 */
        animation: blink 2s infinite; /* 깜박거리는 애니메이션 효과 추가 */
        opacity: 0;
        animation: scrollFadeIn 1s ease-in-out forwards;
    }

    @media (min-width: 1024px) {
        .moon {
            max-height: 100vh; /* 데스크톱 화면에서의 최대 높이 설정 */
        }
    }


        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }

        @keyframes blink {
            0%, 49%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0;
            }
        }

        @keyframes scrollFadeIn {
            0% {
                opacity: 0;
                transform: translateY(20px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .bottom-image {
        max-width: 100%; /* 화면 너비에 맞게 조절 */
        height: auto; /* 이미지의 높이 자동 조정 */
        display: block; /* 가운데 정렬 */
        animation: blink 2s infinite; /* 깜박거리는 애니메이션 효과 추가 */
        opacity: 0;
        animation: scrollFadeIn 1s ease-in-out forwards;
    }

    /* 나머지 스타일은 여기에 둡니다. */

    @media (min-width: 1024px) {
        .bottom-image {
            max-width: 100%; /* 화면 너비에 맞게 조절 */
            height: auto; /* 이미지의 높이 자동 조정 */
        }
    }
    .button img {
        max-width: 100%; /* 버튼 내 이미지 화면 너비에 맞게 조절 */
        height: auto; /* 이미지의 높이 자동 조정 */
    }

    /* 나머지 스타일은 여기에 둡니다. */

    @media (min-width: 1024px) {
        .button img {
            max-width: 100%; /* 버튼 내 이미지 화면 너비에 맞게 조절 */
            height: auto; /* 이미지의 높이 자동 조정 */
        }
    }
    </style>
</head>
<body>
    <div class="back">
        <a target="_blank" href="11index.html" style="position: relative;">
            <img class="moon scroll-animation" src="38.jpeg" alt="달덩이">
        </a>
    </div>

    <div class="text scroll-animation">
        CALLERT
    </div>
    <div class="grid-container">
        <div class="grid-item scroll-animation">
            <img src="28.jpeg" alt="이미지 1">
        </div>
        <div class="grid-item scroll-animation">
            <img src="39.jpeg" alt="이미지 2">
        </div>
        <div class="grid-item scroll-animation">
            <img src="41.jpeg" alt="이미지 3">
        </div>
        <div class="grid-item scroll-animation">
            <img src="27.png" alt="이미지 4">
        </div>
        <div class="grid-item scroll-animation">
            <img src="40.jpeg" alt="이미지 5">
        </div>
        <div class="grid-item scroll-animation">
            <img src="43.jpeg" alt="이미지 6">
        </div>
    </div>
    <div class="text scroll-animation">
        One day, precious relationships come to us.
        <div class="inner-text">Maybe it wasn't a relationship we'd already met before we met?</div>
    </div>

    <!-- 동영상 추가 및 스타일 설정 -->
    <div class="video-container scroll-animation">
        <video id="myVideo" src="9999.mp4" class="video-item" controls autoplay alt="동영상"></video>
    </div>
    <div class="text scroll-animation">
        Maybe it wasn't a relationship we'd already met before we met?
    </div>
    <!-- 밑에 이미지 추가 -->
    <img class="bottom-image scroll-animation" src="nono.png" alt="밑에 이미지">

    <!-- 버튼을 통한 페이지 이동 -->
    <div style="text-align: center;">
        <button type="button" class="button" onclick="location.href='aa2.html'">
            <h1 class="video-title">1. Camera</h1>
            <img src="pop.jpeg" width="350" height="500" alt="카메라 이미지">
            <p class="tag">온몸으로 잉크처럼 짙게 번지어, 하나의 필름에 묻어난다.</p>
        </button>
    </div>
</body>
</html>
