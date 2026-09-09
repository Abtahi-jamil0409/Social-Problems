# Social-Problems
<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>সমাজ ও রাজনীতি · বাংলা পোর্টাল</title>
    <!-- Font Awesome 6 (free) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Noto Sans Bengali', system-ui, -apple-system, sans-serif;
            background: #0b0e14;
            color: #e8edf5;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .site-container {
            display: flex;
            width: 1360px;
            max-width: 100%;
            min-height: 85vh;
            max-height: 950px;
            background: #11161f;
            border-radius: 36px;
            box-shadow: 0 20px 40px -12px rgba(0, 0, 0, 0.8), 0 8px 24px -6px rgba(0, 20, 60, 0.5);
            overflow: hidden;
            border: 1px solid #1e2a3a;
        }

        /* ---------- SIDEBAR (black & blue) ---------- */
        .sidebar {
            width: 290px;
            background: #0d121c;
            border-right: 2px solid #1a2a40;
            padding: 28px 16px 24px 20px;
            display: flex;
            flex-direction: column;
            flex-shrink: 0;
            overflow-y: auto;
        }

        .sidebar::-webkit-scrollbar {
            width: 5px;
        }
        .sidebar::-webkit-scrollbar-track {
            background: #1a2332;
            border-radius: 12px;
        }
        .sidebar::-webkit-scrollbar-thumb {
            background: #2a6bc4;
            border-radius: 12px;
        }

        .sidebar-header {
            margin-bottom: 18px;
            padding-bottom: 16px;
            border-bottom: 3px solid #1f4a8a;
        }

        .sidebar-header h2 {
            font-size: 1.7rem;
            font-weight: 600;
            color: #d6e4ff;
            display: flex;
            align-items: center;
            gap: 12px;
            letter-spacing: -0.3px;
        }

        .sidebar-header h2 i {
            color: #3b8cff;
            font-size: 1.9rem;
        }

        .sidebar-header .sub {
            font-size: 0.9rem;
            color: #7a9bd6;
            margin-top: 4px;
            padding-left: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
            font-weight: 400;
        }

        .home-btn {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 12px 18px;
            margin-bottom: 14px;
            background: #1a3a6a;
            color: #e8f0ff;
            border-radius: 40px 12px 12px 40px;
            font-weight: 600;
            font-size: 1.1rem;
            border-left: 4px solid #3b8cff;
            cursor: pointer;
            transition: all 0.15s ease;
            box-shadow: 0 4px 8px rgba(0, 20, 60, 0.4);
        }
        .home-btn i {
            color: #5a9eff;
            font-size: 1.3rem;
        }
        .home-btn:hover {
            background: #1f4a8a;
            transform: translateX(4px);
        }

        .topic-list {
            list-style: none;
            margin-top: 6px;
            flex: 1;
        }

        .topic-list li {
            padding: 11px 16px 11px 18px;
            margin-bottom: 4px;
            border-radius: 40px 12px 12px 40px;
            font-weight: 500;
            font-size: 1.02rem;
            color: #b0caf0;
            background: transparent;
            transition: all 0.15s ease;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 14px;
            border-left: 4px solid transparent;
            line-height: 1.4;
        }

        .topic-list li i {
            width: 26px;
            font-size: 1.15rem;
            color: #4a7fc9;
            transition: color 0.2s;
            text-align: center;
        }

        .topic-list li:hover {
            background: #1a2338;
            border-left-color: #3b8cff;
            color: #ffffff;
        }

        .topic-list li.active {
            background: #1a3a6a;
            color: #ffffff;
            border-left-color: #5a9eff;
            box-shadow: 0 4px 12px rgba(0, 40, 100, 0.3);
        }

        .topic-list li.active i {
            color: #7ab0ff;
        }

        .topic-list li .badge {
            background: rgba(59, 140, 255, 0.2);
            padding: 2px 10px;
            border-radius: 30px;
            font-size: 0.65rem;
            font-weight: 600;
            margin-left: auto;
            color: #8ab4ff;
            white-space: nowrap;
        }

        .sidebar-footer {
            margin-top: 18px;
            padding-top: 14px;
            border-top: 2px solid #1a2a40;
            font-size: 0.85rem;
            color: #6a8fc9;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .sidebar-footer i {
            color: #3b8cff;
        }

        /* ---------- MAIN CONTENT (পুরো এলাকা জুড়ে) ---------- */
        .content {
            flex: 1;
            background: #111822;
            padding: 36px 42px 32px 38px;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
        }

        .content::-webkit-scrollbar {
            width: 8px;
        }
        .content::-webkit-scrollbar-track {
            background: #1a2332;
            border-radius: 20px;
        }
        .content::-webkit-scrollbar-thumb {
            background: #2a6bc4;
            border-radius: 20px;
        }

        /* homepage - আমাদের কাজ ও উদ্দেশ্য সহ */
        .homepage-content {
            display: flex;
            flex-direction: column;
            justify-content: center;
            height: 100%;
            min-height: 350px;
        }
        .homepage-content h1 {
            font-size: 2.8rem;
            color: #d6e4ff;
            margin-bottom: 16px;
            display: flex;
            align-items: center;
            gap: 16px;
            flex-wrap: wrap;
        }
        .homepage-content h1 i {
            color: #3b8cff;
        }
        .homepage-content .lead {
            font-size: 1.2rem;
            color: #8aafdf;
            max-width: 700px;
            line-height: 1.8;
            margin-bottom: 28px;
        }

        /* আমাদের কাজ ও উদ্দেশ্য সেকশন */
        .mission-section {
            background: #0f1a2e;
            padding: 28px 32px;
            border-radius: 24px 8px 24px 8px;
            border-left: 6px solid #3b8cff;
            margin: 20px 0 28px 0;
        }
        .mission-section h2 {
            color: #d6e4ff;
            font-size: 1.6rem;
            margin-bottom: 16px;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        .mission-section h2 i {
            color: #3b8cff;
        }
        .mission-section p {
            color: #b8d4ff;
            line-height: 1.8;
            font-size: 1.05rem;
            margin-bottom: 10px;
        }
        .mission-section .mission-list {
            display: flex;
            flex-wrap: wrap;
            gap: 16px 30px;
            margin-top: 12px;
        }
        .mission-section .mission-list li {
            list-style: none;
            display: flex;
            align-items: center;
            gap: 10px;
            color: #c8dfff;
            font-size: 1rem;
        }
        .mission-section .mission-list li i {
            color: #3b8cff;
            width: 20px;
        }

        .homepage-content .feature-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 12px;
        }
        .homepage-content .feature-item {
            background: #1a2338;
            padding: 18px 24px;
            border-radius: 40px 12px 40px 12px;
            border-left: 6px solid #3b8cff;
            display: flex;
            align-items: center;
            gap: 14px;
            font-weight: 500;
            color: #c8dfff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }
        .homepage-content .feature-item i {
            color: #5a9eff;
            font-size: 1.5rem;
        }
        .homepage-content .blue-quote-home {
            background: #0f1a2e;
            padding: 18px 28px;
            border-radius: 24px 8px 24px 8px;
            margin: 28px 0 10px 0;
            font-style: italic;
            color: #b8d4ff;
            border-left: 8px solid #3b8cff;
        }

        /* topic view - ফুল স্ক্রিনে */
        .topic-header {
            display: flex;
            align-items: baseline;
            flex-wrap: wrap;
            gap: 12px 20px;
            border-bottom: 3px solid #1a3a6a;
            padding-bottom: 16px;
            margin-bottom: 26px;
        }
        .topic-header h1 {
            font-size: 2.4rem;
            font-weight: 600;
            color: #d6e4ff;
            letter-spacing: -0.3px;
            line-height: 1.2;
        }
        .topic-header .tag {
            background: #0f1a2e;
            padding: 4px 20px;
            border-radius: 40px;
            font-size: 0.85rem;
            font-weight: 500;
            color: #7aacf0;
            border: 1px solid #1f4a8a;
            white-space: nowrap;
        }

        .article-content {
            font-size: 1.08rem;
            line-height: 1.8;
            color: #c8dfff;
            flex: 1;
        }
        .article-content p {
            margin-bottom: 1.4rem;
            text-align: justify;
        }
        .article-content .highlight-box {
            background: #0f1a2e;
            padding: 20px 28px;
            border-radius: 24px 8px 24px 8px;
            border-left: 8px solid #3b8cff;
            margin: 24px 0;
            color: #b8d4ff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }
        .article-content .highlight-box i {
            color: #5a9eff;
            margin-right: 10px;
        }
        .article-content strong {
            color: #7ab0ff;
        }
        .article-content .video-wrapper {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            margin: 30px 0;
            border-radius: 16px;
            overflow: hidden;
            border: 2px solid #1f4a8a;
        }
        .article-content .video-wrapper iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        .article-content .video-link-box {
            background: #0f1a2e;
            padding: 20px 28px;
            border-radius: 16px;
            border: 1px solid #1f4a8a;
            margin: 24px 0;
            display: flex;
            align-items: center;
            gap: 16px;
            flex-wrap: wrap;
        }
        .article-content .video-link-box i {
            font-size: 2rem;
            color: #3b8cff;
        }
        .article-content .video-link-box a {
            color: #7ab0ff;
            text-decoration: none;
            font-weight: 500;
            word-break: break-all;
        }
        .article-content .video-link-box a:hover {
            text-decoration: underline;
            color: #aac8ff;
        }

        .content-footer {
            margin-top: 28px;
            padding-top: 16px;
            border-top: 2px solid #1a2a40;
            display: flex;
            justify-content: space-between;
            color: #6a8fc9;
            font-size: 0.95rem;
            flex-wrap: wrap;
            gap: 8px;
        }
        .content-footer i {
            color: #3b8cff;
            margin: 0 4px;
        }

        .hidden {
            display: none !important;
        }

        /* responsive */
        @media (max-width: 820px) {
            .site-container {
                flex-direction: column;
                min-height: 92vh;
                max-height: none;
                border-radius: 28px;
            }
            .sidebar {
                width: 100%;
                max-height: 220px;
                border-right: none;
                border-bottom: 2px solid #1a2a40;
                padding: 14px 12px;
                flex-shrink: 0;
                flex-direction: row;
                flex-wrap: wrap;
                align-items: center;
                gap: 6px 10px;
                overflow-y: auto;
            }
            .sidebar-header {
                border-bottom: none;
                padding-bottom: 4px;
                margin-bottom: 4px;
                width: 100%;
            }
            .sidebar-header h2 {
                font-size: 1.3rem;
            }
            .sidebar-header .sub {
                display: none;
            }
            .home-btn {
                padding: 6px 16px;
                font-size: 0.9rem;
                margin-bottom: 4px;
                border-radius: 40px;
                border-left: none;
                background: #1a3a6a;
            }
            .topic-list {
                display: flex;
                flex-wrap: wrap;
                gap: 4px 8px;
                margin-top: 2px;
                flex: 1;
                align-items: center;
            }
            .topic-list li {
                padding: 5px 14px 5px 12px;
                border-radius: 40px;
                border-left: none;
                background: #1a2338;
                font-size: 0.85rem;
                margin-bottom: 2px;
                white-space: nowrap;
                gap: 4px;
                color: #b0caf0;
            }
            .topic-list li i {
                display: none;
            }
            .topic-list li .badge {
                display: none;
            }
            .topic-list li.active {
                background: #1a3a6a;
                color: #ffffff;
            }
            .sidebar-footer {
                display: none;
            }
            .content {
                padding: 22px 18px;
            }
            .homepage-content h1 {
                font-size: 2.0rem;
            }
            .topic-header h1 {
                font-size: 1.8rem;
            }
            .mission-section {
                padding: 20px 18px;
            }
            .mission-section .mission-list {
                flex-direction: column;
                gap: 10px;
            }
        }

        @media (max-width: 480px) {
            body {
                padding: 10px;
            }
            .content {
                padding: 16px 12px;
            }
            .homepage-content h1 {
                font-size: 1.7rem;
            }
            .topic-header h1 {
                font-size: 1.5rem;
            }
            .homepage-content .feature-item {
                padding: 12px 16px;
            }
            .mission-section h2 {
                font-size: 1.3rem;
            }
        }

        .topic-list li .fa-arrow-right {
            font-size: 0.7rem;
            opacity: 0.5;
            margin-left: 2px;
        }
        .topic-list li.active .fa-arrow-right {
            opacity: 1;
            color: #7ab0ff;
        }
    </style>
</head>
<body>

    <div class="site-container">

        <!-- SIDEBAR -->
        <aside class="sidebar">
            <div class="sidebar-header">
                <h2>
                    <i class="fas fa-landmark"></i>
                    <span>বিষয়</span>
                </h2>
                <div class="sub"><i class="fas fa-arrow-right" style="color:#3b8cff;"></i> সামাজিক · রাজনৈতিক</div>
            </div>

            <div class="home-btn" id="homeBtn">
                <i class="fas fa-home"></i>
                <span>হোমপেজ</span>
                <i class="fas fa-chevron-right" style="margin-left:auto; font-size:0.8rem; opacity:0.7;"></i>
            </div>

            <ul class="topic-list" id="topicList">
                <!-- populated by JS -->
            </ul>

            <div class="sidebar-footer">
                <span><i class="fas fa-comment-dots"></i> ৬টি আলোচনা</span>
                <span><i class="fas fa-chevron-circle-right"></i></span>
            </div>
        </aside>

        <!-- MAIN CONTENT (পুরো এলাকা) -->
        <main class="content" id="contentArea">
            <!-- HOMEPAGE - আমাদের কাজ ও উদ্দেশ্য সহ -->
            <div id="homepageView">
                <div class="homepage-content">
                    <h1><i class="fas fa-bangladesh-taka"></i> সামাজিক ও রাজনৈতিক <br>বাংলা ব্লগ</h1>
                    <p class="lead">
                        <i class="fas fa-quote-left" style="color:#3b8cff; margin-right:8px;"></i>
                        বাংলাদেশের সমাজ ও রাজনীতির নানা সমস্যা নিয়ে আলোচনা। বাম পাশের সাইডবার থেকে যেকোনো টপিক নির্বাচন করুন।
                    </p>

                    <!-- আমাদের কাজ ও উদ্দেশ্য -->
                    <div class="mission-section">
                        <h2><i class="fas fa-bullseye"></i> আমাদের কাজ ও উদ্দেশ্য</h2>
                        <p>
                            এই প্ল্যাটফর্মটির মূল লক্ষ্য হলো বাংলাদেশের সমাজ ও রাজনীতির জটিল সমস্যাগুলোকে সহজ, বিশ্লেষণধর্মী ও তথ্যভিত্তিক আলোচনার মাধ্যমে তুলে ধরা। আমরা বিশ্বাস করি, সঠিক তথ্য ও যুক্তিপূর্ণ বক্তব্য সমাজকে ইতিবাচক পরিবর্তনের পথে এগিয়ে নিতে পারে।
                        </p>
                        <ul class="mission-list">
                            <li><i class="fas fa-check-circle"></i> গণতন্ত্র, ধর্মনিরপেক্ষতা, নারীবাদ, শিক্ষাব্যবস্থা, পুঁজিবাদ ও সমাজতন্ত্র—এই ছয়টি মূল বিষয়ের ওপর গভীর বিশ্লেষণ</li>
                            <li><i class="fas fa-check-circle"></i> ঐতিহাসিক, তাত্ত্বিক ও বাস্তবমুখী দৃষ্টিভঙ্গি থেকে সমস্যাগুলোর ব্যবচ্ছেদ</li>
                            <li><i class="fas fa-check-circle"></i> প্রামাণ্য ভিডিও, বই ও গবেষণার আলোকে তথ্য উপস্থাপন</li>
                            <li><i class="fas fa-check-circle"></i> পাঠকদের চিন্তার স্বাধীনতা ও সমালোচনামূলক দৃষ্টিভঙ্গি গঠনে সহায়তা</li>
                        </ul>
                    </div>

                    <div class="feature-grid">
                        <div class="feature-item"><i class="fas fa-landmark"></i> গণতন্ত্র</div>
                        <div class="feature-item"><i class="fas fa-people-arrows"></i> ধর্মনিরপেক্ষতা</div>
                        <div class="feature-item"><i class="fas fa-venus"></i> নারীবাদ</div>
                        <div class="feature-item"><i class="fas fa-chalkboard-teacher"></i> শিক্ষাব্যবস্থা</div>
                        <div class="feature-item"><i class="fas fa-chart-line"></i> পুঁজিবাদ</div>
                        <div class="feature-item"><i class="fas fa-handshake"></i> সমাজতন্ত্র</div>
                    </div>
                    <div class="blue-quote-home">
                        <i class="fas fa-quote-left"></i> “সমাজের প্রতিটি সমস্যা আমাদের অংশগ্রহণে সমাধান লাভ করে।”
                    </div>
                    <p style="margin-top:8px; color:#6a8fc9; font-weight:400;">
                        <i class="fas fa-arrow-right"></i> সাইডবার থেকে যেকোনো টপিকে ক্লিক করুন।
                    </p>
                </div>
            </div>

            <!-- TOPIC VIEW (ফুল স্ক্রিন) -->
            <div id="topicView" class="hidden">
                <div class="topic-header">
                    <h1 id="topicTitle">শিরোনাম</h1>
                    <span class="tag" id="topicTag">ট্যাগ</span>
                </div>
                <div class="article-content" id="articleContent"></div>
                <div class="content-footer">
                    <span><i class="fas fa-pen-fancy"></i> বাংলা · সমস্যা ও বিশ্লেষণ</span>
                    <span id="pageIndicator"><i class="fas fa-arrow-right"></i> ১/৬</span>
                </div>
            </div>
        </main>
    </div>

    <script>
        (function() {
            // ----- TOPICS (গণতন্ত্র, ধর্মনিরপেক্ষতা, নারীবাদ, শিক্ষাব্যবস্থা, পুঁজিবাদ, সমাজতন্ত্র) -----
            const topics = [{
                title: "গণতন্ত্রের সমস্যা",
                tag: "রাজনীতি",
                content: `
                        <p><i class="fas fa-landmark" style="color:#3b8cff;"></i> গণতন্ত্রের মূল সমস্যা হলো জনগণের অংশগ্রহণের অভাব, দুর্নীতি, ও দলীয় স্বার্থে জাতীয় স্বার্থকে ত্যাগ করা। নিচের ভিডিওগুলোতে গণতন্ত্রের বাস্তবতা ও দুর্বলতা সম্পর্কে বিস্তারিত আলোচনা করা হয়েছে।</p>

                        <div class="video-wrapper">
                            <iframe src="https://www.youtube.com/embed/-rWztVkSpsE" allowfullscreen></iframe>
                        </div>

                        <div class="highlight-box">
                            <i class="fas fa-video"></i> <strong>ভিডিওর মূল বক্তব্য (Democracy for Realists):</strong><br>
                            <ul style="list-style: none; padding-left: 10px; margin-top: 8px;">
                                <li>• <strong>গণতন্ত্রের লোকগাথা (Folk Theory):</strong> নাগরিকরা সচেতনভাবে নেতা বাছাই করেন এবং নির্বাচিত নেতারা জনগণের ইচ্ছামতো দেশ চালান—এই ধারণা রূপকথার মতো।</li>
                                <li>• <strong>পশ্চাৎমুখী ভোট (Retrospective Voting):</strong> ভোটাররা নীতির বিস্তারিত না জেনে শুধু বর্তমান সরকারের অবস্থা দেখে ভোট দেয়।</li>
                                <li>• <strong>অন্ধ পশ্চাদদৃষ্টি (Blind Retrospection):</strong> ১৯১৬ সালের হাঙর আক্রমণের মতো সম্পূর্ণ সম্পর্কহীন ঘটনাও ভোটের ফলকে প্রভাবিত করতে পারে।</li>
                                <li>• <strong>অর্থনৈতিক ভোট (Economic Voting):</strong> মহামন্দার মতো পরিস্থিতিতে জনগণ আদর্শগত বিচারের বদলে অর্থনৈতিক অনুভূতির ভিত্তিতে ভোট দেয়।</li>
                                <li>• <strong>সামাজিক পরিচয় (Social Identity):</strong> মানুষ মূলত নীতি বুঝে নয়, বরং ধর্ম, জাতিসত্তা, এবং দলীয় পরিচয়ের ভিত্তিতে ভোট দেয়।</li>
                            </ul>
                        </div>

                        <div class="video-link-box">
                            <i class="fab fa-facebook"></i>
                            <span><strong>Puron's Bookshelf</strong> - কেন প্লেটো গণতন্ত্রকে ঘৃণা করতেন? (Why Plato hate democracy?)</span>
                            <a href="https://www.facebook.com/reel/1306981144672542" target="_blank">ভিডিওটি দেখতে এখানে ক্লিক করুন</a>
                        </div>

                        <div class="highlight-box">
                            <i class="fas fa-quote-left"></i> <strong>প্লেটোর গণতন্ত্র-বিরোধী মতবাদ:</strong> প্লেটো তাঁর 'দ্য রিপাবলিক' গ্রন্থে গণতন্ত্রকে 'ভীড়ের শাসন' হিসেবে আখ্যায়িত করেছেন। তার মতে, অযোগ্য ও অশিক্ষিত জনগণ আবেগের বশবর্তী হয়ে চাটুকার নেতাদের নির্বাচিত করে, যা সমাজের জন্য ধ্বংস ডেকে আনে। তিনি বিশ্বাস করতেন, রাষ্ট্র পরিচালনার জন্য দার্শনিক রাজার (Philosopher King) প্রয়োজন, যিনি জ্ঞান ও প্রজ্ঞার দ্বারা শাসন করবেন।
                        </div>

                        <p><strong>গণতন্ত্রের অন্ধগলি: একটি শাসনব্যবস্থার তাত্ত্বিক, ঐতিহাসিক ও বাস্তবমুখী ব্যবচ্ছেদ</strong></p>

                        <p><strong>ভূমিকা ও ঐতিহাসিক পটভূমি:</strong> রাজনৈতিক চিন্তার ইতিহাসে ‘গণতন্ত্র’ শব্দটি যতটা আকর্ষণীয়, বাস্তবে এর প্রয়োগ ততটাই জটিল ও কণ্টকাকীর্ণ। সাধারণত গণতন্ত্র বলতে জনগণের দ্বারা, জনগণের জন্য এবং জনগণের শাসনব্যবস্থাকে বোঝানো হলেও, মানব ইতিহাসের গোড়াপত্তন থেকেই সেরা চিন্তাবিদ ও দার্শনিকরা এই ব্যবস্থার অন্তর্নিহিত দুর্বলতা সম্পর্কে প্রতিনিয়ত সতর্ক করে এসেছেন। প্রাচীন গ্রিসের অ্যাথেন্সে যে প্রত্যক্ষ গণতন্ত্রের সূচনা হয়েছিল, তা অল্প সময়ের মধ্যেই রাজনৈতিক বিশৃঙ্খলা, অবিবেচক সিদ্ধান্ত এবং সক্রেটিসের মতো মহান দার্শনিককে মৃত্যুদণ্ড দেওয়ার মতো চরম মূর্খতার জন্ম দিয়েছিল। প্রাচীন রাজনৈতিক চিন্তাবিদদের মধ্যে প্লেটো, অ্যারিস্টটল এবং পরবর্তীতে আধুনিক যুগের নোয়াম চমস্কি বা এরিক হবসবমের মতো চিন্তাবিদরা গণতন্ত্রকে একটি আদর্শিক ব্যবস্থার চেয়ে বরং একটি অত্যন্ত ঝুঁকিপূর্ণ ও অপব্যবহারযোগ্য সামাজিক চুক্তি হিসেবেই প্রত্যক্ষ করেছেন।</p>

                        <p>গণতন্ত্র কেবল একটি শাসনপদ্ধতি নয়; এটি এমন একটি গাণিতিক প্রক্রিয়া যা রাষ্ট্রের সিদ্ধান্ত গ্রহণের ক্ষমতা তুলে দেয় কেবল সংখ্যার সমীকরণের ওপর। যখনই কোনো সমাজে নীতি, আদর্শ, নৈতিকতা ও প্রজ্ঞার চেয়ে কেবল মানুষের মাথাপিছু গণনা বা গাণিতিক যোগফল মুখ্য হয়ে ওঠে, তখনই সেই সমাজ ধাপে ধাপে একটি প্রাতিষ্ঠানিক সংকটের দিকে ধাবিত হয়। আধুনিক বিশ্বে বিশ্বায়ন, পুঁজিবাদ এবং প্রযুক্তির তীব্র প্রসারের ফলে গণতন্ত্রের যে নতুন নতুন রূপ আমরা দেখতে পাচ্ছি, তা এই শাসনব্যবস্থার ভেতরে লুকিয়ে থাকা পুরোনো ক্ষতগুলোকে আরও বেশি উন্মোচিত ও বিষাক্ত করে তুলেছে।</p>

                        <p><strong>১. গাণিতিক গণনার ভুল এবং মেধা ও প্রজ্ঞার অবমূল্যায়ন:</strong> গণতন্ত্রের সবচেয়ে বড় মৌলিক ও তাত্ত্বিক সমস্যা হলো এটি সকল মানুষের সিদ্ধান্ত নেওয়ার ক্ষমতাকে সমান বলে ধরে নেয়, যা বাস্তবে একটি চরম বৈজ্ঞানিক ও সামাজিক অসত্য। রাষ্ট্র পরিচালন একটি অত্যন্ত জটিল ও মনস্তাত্ত্বিক বিষয়, যার জন্য প্রয়োজন গভীর জ্ঞান, সামাজিক মনস্তত্ত্বের অনুধাবন, অর্থনৈতিক বোঝাপড়া এবং নীতিগত দূরদর্শিতা। কিন্তু গণতান্ত্রিক প্রক্রিয়ায় একজন বিশ্ববিখ্যাত অর্থনীতিবিদ, বিজ্ঞানী বা বিচারকের একটি ভোটের রাজনৈতিক মূল্য এবং একজন রাজনৈতিকভাবে অসচেতন, লোভী বা অশিক্ষিত ব্যক্তির একটি ভোটের মূল্য হুবহু সমান।</p>

                        <p>অ্যারিস্টটল তাঁর রাজনৈতিক বিশ্লেষণে উল্লেখ করেছিলেন যে, সমতার নামে অসম সক্ষমতার মানুষকে সমান মর্যাদা দেওয়া এক ধরনের চরম বৈষম্য। যখন রাষ্ট্রের ভাগ্য নির্ধারণের দায়িত্ব এমন সাধারণ জনগোষ্ঠীর হাতে তুলে দেওয়া হয়, যারা অর্থনীতির জটিল সমীকরণ বা আন্তর্জাতিক কূটনীতির প্যাঁচ বোঝেন না, তখন তারা খুব সহজেই চাটুকার নেতাদের দ্বারা প্রভাবিত হন। রাজনীতিকরা জনসমক্ষে এমন সব প্রতিশ্রুতির ফুলঝুরি ফোটান, যা রাষ্ট্রের অর্থনীতির জন্য ক্ষতিকর হলেও সাধারণ মানুষের কানে শুনতে ভালো লাগে। এর ফলে রাষ্ট্রীয় নীতি নির্ধারিত হয় যুক্তিবোধ ও বিজ্ঞতার ভিত্তিতে নয়, বরং আমজনতার তাৎক্ষণিক আবেগ ও অজ্ঞতার ওপর নির্ভর করে।</p>

                        <p><strong>২. সংখ্যাগরিষ্ঠের স্বৈরাচার (Tyranny of the Majority):</strong> গণতন্ত্রের অন্যতম প্রধান স্তম্ভ হলো ‘সংখ্যাগরিষ্ঠের মত’। কিন্তু রাষ্ট্রবিজ্ঞানের দৃষ্টিভঙ্গিতে এই গাণিতিক নীতিটি অনেক সময় অত্যন্ত নির্মম ও নিষ্ঠুর স্বৈরাচারে রূপ নেয়। ৫০ শতাংশের সাথে আরও ১ শতাংশ ভোট যুক্ত হলেই একটি দল বা গোষ্ঠী পুরো ১০০ শতাংশ মানুষের ভাগ্য নিয়ন্ত্রণ করার আইনি বৈধতা পেয়ে যায়। এই ব্যবস্থার সবচেয়ে বড় ভুক্তভোগী হয় সমাজে অবস্থানরত নানা ধরনের সংখ্যালঘু গোষ্ঠী—তা ধর্মীয়, জাতিগত, ভাষাগত কিংবা চিন্তাগত যে রূপেরই হোক না কেন।</p>

                        <p>গণতান্ত্রিক প্রক্রিয়ায় বিজয়ী সংখ্যাগরিষ্ঠ গোষ্ঠী যদি অমানবিক বা বৈষম্যমূলক আইনও পাস করে, তবে গণতান্ত্রিক কাঠামোর দোহাই দিয়ে সেটিকে ‘জনগণের রায়’ বলে চালিয়ে দেওয়া হয়। ইতিহাস সাক্ষী, অ্যাডলফ হিটলার বা বেনিতো মুসোলিনির মতো একনায়করা রাতারাতি আকাশ থেকে পড়েননি; তারা গণতান্ত্রিক নির্বাচনের মাধ্যমে জনগণের উল্লেখযোগ্য সমর্থন নিয়েই ক্ষমতার মসনদে বসেছিলেন এবং পরবর্তীতে গণতান্ত্রিক আইনি পন্থাবলি ব্যবহার করেই ফ্যাসিবাদের জন্ম দিয়েছিলেন। ফলে গণতন্ত্র ক্ষেত্রবিশেষে নিরঙ্কুশ ও সুসংগঠিত স্বৈরাচার তৈরির সবচেয়ে সুবিধাজনক মোড়ক হিসেবে ব্যবহৃত হয়।</p>

                        <p><strong>৩. জনমোহিনী রাজনীতি (Populism) ও আবেগের ম্যানিপুলেশন:</strong> আধুনিক গণতান্ত্রিক ব্যবস্থার সবচেয়ে বড় ব্যাধি হলো জনমোহিনী বা পপুলিস্ট রাজনীতি। পপুলিজম হলো এমন একটি রাজনৈতিক কৌশল যেখানে জটিল সমস্যার অতি-সরলীকৃত সমাধান হাজির করা হয় এবং জনগণের ভয়, ঘৃণা ও আবেগকে চরমভাবে উসকে দেওয়া হয়। একজন চতুর রাজনীতিবিদ খুব সহজেই জানেন যে, দেশের মৌলিক কাঠামোগত সমস্যা সমাধান করার চেয়ে জনগণের অবচেতন মনে জমে থাকা ভয় ও ক্ষোভকে কাজে লাগানো অনেক বেশি সহজ ও কার্যকরী।</p>

                        <p>আজকের গণতান্ত্রিক নির্বাচনে প্রার্থীরা যুক্তি বা তথ্যের ভিত্তিতে বিতর্ক করেন না; বরং তারা প্রতিপক্ষের বিরুদ্ধে ঘৃণা ছড়ানো, কাল্পনিক শত্রু দাঁড় করানো এবং অবাস্তব স্বপ্ন বিক্রির খেলায় মেতে ওঠেন। যে নেতা যত বেশি উত্তেজনা ছড়াতে পারেন, ট্রল ও স্লোগান তৈরি করতে পারেন এবং সাধারণ মানুষের নিম্নগামী মনস্তত্ত্বকে স্পর্শ করতে পারেন, ভোটে তার জয়ের সম্ভাবনা তত বেড়ে যায়। এর ফলে সুস্থ রাজনৈতিক চর্চা বিলুপ্ত হয় এবং পুরো রাষ্ট্রটি এক ধরণের উন্মাদনা ও সস্তা বিনোদনের মঞ্চে পরিণত হয়।</p>

                        <p><strong>৪. পুঁজিবাদ, কর্পোরেট অর্থায়ন ও ধনিকতন্ত্রের (Oligarchy) বিস্তার:</strong> বর্তমান যুগে গণতন্ত্র ও পুঁজিপতিদের মধ্যকার সম্পর্ক অত্যন্ত মাফিয়া সুলভ রূপ ধারণ করেছে। আধুনিক নির্বাচনে জয়ী হতে হলে যে বিশাল পরিমাণ অর্থ, প্রচার-প্রচারণা, বিজ্ঞাপনী সংস্থা এবং মিডিয়া ম্যানেজমেন্টের প্রয়োজন হয়, তা কোনো সাধারণ মানুষের সাধ্যের মধ্যে থাকে না। নির্বাচনে প্রার্থী হওয়া এবং টিকে থাকার পূর্বশর্তই হলো শত শত কোটি টাকার মালিক হওয়া বা কোনো বড় কর্পোরেট গোষ্ঠীর সমর্থন লাভ করা।</p>

                        <p>রাজনৈতিক দলগুলো তাদের নির্বাচনী তহবিল জোগাড় করার জন্য বড় বড় শিল্পপতি, ব্যাংক মালিক ও ব্যবসায়ী গোষ্ঠীর কাছে নিজেদের বিকিয়ে দেয়। নির্বাচন শেষ হলে এবং দল ক্ষমতায় এলে, সেই বিনিয়োগ করা অর্থের মুনাফা তুলে দেওয়ার কাজ শুরু হয়। সংসদ বা আইনসভায় এমন সব আইন তৈরি করা হয় যা সাধারণ জনগণের পকেট কেটে ওই পুঁজিপতিদের পকেট ভারী করে। পরিবেশ সুরক্ষা আইন শিথিল করা, কর ছাড় দেওয়া, ব্যাংকের ঋণ মওকুফ করা কিংবা রাষ্ট্রীয় মেগা প্রজেক্টের কাজ স্বজনদের হাতে তুলে দেওয়ার মাধ্যমে গণতন্ত্রকে আড়ালে রেখে মূলত একটি চরম ‘ধনিকতন্ত্র’ বা ওলিগার্কি পরিচালনা করা হয়। সাধারণ মানুষ ভাবে তারা প্রতিনিধি নির্বাচন করছে, কিন্তু বাস্তবে তারা ধনকুবেরদের তৈরি করা পুতুলপ্রার্থীদের মধ্য থেকেই কাউকে না কাউকে বেছে নিতে বাধ্য হয়।</p>

                        <p><strong>৫. রাজনৈতিক স্বল্পমেয়াদিতা (Short-termism) ও দীর্ঘমেয়াদী ধ্বংস:</strong> গণতান্ত্রিক সরকারের একটি নির্দিষ্ট মেয়াদ থাকে—সাধারণত চার বা পাঁচ বছর। আপাতদৃষ্টিতে এটি ক্ষমতার অপব্যবহার রোধের উপায় মনে হলেও, রাষ্ট্রীয় নীতি নির্ধারণের ক্ষেত্রে এর পরিণতি অত্যন্ত মারাত্মক। একটি নির্বাচিত সরকার সর্বদা পরবর্তী নির্বাচনকে মাথায় রেখে কাজ করে। তাদের প্রধান লক্ষ্য থাকে এমন সব প্রকল্প গ্রহণ করা যা আগামী ৪ বছরের মধ্যে শেষ হবে এবং যার দৃশ্যমান প্রচার চালিয়ে পরের নির্বাচনে ভোট পাওয়া যাবে।</p>

                        <p>রাষ্ট্রের জন্য অত্যন্ত জরুরি কিন্তু দীর্ঘমেয়াদী যেসব খাত রয়েছে—যেমন মৌলিক শিক্ষা ব্যবস্থার সংস্কার, বৈজ্ঞানিক গবেষণা, জলবায়ু পরিবর্তনের প্রভাব মোকাবিলা বা নতুন প্রজন্মকে দক্ষ মানবসম্পদে রূপান্তর—এসব খাতের সুফল আসতে অন্তত ২০ থেকে ৩০ বছর সময় লাগে। যেহেতু এই দীর্ঘমেয়াদী প্রজেক্টগুলোর রাজনৈতিক সুবিধা তাৎক্ষণিকভাবে পাওয়া যায় না, তাই কোনো গণতান্ত্রিক সরকারই এসব মৌলিক খাতে দীর্ঘমেয়াদী বিনিয়োগ করতে চায় না। ফলে রাষ্ট্র কেবল সাময়িক মলম লাগানোর নীতিতে চলে এবং দূরদর্শী কোনো টেকসই পরিবর্তন অর্জনে ব্যর্থ হয়।</p>

                        <p><strong>৬. সামাজিক মেরুকরণ ও জাতীয় ঐক্যের বিনাশ:</strong> নির্বাচনে বিজয়ী হওয়া যেহেতু গণতান্ত্রিক রাজনীতির মূল লক্ষ্য, তাই রাজনৈতিক দলগুলো সমাজকে একতাবদ্ধ রাখার চেয়ে বিভক্ত করাকেই বেশি লাভজনক মনে করে। একটি ঐক্যবদ্ধ সমাজকে শাসন করা কঠিন, কিন্তু একটি বিভাজিত সমাজকে আবেগে ভাসিয়ে ভোটব্যাংকে রূপান্তর করা অত্যন্ত সহজ।</p>

                        <p>ভোটের রাজনীতির স্বার্থে ধর্ম, জাতি, বর্ণ, অঞ্চল এবং সামাজিক শ্রেণীর ওপর ভিত্তি করে কৃত্রিম বিভাজন তৈরি করা হয়। সাধারণ নাগরিকদের শেখানো হয় যে প্রতিপক্ষ দলের সমর্থকরা কেবল রাজনৈতিক প্রতিদ্বন্দ্বী নয়, বরং তারা দেশের শত্রু বা জাতির জন্য হুমকি। এই অশুভ চর্চার ফলে পরিবার, সমাজ ও রাষ্ট্রের প্রাতিষ্ঠানিক কাঠামোর ভেতরে এক ধরনের মানসিক গৃহযুদ্ধ বা তীব্র মেরুকরণ তৈরি হয়। মানুষ সত্য বা মিথ্যার বিচার ভুলে যায় এবং কেবল নিজেদের রাজনৈতিক গোত্রের অন্ধ সমর্থক হয়ে ওঠে, যা একটি সুস্থ ও সভ্য সামাজিক জীবনকে বিষাক্ত করে তোলে।</p>

                        <p><strong>৭. তথ্যের ম্যানিপুলেশন, অ্যালগরিদম ও জনমতের ভুয়া নির্মাণ:</strong> একবিংশ শতাব্দীতে গণতন্ত্রের ওপর সবচেয়ে বড় আঘাতটি এসেছে তথ্যপ্রযুক্তি ও ডিজিটাল প্ল্যাটফর্মগুলোর কাছ থেকে। অতীতে জনমত গঠিত হতো সরাসরি আলোচনা বা পত্রিকার তথ্যের ওপর ভিত্তি করে, কিন্তু বর্তমানে সোশ্যাল মিডিয়ার অ্যালগরিদম মানুষের চিন্তা ও রাজনৈতিক পছন্দকে নিখুঁতভাবে নিয়ন্ত্রণ করছে। ক্যামব্রিজ অ্যানালিটিকার মতো ঘটনার মধ্য দিয়ে বিশ্ববাসী দেখেছে কীভাবে কোটি কোটি মানুষের ব্যক্তিগত ডাটা চুরি করে, তাদের মনস্তাত্ত্বিক দুর্বলতা বিশ্লেষণ করে নির্দিষ্ট প্রার্থীর পক্ষে ভোট দোলানো সম্ভব।</p>

                        <p>ভুয়া খবর (Fake News), ডিপফেক প্রযুক্তি, পেড ট্রল বাহিনী এবং প্রোপাগান্ডা ব্যবহার করে ভোটারদের মস্তিষ্ক ধোলাই (Brainwash) করা এখন অত্যন্ত সহজ ও সস্তা একটি প্রক্রিয়ায় পরিণত হয়েছে। সাধারণ মানুষ যা দেখছে বা শুনছে, তারা মনে করছে তা তাদের নিজস্ব চিন্তার ফসল, অথচ বাস্তবে তারা কিছু পরাক্রমশালী মিডিয়া ফার্ম ও রাজনৈতিক এজেন্সির দ্বারা চালিত পুতুল মাত্র। যখন তথ্যের সত্যতা এবং বস্তুনিষ্ঠতাই হারিয়ে যায়, তখন সেই তথ্যের ওপর ভিত্তি করে দেওয়া কোনো ভোটাধিকার কখনোই প্রকৃত জনমতের প্রতিফলন হতে পারে না।</p>

                        <p><strong>৮. প্রশাসনিক দীর্ঘসূত্রতা ও জরুরি সংকট মোকাবিলায় অদক্ষতা:</strong> গণতান্ত্রিক শাসনকাঠামোতে প্রতিটি সিদ্ধান্তের জন্য আইনসভার বিতর্ক, সংসদীয় কমিটির পর্যালোচনা, আমলাতান্ত্রিক ছাড়পত্র এবং নানামুখী আইনি যাচাই-বাছাইয়ের প্রয়োজন পড়ে। সাধারণ স্বাভাবিক অবস্থায় এটি ক্ষমতার ভারসাম্য বজায় রাখার উপায় হলেও, জাতীয় জরুরি পরিস্থিতি বা চরম সংকটের সময় এটি রাষ্ট্রের জন্য আত্মঘাতী প্রমাণিত হয়।</p>

                        <p>যুদ্ধ, বিশ্বব্যাপী অর্থনৈতিক ধস, মহামারী কিংবা মারাত্মক প্রাকৃতিক দুর্যোগের সময় রাষ্ট্রকে দ্রুত, নিখুঁত এবং কঠোর সিদ্ধান্ত নিতে হয়। গণতান্ত্রিক প্রক্রিয়ার অহেতুক তর্ক-বিতর্ক এবং রাজনৈতিক বিরোধিতার কারণে অনেক সময় সঠিক সময়ে সঠিক সিদ্ধান্তটি নেওয়া সম্ভব হয় না। বিভিন্ন রাজনৈতিক দলের পারস্পরিক কাদা ছোড়াছুড়ি এবং স্বার্থের দ্বন্দ্বে রাষ্ট্রের কোটি কোটি টাকার ক্ষতি হয় এবং সাধারণ মানুষের জীবন বিপন্ন হয়ে পড়ে। ইতিহাসে দেখা গেছে, দ্রুত সিদ্ধান্ত গ্রহণের ক্ষেত্রে গণতান্ত্রিক কাঠামোর চেয়ে কেন্দ্রিক বা একক কর্তৃত্ববাদী প্রশাসনিক কাঠামো অনেক বেশি কার্যকারিতা দেখিয়েছে।</p>

                        <p><strong>৯. প্রাতিষ্ঠানিক দুর্নীতি ও নৈতিক ধস:</strong> ক্ষমতায় যাওয়া এবং ক্ষমতা ধরে রাখার এই নিরন্তর দৌড় রাজনীতির ভেতরকার সর্বনিম্ন নৈতিকতাটুকুও ধ্বংস করে দেয়। রাজনীতি যেখানে জনসেবার মাধ্যম হওয়ার কথা ছিল, গণতন্ত্রের ছোঁয়ায় তা আজ লাভজনক ব্যবসায় পরিণত হয়েছে। নির্বাচনে যে পরিমাণ অর্থ বিনিয়োগ করা হয়, ক্ষমতায় এসে তার দ্বিগুণ বা তিনগুণ অর্থ দুর্নীতি ও ঘুষের মাধ্যমে তুলে নেওয়াকে রাজনীতিবিদরা তাদের আইনি অধিকার মনে করেন।</p>

                        <p>রাষ্ট্রীয় প্রতিষ্ঠানগুলো—যেমন বিচার বিভাগ, পুলিশ প্রশাসন, নির্বাচন কমিশন এবং দুর্নীতি দমন কমিশন—যেগুলোকে নিরপেক্ষ থাকার কথা ছিল, রাজনৈতিক দলগুলো ক্ষমতায় এসে সেগুলোকে নিজেদের স্বার্থে ব্যবহার করতে শুরু করে। বিচারক নিয়োগে দলীয় আনুগত্য দেখা হয়, প্রশাসনিক কর্মকর্তাদের দলীয় ক্যাডারে রূপান্তর করা হয় এবং আইন প্রয়োগকারী সংস্থাকে ব্যবহার করা হয় বিরোধী মতকে দমন করার জন্য। এর ফলে রাষ্ট্রের সকল নিরপেক্ষ স্তম্ভ ভেঙে পড়ে এবং পুরো প্রশাসনিক ব্যবস্থাটি ভেতর থেকে পচে নষ্ট হয়ে যায়।</p>

                        <p><strong>১০. রাজনৈতিক হতাশা ও সাধারণ মানুষের অনীহা (Political Apathy):</strong> বছরের পর বছর ধরে গণতান্ত্রিক ব্যবস্থার এই ভণ্ডামি, প্রতিশ্রুতি ভঙ্গ এবং দুর্নীতির মহোৎসব দেখতে দেখতে সাধারণ মানুষের মনে রাজনীতি সম্পর্কে চরম অনীহা ও ঘৃণার জন্ম হয়। মানুষ বুঝতে পারে যে, তারা যে দলকেই ভোট দিক না কেন, তাদের মূল ভাগ্য, দ্রব্যমূল্য, কর্মসংস্থান বা জীবনযাত্রার মানের কোনো বাস্তব পরিবর্তন ঘটে না। কেবল মুখের ভাষা ও চেহারার পরিবর্তন হয়, কিন্তু শোষণের কাঠামো একই থেকে যায়।</p>

                        <p>এই গভীর হতাশা থেকে সাধারণ নাগরিকরা গণতান্ত্রিক প্রক্রিয়া থেকে মুখ ফিরিয়ে নেয়। নির্বাচনে ভোটারের উপস্থিতি আশঙ্কাজনকভাবে কমতে থাকে। একটি দেশে যখন অর্ধেকেরও কম মানুষ ভোট দিতে যায় এবং সেখান থেকে সামান্য ব্যবধানে কেউ জয়ী হয়, তখন সেই বিজয়ী প্রতিনিধি প্রকৃতপক্ষে মোট জনসংখ্যার খুবই ক্ষুদ্র একটি অংশের প্রতিনিধিত্ব করে। এর ফলে শাসনব্যবস্থার নৈতিক গ্রহণযোগ্যতাই নষ্ট হয়ে যায় এবং গণতন্ত্র একটি অর্থহীন আনুষ্ঠানিকতায় পর্যবসিত হয়।</p>

                        <p><strong>উপসংহার:</strong> গণতন্ত্রের এই দীর্ঘ ও গভীর ব্যবচ্ছেদ প্রমাণ করে যে, একে একটি স্বয়ংসম্পূর্ণ, ত্রুটিহীন বা পরম শাসনব্যবস্থা হিসেবে বিবেচনা করার কোনো সুযোগ নেই। এটি মূলত মানুষের তৈরি এমন একটি ভঙ্গুর সামাজিক কাঠামো, যার ভেতরে রয়েছে ক্ষমতার লোভ, গাণিতিক বোকামি, সামাজিক বিভাজন এবং ধনকুবেরদের স্বার্থসিদ্ধির অগণিত সুযোগ।</p>

                        <p>যদি কোনো সমাজে উচ্চমানের শিক্ষার বিস্তার, প্রাতিষ্ঠানিক স্বচ্ছতা, শক্তিশালী বিচার ব্যবস্থা, সচেতন নাগরিক সমাজ এবং অর্থবিত্তের প্রভাবমুক্ত রাজনৈতিক সংস্কৃতির অভাব থাকে, তবে সেখানে গণতন্ত্র কখনোই জনগণের মুক্তি এনে দিতে পারে না। বরং তা ছদ্মবেশে সংখ্যাগরিষ্ঠের স্বৈরাচার, চরম দুর্নীতি এবং সামাজিক নৈরাজ্যেরই রূপ নেয়। তাই গণতন্ত্রকে অন্ধভাবে পূজা না করে এর অন্তর্নিহিত দুর্বলতাগুলোকে সঠিকভাবে অনুধাবন করা এবং এর বিকল্প বা পরিমার্জিত নীতি নিয়ে চিন্তা করাই আধুনিক রাষ্ট্রবিজ্ঞানের সবচেয়ে বড় চ্যালেঞ্জ।</p>
                    `
            }, {
                title: "ধর্মনিরপেক্ষতার সংকট",
                tag: "সমাজ",
                content: `
                        <p><i class="fas fa-people-arrows" style="color:#3b8cff;"></i> ধর্মনিরপেক্ষতা বাংলাদেশের সংবিধানের মূল স্তম্ভ, কিন্তু বাস্তবে এটি বারবার চ্যালেঞ্জের মুখে পড়ে। সাম্প্রদায়িক সহিংসতা, ধর্মীয় সংখ্যালঘুদের ওপর আক্রমণ, ও রাজনৈতিক দলগুলোর ধর্মীয় আবেদন ধর্মনিরপেক্ষতাকে দুর্বল করে।</p>
                        <p>শিক্ষা ব্যবস্থায় ধর্মীয় শিক্ষার প্রসার, গণমাধ্যমে সাম্প্রদায়িক বক্তব্য, ও আইন প্রয়োগের বৈষম্য—এই তিনটি বিষয় ধর্মনিরপেক্ষতার জন্য হুমকি।</p>
                        <div class="highlight-box"><i class="fas fa-lightbulb"></i> “ধর্মনিরপেক্ষতা মানে ধর্মকে অস্বীকার করা নয়, বরং সব ধর্মের প্রতি সমান সম্মান ও রাষ্ট্রের নিরপেক্ষতা নিশ্চিত করা।”</div>
                        <p><strong>সমাধান:</strong> সাম্প্রদায়িক বক্তব্য নিয়ন্ত্রণ, সংখ্যালঘুদের নিরাপত্তা নিশ্চিত করা, ও শিক্ষায় মানবতাবাদী মূল্যবোধ প্রসারিত করা জরুরি।</p>
                    `
            }, {
                title: "নারীবাদ ও নারীর অধিকার",
                tag: "সামাজিক",
                content: `
                        <p><i class="fas fa-venus" style="color:#3b8cff;"></i> নারীবাদ শুধু নারীর অধিকার নয়, বরং সমাজের সকল স্তরে লৈঙ্গিক বৈষম্য দূরীকরণ। বাংলাদেশে নারী নির্যাতন, যৌন হয়রানি, ও কর্মক্ষেত্রে বৈষম্য এখনও প্রকট। আইনি সুরক্ষা থাকলেও বাস্তবে তার প্রয়োগ নেই।</p>
                        <p>পারিবারিক সহিংসতা, বাল্যবিবাহ, ও নারীর অর্থনৈতিক অংশগ্রহণের সীমাবদ্ধতা—এই সমস্যাগুলো নারীবাদী আন্দোলনের মূল লক্ষ্য।</p>
                        <div class="highlight-box"><i class="fas fa-fist-raised"></i> “নারীর অধিকার মানবাধিকার — এটি উপলব্ধি করতে হবে। নারীবাদ পুরুষের বিরুদ্ধে নয়, বরং পুরুষতান্ত্রিক কাঠামোর বিরুদ্ধে।”</div>
                        <p><strong>সমাধান:</strong> আইনের কঠোর প্রয়োগ, শিক্ষায় লৈঙ্গিক সচেতনতা, ও নারীর অর্থনৈতিক ক্ষমতায়ন নারীবাদকে বাস্তবায়িত করতে পারে।</p>
                    `
            }, {
                title: "শিক্ষাব্যবস্থার ভঙ্গুরতা",
                tag: "শিক্ষা",
                content: `
                        <p><i class="fas fa-chalkboard-teacher" style="color:#3b8cff;"></i> বাংলাদেশের শিক্ষাব্যবস্থা গুণগত মান, সুযোগের বৈষম্য, ও পাঠ্যক্রমের অপ্রাসঙ্গিকতায় ভুগছে। গ্রাম-শহর ব্যবধান, শিক্ষকের যোগ্যতার অভাব, ও কারিগরি শিক্ষার প্রতি অনীহা শিক্ষাব্যবস্থার প্রধান সমস্যা।</p>
                        <p>উচ্চশিক্ষায় গবেষণার অভাব, বিজ্ঞান-প্রযুক্তি শিক্ষার দুর্বলতা, ও শিক্ষার বাণিজ্যিকীকরণও গুরুত্বপূর্ণ সংকট।</p>
                        <div class="highlight-box"><i class="fas fa-quote-left"></i> “শিক্ষা মানে শুধু পাস করা নয়, বরং চিন্তার স্বাধীনতা ও সমালোচনামূলক দৃষ্টিভঙ্গি তৈরি করা।”</div>
                        <p><strong>সমাধান:</strong> পাঠ্যক্রম সংস্কার, শিক্ষক প্রশিক্ষণ, ও ডিজিটাল শিক্ষার প্রসার শিক্ষাব্যবস্থার উন্নতি ঘটাতে পারে।</p>
                    `
            }, {
                title: "পুঁজিবাদ ও অর্থনৈতিক বৈষম্য",
                tag: "অর্থনীতি",
                content: `
                        <p><i class="fas fa-chart-line" style="color:#3b8cff;"></i> পুঁজিবাদী অর্থব্যবস্থা বাংলাদেশে অর্থনৈতিক প্রবৃদ্ধি ঘটালেও বৈষম্য বাড়িয়েছে। সম্পদের অসম বণ্টন, শ্রমিকদের শোষণ, ও কর ফাঁকি পুঁজিবাদের অন্ধকার দিক।</p>
                        <p>বহুজাতিক কোম্পানির প্রভাব, কৃষকদের দারিদ্র্য, ও মধ্যবিত্তের সংকোচন—এই সমস্যাগুলো পুঁজিবাদী কাঠামোতে প্রকট।</p>
                        <div class="highlight-box"><i class="fas fa-lightbulb"></i> “পুঁজিবাদ অর্থনৈতিক স্বাধীনতা দেয়, কিন্তু সামাজিক ন্যায়বিচার নিশ্চিত করে না।”</div>
                        <p><strong>সমাধান:</strong> কর ব্যবস্থার সংস্কার, শ্রমিক অধিকার নিশ্চিত করা, ও ছোট ও মাঝারি শিল্পের উন্নয়ন পুঁজিবাদের নেতিবাচক প্রভাব কমাতে পারে।</p>
                    `
            }, {
                title: "সমাজতন্ত্রের চ্যালেঞ্জ",
                tag: "রাজনীতি",
                content: `
                        <p><i class="fas fa-handshake" style="color:#3b8cff;"></i> সমাজতন্ত্র সাম্যের আদর্শে বিশ্বাসী, কিন্তু বাস্তবে তা বাস্তবায়ন করা কঠিন। বাংলাদেশে সমাজতান্ত্রিক আন্দোলন দুর্বল, রাজনৈতিক দলগুলোর মধ্যে মতপার্থক্য, ও অর্থনৈতিক নীতিতে পুঁজিবাদী প্রবণতা সমাজতন্ত্রকে চ্যালেঞ্জের মুখে ফেলেছে।</p>
                        <p>রাষ্ট্রীয় সম্পদের অপব্যবহার, দুর্নীতি, ও আমলাতান্ত্রিক জটিলতা সমাজতন্ত্রের মূল বাধা।</p>
                        <div class="highlight-box"><i class="fas fa-quote-left"></i> “সমাজতন্ত্র মানে রাষ্ট্রের সবকিছু নিয়ন্ত্রণ নয়, বরং জনকল্যাণ ও সুযোগের সমতা নিশ্চিত করা।”</div>
                        <p><strong>সমাধান:</strong> দুর্নীতি দমন, স্বচ্ছতা বাড়ানো, ও জনগণের অংশগ্রহণ সমাজতন্ত্রকে কার্যকর করতে পারে।</p>
                    `
            }];

            // DOM elements
            const listEl = document.getElementById('topicList');
            const homepageView = document.getElementById('homepageView');
            const topicView = document.getElementById('topicView');
            const titleEl = document.getElementById('topicTitle');
            const tagEl = document.getElementById('topicTag');
            const contentEl = document.getElementById('articleContent');
            const pageIndicator = document.getElementById('pageIndicator');
            const homeBtn = document.getElementById('homeBtn');

            let activeIndex = -1;

            // render sidebar
            function renderSidebar() {
                listEl.innerHTML = '';
                const iconMap = ['fa-landmark', 'fa-people-arrows', 'fa-venus', 'fa-chalkboard-teacher', 'fa-chart-line',
                    'fa-handshake'
                ];
                topics.forEach((item, idx) => {
                    const li = document.createElement('li');
                    li.dataset.index = idx;

                    const icon = document.createElement('i');
                    icon.className = `fas ${iconMap[idx]}`;
                    li.appendChild(icon);

                    const shortName = item.title.length > 18 ? item.title.slice(0, 18) + '…' : item.title;
                    const span = document.createElement('span');
                    span.textContent = shortName;
                    li.appendChild(span);

                    const badge = document.createElement('span');
                    badge.className = 'badge';
                    badge.textContent = item.tag;
                    li.appendChild(badge);

                    const arrow = document.createElement('i');
                    arrow.className = 'fas fa-arrow-right';
                    arrow.style.marginLeft = '6px';
                    arrow.style.fontSize = '0.7rem';
                    li.appendChild(arrow);

                    if (idx === activeIndex) li.classList.add('active');

                    li.addEventListener('click', function() {
                        const newIndex = parseInt(this.dataset.index, 10);
                        if (newIndex === activeIndex) return;
                        showTopic(newIndex);
                    });

                    listEl.appendChild(li);
                });
            }

            function showTopic(index) {
                if (index < 0 || index >= topics.length) return;
                activeIndex = index;

                homepageView.classList.add('hidden');
                topicView.classList.remove('hidden');

                const items = listEl.querySelectorAll('li');
                items.forEach((li, i) => {
                    li.classList.toggle('active', i === index);
                });

                const topic = topics[index];
                titleEl.textContent = topic.title;
                tagEl.textContent = topic.tag;
                contentEl.innerHTML = topic.content;
                pageIndicator.innerHTML = `<i class="fas fa-arrow-right"></i> ${index+1}/${topics.length}`;
            }

            function showHomepage() {
                activeIndex = -1;
                homepageView.classList.remove('hidden');
                topicView.classList.add('hidden');

                const items = listEl.querySelectorAll('li');
                items.forEach(li => li.classList.remove('active'));
            }

            function init() {
                renderSidebar();
                showHomepage();
                homeBtn.addEventListener('click', showHomepage);
            }

            init();
        })();
    </script>
</body>
</html>
