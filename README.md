# Rec-Rux- :root {
    --yellow: #ffd400;
    --yellow-bright: #ffe600;
    --black: #050505;
    --black-2: #0b0b0b;
    --black-3: #111111;
    --panel: #151515;
    --border: #292929;
    --white: #ffffff;
    --grey: #a5a5a5;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    background: var(--black);
    color: var(--white);
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.6;
}

a {
    color: inherit;
    text-decoration: none;
}

button,
a {
    -webkit-tap-highlight-color: transparent;
}

button {
    font-family: inherit;
}

.container {
    width: min(1180px, calc(100% - 40px));
    margin: auto;
}


/* NAVBAR */

.navbar {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;

    background: rgba(5, 5, 5, 0.94);
    border-bottom: 1px solid var(--border);
    backdrop-filter: blur(12px);
}

.nav-inner {
    min-height: 78px;

    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 24px;
}

.logo {
    font-size: 22px;
    font-weight: 900;
    letter-spacing: 2px;
    white-space: nowrap;
}

.logo span {
    color: var(--yellow);
}

nav {
    display: flex;
    align-items: center;
    gap: 18px;
}

nav a {
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.7px;
    color: #c8c8c8;

    transition:
        color 0.2s ease,
        transform 0.2s ease;
}

nav a:hover {
    color: var(--yellow);
    transform: translateY(-1px);
}

.nav-button {
    padding: 11px 15px;

    background: var(--yellow);
    color: var(--black);

    font-size: 11px;
    font-weight: 900;
    letter-spacing: 0.7px;

    transition:
        background 0.2s ease,
        transform 0.2s ease;
}

.nav-button:hover {
    background: var(--yellow-bright);
    transform: translateY(-2px);
}

.mobile-menu {
    display: none;

    border: 1px solid var(--yellow);
    background: transparent;
    color: var(--yellow);

    padding: 9px 12px;

    font-size: 11px;
    font-weight: 900;
}


/* HERO */

.hero {
    min-height: 100vh;
    padding-top: 78px;

    position: relative;
    overflow: hidden;

    display: flex;
    align-items: center;
}

.hero-grid {
    position: absolute;
    inset: 0;

    opacity: 0.17;

    background-image:
        linear-gradient(
            rgba(255, 212, 0, 0.2) 1px,
            transparent 1px
        ),
        linear-gradient(
            90deg,
            rgba(255, 212, 0, 0.2) 1px,
            transparent 1px
        );

    background-size: 70px 70px;

    mask-image: linear-gradient(
        to bottom,
        black,
        transparent
    );
}

.hero-content {
    position: relative;
    z-index: 2;
}

.eyebrow {
    color: var(--yellow);
    font-size: 12px;
    font-weight: 900;
    letter-spacing: 3px;
    margin-bottom: 18px;
}

.hero h1 {
    max-width: 900px;

    font-size: clamp(70px, 13vw, 170px);
    line-height: 0.83;

    font-weight: 1000;
    letter-spacing: -7px;
}

.hero h1 span {
    color: var(--yellow);
}

.hero-text {
    max-width: 580px;
    margin-top: 35px;

    color: var(--grey);
    font-size: 18px;
}

.hero-buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;

    margin-top: 30px;
}

.button {
    display: inline-flex;
    align-items: center;
    justify-content: center;

    min-height: 48px;
    padding: 0 22px;

    border: 1px solid var(--yellow);

    font-size: 12px;
    font-weight: 900;
    letter-spacing: 1px;

    cursor: pointer;

    transition:
        transform 0.2s ease,
        background 0.2s ease,
        color 0.2s ease;
}

.button:hover {
    transform: translateY(-3px);
}

.button.primary {
    background: var(--yellow);
    color: var(--black);
}

.button.primary:hover {
    background: var(--yellow-bright);
}

.button.secondary {
    background: transparent;
    color: var(--yellow);
}

.button.secondary:hover {
    background: var(--yellow);
    color: var(--black);
}

.hero-stats {
    display: grid;
    grid-template-columns: repeat(4, 1fr);

    max-width: 650px;
    margin-top: 70px;

    border-top: 1px solid var(--border);
}

.hero-stats div {
    padding: 20px 15px;
    border-right: 1px solid var(--border);
}

.hero-stats div:last-child {
    border-right: 0;
}

.hero-stats strong {
    display: block;

    color: var(--yellow);

    font-size: 18px;
}

.hero-stats span {
    color: var(--grey);
    font-size: 11px;
    text-transform: uppercase;
}


/* SECTIONS */

.section {
    padding: 120px 0;
}

.dark-section {
    background: var(--black-2);
}

.section-heading {
    max-width: 760px;
    margin-bottom: 55px;
}

.section-heading h2,
.final-cta h2 {
    font-size: clamp(40px, 7vw, 82px);
    line-height: 0.95;
    letter-spacing: -3px;
}

.section-heading p:not(.eyebrow) {
    margin-top: 22px;
    color: var(--grey);
    max-width: 650px;
}

.split-heading {
    display: flex;
    align-items: end;
    justify-content: space-between;
    gap: 50px;

    max-width: none;
}

.split-heading > p {
    max-width: 400px;
}


/* GAME */

.game-layout {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 18px;
}

.game-panel {
    min-height: 290px;

    padding: 35px;

    background: var(--panel);
    border: 1px solid var(--border);

    position: relative;

    transition:
        border-color 0.2s ease,
        transform 0.2s ease;
}

.game-panel:hover {
    border-color: var(--yellow);
    transform: translateY(-4px);
}

.game-panel.large {
    grid-row: span 2;
    min-height: 600px;

    display: flex;
    flex-direction: column;
    justify-content: end;

    background:
        linear-gradient(
            135deg,
            #191919,
            #0b0b0b
        );
}

.panel-number {
    position: absolute;
    top: 25px;
    right: 25px;

    color: var(--yellow);
    font-size: 13px;
    font-weight: 900;
}

.game-panel h3 {
    font-size: 38px;
    line-height: 1;
}

.game-panel p {
    max-width: 500px;
    margin: 18px 0 25px;

    color: var(--grey);
}

.text-button {
    border: 0;
    background: transparent;
    color: var(--yellow);

    font-size: 11px;
    font-weight: 900;
    letter-spacing: 1px;

    cursor: pointer;
}


/* FEATURES */

.feature-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;

    background: var(--border);
    border: 1px solid var(--border);
}

.feature-card {
    min-height: 250px;

    padding: 30px;

    background: var(--black-2);
}

.feature-card span {
    color: var(--yellow);
    font-weight: 900;
}

.feature-card h3 {
    margin: 55px 0 10px;

    font-size: 25px;
}

.feature-card p {
    color: var(--grey);
}


/* GAMES */

.games-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
}

.game-card {
    padding: 30px;

    min-height: 300px;

    border: 1px solid var(--border);
    background: var(--panel);

    display: flex;
    flex-direction: column;

    transition:
        border-color 0.2s ease,
        transform 0.2s ease;
}

.game-card:hover {
    border-color: var(--yellow);
    transform: translateY(-5px);
}

.game-number {
    color: var(--yellow);
    font-weight: 900;
}

.game-card h3 {
    margin-top: auto;

    font-size: 31px;
}

.game-card p {
    margin: 12px 0 25px;
    color: var(--grey);
}

.game-action {
    width: max-content;

    border: 1px solid var(--yellow);

    padding: 10px 18px;

    background: transparent;
    color: var(--yellow);

    font-size: 11px;
    font-weight: 900;

    cursor: pointer;
}

.game-action:hover {
    background: var(--yellow);
    color: var(--black);
}


/* COMMUNITY */

.community-section {
    padding: 80px 0;
}

.community-box {
    padding: 65px;

    background: var(--yellow);
    color: var(--black);

    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 50px;
}

.community-box .eyebrow {
    color: var(--black);
}

.community-box h2 {
    max-width: 700px;

    font-size: clamp(35px, 6vw, 70px);
    line-height: 0.95;
}

.community-box p:not(.eyebrow):not(.community-note) {
    max-width: 650px;
    margin-top: 20px;
}

.community-box .button.primary {
    background: var(--black);
    border-color: var(--black);
    color: var(--yellow);
}

.community-box .button.primary:hover {
    background: #202020;
}

.community-note {
    margin-top: 12px;

    text-align: center;

    font-size: 10px;
    font-weight: 900;
    letter-spacing: 1px;
}


/* EVENTS */

.timeline {
    border-top: 1px solid var(--border);
}

.event {
    display: grid;
    grid-template-columns: 180px 1fr;

    padding: 30px 0;

    border-bottom: 1px solid var(--border);
}

.event-date {
    color: var(--yellow);
    font-size: 11px;
    font-weight: 900;
}

.event-content h3 {
    font-size: 28px;
}

.event-content p {
    max-width: 650px;
    margin: 10px 0;

    color: var(--grey);
}

.event-content span {
    color: var(--yellow);

    font-size: 10px;
    font-weight: 900;
    letter-spacing: 1px;
}


/* LEADERBOARD */

.leaderboard {
    border: 1px solid var(--border);
}

.leader-row {
    display: grid;
    grid-template-columns: 100px 1fr 150px 150px;

    padding: 22px 25px;

    border-bottom: 1px solid var(--border);
}

.leader-row:last-child {
    border-bottom: 0;
}

.leader-header {
    background: var(--yellow);
    color: var(--black);

    font-size: 10px;
    font-weight: 900;
}

.leader-row:not(.leader-header):hover {
    background: var(--panel);
}

.leader-row:not(.leader-header) span:first-child {
    color: var(--yellow);
    font-weight: 900;
}


/* CREATORS */

.creator-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
}

.creator-card {
    padding: 40px;

    min-height: 300px;

    border: 1px solid var(--border);
}

.creator-card span {
    color: var(--yellow);
    font-weight: 900;
}

.creator-card h3 {
    margin-top: 90px;
    font-size: 30px;
}

.creator-card p {
    margin-top: 10px;
    color: var(--grey);
}


/* NEWS */

.news-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
}

.news-card {
    padding: 35px;

    min-height: 320px;

    border: 1px solid var(--border);
    background: var(--panel);
}

.news-card > span {
    color: var(--yellow);

    font-size: 10px;
    font-weight: 900;
    letter-spacing: 1px;
}

.news-card h3 {
    margin-top: 65px;
    font-size: 27px;
}

.news-card p {
    margin: 12px 0 25px;
    color: var(--grey);
}


/* FAQ */

.faq {
    border-top: 1px solid var(--border);
}

details {
    border-bottom: 1px solid var(--border);
}

summary {
    padding: 25px 0;

    cursor: pointer;

    font-size: 19px;
    font-weight: 800;

    list-style: none;
}

summary::-webkit-details-marker {
    display: none;
}

summary::after {
    content: "+";

    float: right;

    color: var(--yellow);
}

details[open] summary::after {
    content: "−";
}

details p {
    max-width: 700px;

    padding: 0 0 25px;

    color: var(--grey);
}


/* FINAL CTA */

.final-cta {
    padding: 150px 0;

    text-align: center;

    background:
        linear-gradient(
            rgba(255, 212, 0, 0.08),
            transparent
        );
}

.final-cta .eyebrow {
    margin-bottom: 25px;
}

.final-cta h2 {
    max-width: 1000px;
    margin: auto;
}

.final-cta p:not(.eyebrow) {
    margin-top: 20px;
    color: var(--grey);
}


/* FOOTER */

footer {
    background: #020202;
    border-top: 1px solid var(--border);
}

.footer-grid {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr 1fr;

    gap: 40px;

    padding: 70px 0;
}

.footer-grid > div:first-child p {
    margin-top: 12px;
    color: var(--grey);
}

.footer-grid h4 {
    margin-bottom: 15px;

    color: var(--yellow);

    font-size: 11px;
    letter-spacing: 1px;
}

.footer-grid a:not(.logo) {
    display: block;

    margin: 8px 0;

    color: var(--grey);

    font-size: 13px;
}

.footer-grid a:hover {
    color: var(--yellow);
}

.footer-bottom {
    border-top: 1px solid var(--border);
}

.footer-bottom .container {
    min-height: 65px;

    display: flex;
    align-items: center;
    justify-content: space-between;

    color: #666;

    font-size: 11px;
}


/* MODAL */

.modal {
    position: fixed;
    inset: 0;

    z-index: 2000;

    display: none;
    align-items: center;
    justify-content: center;

    padding: 20px;

    background: rgba(0, 0, 0, 0.85);
}

.modal.active {
    display: flex;
}

.modal-box {
    width: min(800px, 100%);

    padding: 40px;

    background: var(--black-2);
    border: 1px solid var(--yellow);

    position: relative;
}

.modal-close {
    position: absolute;
    top: 20px;
    right: 20px;

    padding: 8px 12px;

    background: transparent;
    border: 1px solid var(--border);
    color: var(--grey);

    cursor: pointer;

    font-size: 10px;
    font-weight: 900;
}

.modal-close:hover {
    border-color: var(--yellow);
    color: var(--yellow);
}

.modal-box h2 {
    font-size: 50px;
}

.modal-box > p:not(.eyebrow) {
    color: var(--grey);
}


/* FAKE GAME */

.fake-game {
    margin-top: 30px;

    border: 1px solid var(--border);
    padding: 20px;
}

.game-score {
    color: var(--yellow);

    font-size: 12px;
    font-weight: 900;
}

.game-stage {
    height: 250px;

    margin: 15px 0;

    position: relative;
    overflow: hidden;

    background:
        linear-gradient(
            90deg,
            transparent 49%,
            rgba(255, 212, 0, 0.08) 50%,
            transparent 51%
        );

    border: 1px solid var(--border);
}

.player,
.target {
    width: 35px;
    height: 35px;

    position: absolute;
}

.player {
    left: 30px;
    bottom: 30px;

    background: var(--yellow);
}

.target {
    right: 40px;
    top: 50px;

    background: var(--white);
}


/* RESPONSIVE */

@media (max-width: 1100px) {

    nav {
        display: none;
    }

    .mobile-menu {
        display: block;
    }

    .nav-button {
        display: none;
    }

    .game-layout {
        grid-template-columns: 1fr;
    }

    .game-panel.large {
        grid-row: auto;
        min-height: 400px;
    }

    .feature-grid,
    .games-grid,
    .creator-grid,
    .news-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .community-box {
        flex-direction: column;
        align-items: flex-start;
    }

}

@media (max-width: 700px) {

    .container {
        width: min(100% - 28px, 1180px);
    }

    .section {
        padding: 80px 0;
    }

    .hero h1 {
        font-size: clamp(55px, 18vw, 100px);
        letter-spacing: -4px;
    }

    .hero-text {
        font-size: 16px;
    }

    .hero-stats {
        grid-template-columns: repeat(2, 1fr);
    }

    .hero-stats div:nth-child(2) {
        border-right: 0;
    }

    .feature-grid,
    .games-grid,
    .creator-grid,
    .news-grid {
        grid-template-columns: 1fr;
    }

    .split-heading {
        display: block;
    }

    .split-heading > p {
        margin-top: 20px;
    }

    .community-box {
        padding: 35px 25px;
    }

    .event {
        grid-template-columns: 1fr;
        gap: 12px;
    }

    .leader-row {
        grid-template-columns: 55px 1fr 70px 90px;
        padding: 18px 12px;

        font-size: 11px;
    }

    .footer-grid {
        grid-template-columns: 1fr 1fr;
    }

    .footer-bottom .container {
        padding: 18px 0;

        flex-direction: column;
        align-items: flex-start;
        gap: 5px;
    }

    .modal-box {
        padding: 25px;
    }

    .modal-box h2 {
        font-size: 38px;
    }

}<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Rec Rux | Play. Create. Connect.</title>

    <meta
        name="description"
        content="Rec Rux is a community gaming platform built for players, creators, events and competitive challenges."
    >

    <link rel="stylesheet" href="style.css">
</head>

<body>

    <!-- =========================
         HEADER
    ========================== -->

    <header class="navbar">

        <div class="container nav-inner">

            <a href="#home" class="logo">
                REC <span>RUX</span>
            </a>

            <button class="mobile-menu" id="mobileMenu">
                MENU
            </button>

            <nav id="mainNav">

                <a href="#home">Home</a>
                <a href="#game">Game</a>
                <a href="#features">Features</a>
                <a href="#games">Games</a>
                <a href="#community">Community</a>
                <a href="#events">Events</a>
                <a href="#leaderboards">Leaderboards</a>
                <a href="#creators">Creators</a>
                <a href="#news">News</a>
                <a href="#support">Support</a>

            </nav>

            <a
                href="https://discord.gg/HbAxApTSu"
                target="_blank"
                rel="noopener noreferrer"
                class="nav-button"
            >
                JOIN COMMUNITY
            </a>

        </div>

    </header>


    <!-- =========================
         HERO
    ========================== -->

    <main>

        <section id="home" class="hero">

            <div class="hero-grid"></div>

            <div class="container hero-content">

                <p class="eyebrow">
                    WELCOME TO REC RUX
                </p>

                <h1>
                    PLAY.
                    <br>
                    CREATE.
                    <br>
                    <span>CONNECT.</span>
                </h1>

                <p class="hero-text">
                    Rec Rux is a gaming experience built around
                    creativity, competition, community and fun.
                </p>

                <div class="hero-buttons">

                    <a href="#game" class="button primary">
                        PLAY REC RUX
                    </a>

                    <a
                        href="https://discord.gg/HbAxApTSu"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="button secondary"
                    >
                        JOIN THE COMMUNITY
                    </a>

                </div>

                <div class="hero-stats">

                    <div>
                        <strong>01</strong>
                        <span>Gaming</span>
                    </div>

                    <div>
                        <strong>02</strong>
                        <span>Community</span>
                    </div>

                    <div>
                        <strong>03</strong>
                        <span>Creation</span>
                    </div>

                    <div>
                        <strong>04</strong>
                        <span>Competition</span>
                    </div>

                </div>

            </div>

        </section>


        <!-- =========================
             GAME
        ========================== -->

        <section id="game" class="section">

            <div class="container">

                <div class="section-heading">

                    <p class="eyebrow">
                        THE GAME
                    </p>

                    <h2>
                        ENTER REC RUX
                    </h2>

                    <p>
                        Explore a growing world filled with games,
                        challenges, social spaces and creator-made
                        experiences.
                    </p>

                </div>

                <div class="game-layout">

                    <div class="game-panel large">

                        <span class="panel-number">
                            01
                        </span>

                        <h3>
                            REC RUX HUB
                        </h3>

                        <p>
                            Your central destination for discovering
                            games, meeting players and finding the
                            latest Rec Rux activities.
                        </p>

                        <button
                            class="button primary launch-button"
                            data-game="Rec Rux Hub"
                        >
                            ENTER HUB
                        </button>

                    </div>

                    <div class="game-panel">

                        <span class="panel-number">
                            02
                        </span>

                        <h3>
                            CHALLENGES
                        </h3>

                        <p>
                            Take on rotating challenges and compete
                            for leaderboard positions.
                        </p>

                        <button
                            class="text-button launch-button"
                            data-game="Challenges"
                        >
                            VIEW CHALLENGES
                        </button>

                    </div>

                    <div class="game-panel">

                        <span class="panel-number">
                            03
                        </span>

                        <h3>
                            CREATOR WORLD
                        </h3>

                        <p>
                            Discover community-created experiences
                            and new content from Rec Rux creators.
                        </p>

                        <button
                            class="text-button launch-button"
                            data-game="Creator World"
                        >
                            EXPLORE CREATORS
                        </button>

                    </div>

                </div>

            </div>

        </section>


        <!-- =========================
             FEATURES
        ========================== -->

        <section id="features" class="section dark-section">

            <div class="container">

                <div class="section-heading">

                    <p class="eyebrow">
                        FEATURES
                    </p>

                    <h2>
                        BUILT FOR PLAYERS
                    </h2>

                </div>

                <div class="feature-grid">

                    <article class="feature-card">
                        <span>01</span>
                        <h3>Multiplayer</h3>
                        <p>
                            Play alongside friends and other members
                            of the Rec Rux community.
                        </p>
                    </article>

                    <article class="feature-card">
                        <span>02</span>
                        <h3>Mini Games</h3>
                        <p>
                            Jump into different game modes and
                            challenges whenever you want.
                        </p>
                    </article>

                    <article class="feature-card">
                        <span>03</span>
                        <h3>XP System</h3>
                        <p>
                            Earn experience by playing, completing
                            challenges and participating in events.
                        </p>
                    </article>

                    <article class="feature-card">
                        <span>04</span>
                        <h3>Achievements</h3>
                        <p>
                            Complete objectives and build your
                            collection of achievements.
                        </p>
                    </article>

                    <article class="feature-card">
                        <span>05</span>
                        <h3>Events</h3>
                        <p>
                            Participate in community events,
                            competitions and special activities.
                        </p>
                    </article>

                    <article class="feature-card">
                        <span>06</span>
                        <h3>Creator Tools</h3>
                        <p>
                            Give creators space to build and share
                            their own Rec Rux experiences.
                        </p>
                    </article>

                </div>

            </div>

        </section>


        <!-- =========================
             GAMES
        ========================== -->

        <section id="games" class="section">

            <div class="container">

                <div class="section-heading split-heading">

                    <div>
                        <p class="eyebrow">
                            GAME LIBRARY
                        </p>

                        <h2>
                            CHOOSE YOUR GAME
                        </h2>
                    </div>

                    <p>
                        The Rec Rux game library can grow with new
                        experiences and community creations.
                    </p>

                </div>

                <div class="games-grid">

                    <article class="game-card">
                        <div class="game-number">01</div>
                        <h3>Rux Run</h3>
                        <p>
                            Race through challenging obstacle courses.
                        </p>
                        <button
                            class="game-action launch-button"
                            data-game="Rux Run"
                        >
                            PLAY
                        </button>
                    </article>

                    <article class="game-card">
                        <div class="game-number">02</div>
                        <h3>Rux Race</h3>
                        <p>
                            Compete against players in fast races.
                        </p>
                        <button
                            class="game-action launch-button"
                            data-game="Rux Race"
                        >
                            PLAY
                        </button>
                    </article>

                    <article class="game-card">
                        <div class="game-number">03</div>
                        <h3>Rux Arena</h3>
                        <p>
                            Enter competitive multiplayer matches.
                        </p>
                        <button
                            class="game-action launch-button"
                            data-game="Rux Arena"
                        >
                            PLAY
                        </button>
                    </article>

                    <article class="game-card">
                        <div class="game-number">04</div>
                        <h3>Rux Party</h3>
                        <p>
                            Relax and play casual community games.
                        </p>
                        <button
                            class="game-action launch-button"
                            data-game="Rux Party"
                        >
                            PLAY
                        </button>
                    </article>

                    <article class="game-card">
                        <div class="game-number">05</div>
                        <h3>Rux Trials</h3>
                        <p>
                            Complete difficult tasks and earn rewards.
                        </p>
                        <button
                            class="game-action launch-button"
                            data-game="Rux Trials"
                        >
                            PLAY
                        </button>
                    </article>

                    <article class="game-card">
                        <div class="game-number">06</div>
                        <h3>Creator Games</h3>
                        <p>
                            Discover experiences made by the community.
                        </p>
                        <button
                            class="game-action launch-button"
                            data-game="Creator Games"
                        >
                            PLAY
                        </button>
                    </article>

                </div>

            </div>

        </section>


        <!-- =========================
             COMMUNITY
        ========================== -->

        <section id="community" class="section community-section">

            <div class="container community-box">

                <div>

                    <p class="eyebrow">
                        COMMUNITY
                    </p>

                    <h2>
                        JOIN THE REC RUX COMMUNITY
                    </h2>

                    <p>
                        Connect with players, talk about the game,
                        share ideas, discover events and stay updated
                        with everything happening in Rec Rux.
                    </p>

                </div>

                <div>

                    <a
                        href="https://discord.gg/HbAxApTSu"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="button primary large-button"
                    >
                        JOIN DISCORD
                    </a>

                    <p class="community-note">
                        Official Rec Rux Community
                    </p>

                </div>

            </div>

        </section>


        <!-- =========================
             EVENTS
        ========================== -->

        <section id="events" class="section dark-section">

            <div class="container">

                <div class="section-heading">

                    <p class="eyebrow">
                        EVENTS
                    </p>

                    <h2>
                        WHAT'S HAPPENING
                    </h2>

                </div>

                <div class="timeline">

                    <article class="event">

                        <div class="event-date">
                            EVENT 01
                        </div>

                        <div class="event-content">

                            <h3>
                                Community Game Night
                            </h3>

                            <p>
                                Join other Rec Rux players for a
                                community gaming session.
                            </p>

                            <span>
                                COMMUNITY EVENT
                            </span>

                        </div>

                    </article>

                    <article class="event">

                        <div class="event-date">
                            EVENT 02
                        </div>

                        <div class="event-content">

                            <h3>
                                Rux Challenge
                            </h3>

                            <p>
                                Take on a limited challenge and try
                                to reach the top of the leaderboard.
                            </p>

                            <span>
                                COMPETITION
                            </span>

                        </div>

                    </article>

                    <article class="event">

                        <div class="event-date">
                            EVENT 03
                        </div>

                        <div class="event-content">

                            <h3>
                                Creator Showcase
                            </h3>

                            <p>
                                Discover new games and experiences
                                created by the Rec Rux community.
                            </p>

                            <span>
                                CREATOR EVENT
                            </span>

                        </div>

                    </article>

                </div>

            </div>

        </section>


        <!-- =========================
             LEADERBOARDS
        ========================== -->

        <section id="leaderboards" class="section">

            <div class="container">

                <div class="section-heading">

                    <p class="eyebrow">
                        COMPETITION
                    </p>

                    <h2>
                        LEADERBOARDS
                    </h2>

                </div>

                <div class="leaderboard">

                    <div class="leader-row leader-header">
                        <span>RANK</span>
                        <span>PLAYER</span>
                        <span>LEVEL</span>
                        <span>XP</span>
                    </div>

                    <div class="leader-row">
                        <span>01</span>
                        <span>Player One</span>
                        <span>50</span>
                        <span>125000</span>
                    </div>

                    <div class="leader-row">
                        <span>02</span>
                        <span>Player Two</span>
                        <span>47</span>
                        <span>113500</span>
                    </div>

                    <div class="leader-row">
                        <span>03</span>
                        <span>Player Three</span>
                        <span>45</span>
                        <span>108200</span>
                    </div>

                    <div class="leader-row">
                        <span>04</span>
                        <span>Player Four</span>
                        <span>42</span>
                        <span>99500</span>
                    </div>

                    <div class="leader-row">
                        <span>05</span>
                        <span>Player Five</span>
                        <span>40</span>
                        <span>92000</span>
                    </div>

                </div>

            </div>

        </section>


        <!-- =========================
             CREATORS
        ========================== -->

        <section id="creators" class="section dark-section">

            <div class="container">

                <div class="section-heading">

                    <p class="eyebrow">
                        CREATOR PROGRAM
                    </p>

                    <h2>
                        BUILD YOUR WORLD
                    </h2>

                    <p>
                        Rec Rux gives creators a place to experiment,
                        design new experiences and share their work.
                    </p>

                </div>

                <div class="creator-grid">

                    <div class="creator-card">
                        <span>01</span>
                        <h3>CREATE</h3>
                        <p>
                            Build your own game concepts and
                            experiences.
                        </p>
                    </div>

                    <div class="creator-card">
                        <span>02</span>
                        <h3>SHARE</h3>
                        <p>
                            Publish your creations for the community
                            to discover.
                        </p>
                    </div>

                    <div class="creator-card">
                        <span>03</span>
                        <h3>GROW</h3>
                        <p>
                            Build a community around your creations.
                        </p>
                    </div>

                </div>

            </div>

        </section>


        <!-- =========================
             NEWS
        ========================== -->

        <section id="news" class="section">

            <div class="container">

                <div class="section-heading">

                    <p class="eyebrow">
                        NEWS
                    </p>

                    <h2>
                        LATEST REC RUX
                    </h2>

                </div>

                <div class="news-grid">

                    <article class="news-card">

                        <span>
                            UPDATE
                        </span>

                        <h3>
                            Welcome to Rec Rux
                        </h3>

                        <p>
                            Discover the new Rec Rux experience and
                            everything being built for the community.
                        </p>

                        <button class="text-button">
                            READ MORE
                        </button>

                    </article>

                    <article class="news-card">

                        <span>
                            COMMUNITY
                        </span>

                        <h3>
                            Join the Discord
                        </h3>

                        <p>
                            Connect with other Rec Rux players and
                            keep up with announcements.
                        </p>

                        <a
                            href="https://discord.gg/HbAxApTSu"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="text-button"
                        >
                            JOIN NOW
                        </a>

                    </article>

                    <article class="news-card">

                        <span>
                            DEVELOPMENT
                        </span>

                        <h3>
                            More Games Coming
                        </h3>

                        <p>
                            New experiences, challenges and creator
                            content can continue to expand Rec Rux.
                        </p>

                        <button class="text-button">
                            DISCOVER
                        </button>

                    </article>

                </div>

            </div>

        </section>


        <!-- =========================
             FAQ
        ========================== -->

        <section id="support" class="section dark-section">

            <div class="container">

                <div class="section-heading">

                    <p class="eyebrow">
                        SUPPORT
                    </p>

                    <h2>
                        FREQUENTLY ASKED QUESTIONS
                    </h2>

                </div>

                <div class="faq">

                    <details>
                        <summary>
                            What is Rec Rux?
                        </summary>

                        <p>
                            Rec Rux is a gaming and community platform
                            focused on games, creators, challenges and
                            social experiences.
                        </p>
                    </details>

                    <details>
                        <summary>
                            How can I join the community?
                        </summary>

                        <p>
                            You can join the official Rec Rux Discord
                            community using the Join Community button.
                        </p>
                    </details>

                    <details>
                        <summary>
                            Will more games be added?
                        </summary>

                        <p>
                            The platform is designed to support
                            additional games and community-created
                            experiences.
                        </p>
                    </details>

                    <details>
                        <summary>
                            Can I become a creator?
                        </summary>

                        <p>
                            Yes. The Rec Rux concept includes a
                            creator-focused section for developing and
                            sharing new experiences.
                        </p>
                    </details>

                </div>

            </div>

        </section>


        <!-- =========================
             FINAL CTA
        ========================== -->

        <section class="final-cta">

            <div class="container">

                <p class="eyebrow">
                    READY?
                </p>

                <h2>
                    WELCOME TO REC RUX
                </h2>

                <p>
                    Play. Create. Connect.
                </p>

                <div class="hero-buttons">

                    <a
                        href="#game"
                        class="button primary"
                    >
                        EXPLORE REC RUX
                    </a>

                    <a
                        href="https://discord.gg/HbAxApTSu"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="button secondary"
                    >
                        JOIN DISCORD
                    </a>

                </div>

            </div>

        </section>

    </main>


    <!-- =========================
         FOOTER
    ========================== -->

    <footer>

        <div class="container footer-grid">

            <div>

                <a href="#home" class="logo">
                    REC <span>RUX</span>
                </a>

                <p>
                    Play. Create. Connect.
                </p>

            </div>

            <div>

                <h4>EXPLORE</h4>

                <a href="#game">Game</a>
                <a href="#games">Games</a>
                <a href="#events">Events</a>
                <a href="#leaderboards">Leaderboards</a>

            </div>

            <div>

                <h4>COMMUNITY</h4>

                <a href="#community">Community</a>
                <a href="#creators">Creators</a>
                <a href="#news">News</a>

                <a
                    href="https://discord.gg/HbAxApTSu"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    Discord
                </a>

            </div>

            <div>

                <h4>SUPPORT</h4>

                <a href="#support">FAQ</a>
                <a href="#support">Help</a>

            </div>

        </div>

        <div class="footer-bottom">

            <div class="container">

                <span>
                    © 2026 Rec Rux. All rights reserved.
                </span>

                <span>
                    Built for the community.
                </span>

            </div>

        </div>

    </footer>


    <!-- GAME MODAL -->

    <div class="modal" id="gameModal">

        <div class="modal-box">

            <button class="modal-close" id="modalClose">
                CLOSE
            </button>

            <p class="eyebrow">
                REC RUX
            </p>

            <h2 id="modalTitle">
                GAME
            </h2>

            <p id="modalText">
                Loading game...
            </p>

            <div class="fake-game">

                <div class="game-score">
                    SCORE: <span id="score">0000</span>
                </div>

                <div class="game-stage">

                    <div class="player"></div>

                    <div class="target"></div>

                </div>

                <button
                    class="button primary"
                    id="startGame"
                >
                    START
                </button>

            </div>

        </div>

    </div>


    <script src="script.js"></script>

</body>
</html>https://discord.gg/HbAxApTSuhttps://effortless-toffee-ef9f95.netlify.app/const mobileMenu = document.getElementById("mobileMenu");
const mainNav = document.getElementById("mainNav");
if (mobileMenu && mainNav) {
    mobileMenu.addEventListener("click", () => {
        const isOpen = mainNav.classList.toggle("mobile-open");
        if (isOpen) {
            mainNav.style.cssText = "display:flex;position:absolute;top:78px;left:0;right:0;padding:20px;flex-direction:column;align-items:flex-start;background:#050505;border-bottom:1px solid #292929";
        } else {
            mainNav.removeAttribute("style");
        }
    });
    mainNav.querySelectorAll("a").forEach(link => {
        link.addEventListener("click", () => {
            mainNav.classList.remove("mobile-open");
            mainNav.removeAttribute("style");
        });
    });
}

const modal = document.getElementById("gameModal");
const modalClose = document.getElementById("modalClose");
const modalTitle = document.getElementById("modalTitle");
const modalText = document.getElementById("modalText");
const launchButtons = document.querySelectorAll(".launch-button");
launchButtons.forEach(button => {
    button.addEventListener("click", () => {
        const gameName = button.dataset.game || "Rec Rux";
        modalTitle.textContent = gameName.toUpperCase();
        modalText.textContent = `${gameName} is ready to launch. This browser prototype can be connected to the full Rec Rux game later.`;
        modal.classList.add("active");
        document.body.style.overflow = "hidden";
    });
});
function closeModal() {
    modal.classList.remove("active");
    document.body.style.overflow = "";
}
modalClose.addEventListener("click", closeModal);
modal.addEventListener("click", e => { if (e.target === modal) closeModal(); });
document.addEventListener("keydown", e => { if (e.key === "Escape") closeModal(); });

const startGame = document.getElementById("startGame");
const player = document.querySelector(".player");
const target = document.querySelector(".target");
const scoreElement = document.getElementById("score");
let score = 0, gameRunning = false, playerX = 30, playerY = 30, targetX = 0, targetY = 0;
function updateScore() { scoreElement.textContent = String(score).padStart(4, "0"); }
function randomTarget() {
    const stage = document.querySelector(".game-stage");
    if (!stage) return;
    targetX = Math.max(10, Math.floor(Math.random() * (stage.clientWidth - 60)));
    targetY = Math.max(10, Math.floor(Math.random() * (stage.clientHeight - 60)));
    target.style.left = `${targetX}px`;
    target.style.top = `${targetY}px`;
}
function movePlayer() { player.style.left = `${playerX}px`; player.style.bottom = `${playerY}px`; }
function startBrowserGame() {
    score = 0; updateScore(); gameRunning = true;
    playerX = 30; playerY = 30; movePlayer(); randomTarget();
}
startGame?.addEventListener("click", startBrowserGame);
document.addEventListener("keydown", e => {
    if (!gameRunning) return;
    const step = 15;
    if (e.key === "ArrowLeft") playerX -= step;
    if (e.key === "ArrowRight") playerX += step;
    if (e.key === "ArrowUp") playerY += step;
    if (e.key === "ArrowDown") playerY -= step;
    playerX = Math.max(0, Math.min(700, playerX));
    playerY = Math.max(0, Math.min(200, playerY));
    movePlayer(); checkCollision();
});
function checkCollision() {
    const pRect = player.getBoundingClientRect(), tRect = target.getBoundingClientRect();
    if (pRect.left < tRect.right && pRect.right > tRect.left && pRect.top < tRect.bottom && pRect.bottom > tRect.top) {
        score += 100; updateScore(); randomTarget();
    }
}

document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener("click", function(e) {
        const target = document.querySelector(this.getAttribute("href"));
        if (!target) return;
        e.preventDefault();
        target.scrollIntoView({ behavior: "smooth", block: "start" });
    });
});

const sections = document.querySelectorAll("section[id]");
const navLinks = document.querySelectorAll('nav a[href^="#"]');
const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
        navLinks.forEach(link => {
            link.classList.toggle("active", link.getAttribute("href") === `#${entry.target.id}` && entry.isIntersecting);
        });
    });
}, { threshold: 0.35 });
sections.forEach(section => observer.observe(section));

console.log("REC RUX | Play. Create. Connect.\nOfficial Discord: https://discord.gg/HbAxApTSu");
:root {
    --yellow: #ffd400;
    --yellow-bright: #ffe600;
    --black: #050505;
    --black-2: #0b0b0b;
    --black-3: #111111;
    --panel: #151515;
    --border: #292929;
    --white: #ffffff;
    --grey: #a5a5a5;
}

* { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { background: var(--black); color: var(--white); font-family: Arial, Helvetica, sans-serif; line-height: 1.6; }
a { color: inherit; text-decoration: none; }
button, a { -webkit-tap-highlight-color: transparent; }
button { font-family: inherit; }
.container { width: min(1180px, calc(100% - 40px)); margin: auto; }

/* NAVBAR */
.navbar { position: fixed; top: 0; left: 0; right: 0; z-index: 1000; background: rgba(5,5,5,0.94); border-bottom: 1px solid var(--border); backdrop-filter: blur(12px); }
.nav-inner { min-height: 78px; display: flex; align-items: center; justify-content: space-between; gap: 24px; }
.logo { font-size: 22px; font-weight: 900; letter-spacing: 2px; white-space: nowrap; }
.logo span { color: var(--yellow); }
nav { display: flex; align-items: center; gap: 18px; }
nav a { font-size: 12px; font-weight: 700; letter-spacing: 0.7px; color: #c8c8c8; transition: color 0.2s, transform 0.2s; }
nav a:hover { color: var(--yellow); transform: translateY(-1px); }
.nav-button { padding: 11px 15px; background: var(--yellow); color: var(--black); font-size: 11px; font-weight: 900; letter-spacing: 0.7px; transition: background 0.2s, transform 0.2s; }
.nav-button:hover { background: var(--yellow-bright); transform: translateY(-2px); }
.mobile-menu { display: none; border: 1px solid var(--yellow); background: transparent; color: var(--yellow); padding: 9px 12px; font-size: 11px; font-weight: 900; }

/* HERO */
.hero { min-height: 100vh; padding-top: 78px; position: relative; overflow: hidden; display: flex; align-items: center; }
.hero-grid { position: absolute; inset: 0; opacity: 0.17; background-image: linear-gradient(rgba(255,212,0,0.2) 1px, transparent 1px), linear-gradient(90deg, rgba(255,212,0,0.2) 1px, transparent 1px); background-size: 70px 70px; mask-image: linear-gradient(to bottom, black, transparent); }
.hero-content { position: relative; z-index: 2; }
.eyebrow { color: var(--yellow); font-size: 12px; font-weight: 900; letter-spacing: 3px; margin-bottom: 18px; }
.hero h1 { max-width: 900px; font-size: clamp(70px, 13vw, 170px); line-height: 0.83; font-weight: 1000; letter-spacing: -7px; }
.hero h1 span { color: var(--yellow); }
.hero-text { max-width: 580px; margin-top: 35px; color: var(--grey); font-size: 18px; }
.hero-buttons { display: flex; flex-wrap: wrap; gap: 12px; margin-top: 30px; }
.button { display: inline-flex; align-items: center; justify-content: center; min-height: 48px; padding: 0 22px; border: 1px solid var(--yellow); font-size: 12px; font-weight: 900; letter-spacing: 1px; cursor: pointer; transition: transform 0.2s, background 0.2s, color 0.2s; }
.button:hover { transform: translateY(-3px); }
.button.primary { background: var(--yellow); color: var(--black); }
.button.primary:hover { background: var(--yellow-bright); }
.button.secondary { background: transparent; color: var(--yellow); }
.button.secondary:hover { background: var(--yellow); color: var(--black); }
.hero-stats { display: grid; grid-template-columns: repeat(4,1fr); max-width: 650px; margin-top: 70px; border-top: 1px solid var(--border); }
.hero-stats div { padding: 20px 15px; border-right: 1px solid var(--border); }
.hero-stats div:last-child { border-right: 0; }
.hero-stats strong { display: block; color: var(--yellow); font-size: 18px; }
.hero-stats span { color: var(--grey); font-size: 11px; text-transform: uppercase; }

/* SECTIONS */
.section { padding: 120px 0; }
.dark-section { background: var(--black-2); }
.section-heading { max-width: 760px; margin-bottom: 55px; }
.section-heading h2, .final-cta h2 { font-size: clamp(40px,7vw,82px); line-height: 0.95; letter-spacing: -3px; }
.section-heading p:not(.eyebrow) { margin-top: 22px; color: var(--grey); max-width: 650px; }
.split-heading { display: flex; align-items: end; justify-content: space-between; gap: 50px; max-width: none; }
.split-heading > p { max-width: 400px; }

/* GAME */
.game-layout { display: grid; grid-template-columns: 2fr 1fr; gap: 18px; }
.game-panel { min-height: 290px; padding: 35px; background: var(--panel); border: 1px solid var(--border); position: relative; transition: border-color 0.2s, transform 0.2s; }
.game-panel:hover { border-color: var(--yellow); transform: translateY(-4px); }
.game-panel.large { grid-row: span 2; min-height: 600px; display: flex; flex-direction: column; justify-content: end; background: linear-gradient(135deg, #191919, #0b0b0b); }
.panel-number { position: absolute; top: 25px; right: 25px; color: var(--yellow); font-size: 13px; font-weight: 900; }
.game-panel h3 { font-size: 38px; line-height: 1; }
.game-panel p { max-width: 500px; margin: 18px 0 25px; color: var(--grey); }
.text-button { border: 0; background: transparent; color: var(--yellow); font-size: 11px; font-weight: 900; letter-spacing: 1px; cursor: pointer; }

/* FEATURES */
.feature-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 1px; background: var(--border); border: 1px solid var(--border); }
.feature-card { min-height: 250px; padding: 30px; background: var(--black-2); }
.feature-card span { color: var(--yellow); font-weight: 900; }
.feature-card h3 { margin: 55px 0 10px; font-size: 25px; }
.feature-card p { color: var(--grey); }

/* GAMES */
.games-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 16px; }
.game-card { padding: 30px; min-height: 300px; border: 1px solid var(--border); background: var(--panel); display: flex; flex-direction: column; transition: border-color 0.2s, transform 0.2s; }
.game-card:hover { border-color: var(--yellow); transform: translateY(-5px); }
.game-number { color: var(--yellow); font-weight: 900; }
.game-card h3 { margin-top: auto; font-size: 31px; }
.game-card p { margin: 12px 0 25px; color: var(--grey); }
.game-action { width: max-content; border: 1px solid var(--yellow); padding: 10px 18px; background: transparent; color: var(--yellow); font-size: 11px; font-weight: 900; cursor: pointer; }
.game-action:hover { background: var(--yellow); color: var(--black); }

/* COMMUNITY */
.community-section { padding: 80px 0; }
.community-box { padding: 65px; background: var(--yellow); color: var(--black); display: flex; align-items: center; justify-content: space-between; gap: 50px; }
.community-box .eyebrow { color: var(--black); }
.community-box h2 { max-width: 700px; font-size: clamp(35px,6vw,70px); line-height: 0.95; }
.community-box p:not(.eyebrow):not(.community-note) { max-width: 650px; margin-top: 20px; }
.community-box .button.primary { background: var(--black); border-color: var(--black); color: var(--yellow); }
.community-box .button.primary:hover { background: #202020; }
.community-note { margin-top: 12px; text-align: center; font-size: 10px; font-weight: 900; letter-spacing: 1px; }

/* EVENTS */
.timeline { border-top: 1px solid var(--border); }
.event { display: grid; grid-template-columns: 180px 1fr; padding: 30px 0; border-bottom: 1px solid var(--border); }
.event-date { color: var(--yellow); font-size: 11px; font-weight: 900; }
.event-content h3 { font-size: 28px; }
.event-content p { max-width: 650px; margin: 10px 0; color: var(--grey); }
.event-content span { color: var(--yellow); font-size: 10px; font-weight: 900; letter-spacing: 1px; }

/* LEADERBOARD */
.leaderboard { border: 1px solid var(--border); }
.leader-row { display: grid; grid-template-columns: 100px 1fr 150px 150px; padding: 22px 25px; border-bottom: 1px solid var(--border); }
.leader-row:last-child { border-bottom: 0; }
.leader-header { background: var(--yellow); color: var(--black); font-size: 10px; font-weight: 900; }
.leader-row:not(.leader-header):hover { background: var(--panel); }
.leader-row:not(.leader-header) span:first-child { color: var(--yellow); font-weight: 900; }

/* CREATORS */
.creator-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 16px; }
.creator-card { padding: 40px; min-height: 300px; border: 1px solid var(--border); }
.creator-card span { color: var(--yellow); font-weight: 900; }
.creator-card h3 { margin-top: 90px; font-size: 30px; }
.creator-card p { margin-top: 10px; color: var(--grey); }

/* NEWS */
.news-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 16px; }
.news-card { padding: 35px; min-height: 320px; border: 1px solid var(--border); background: var(--panel); }
.news-card > span { color: var(--yellow); font-size: 10px; font-weight: 900; letter-spacing: 1px; }
.news-card h3 { margin-top: 65px; font-size: 27px; }
.news-card p { margin: 12px 0 25px; color: var(--grey); }

/* FAQ */
.faq { border-top: 1px solid var(--border); }
details { border-bottom: 1px solid var(--border); }
summary { padding: 25px 0; cursor: pointer; font-size: 19px; font-weight: 800; list-style: none; }
summary::-webkit-details-marker { display: none; }
summary::after { content: "+"; float: right; color: var(--yellow); }
details[open] summary::after { content: "−"; }
details p { max-width: 700px; padding: 0 0 25px; color: var(--grey); }

/* FINAL CTA */
.final-cta { padding: 150px 0; text-align: center; background: linear-gradient(rgba(255,212,0,0.08), transparent); }
.final-cta .eyebrow { margin-bottom: 25px; }
.final-cta h2 { max-width: 1000px; margin: auto; }
.final-cta p:not(.eyebrow) { margin-top: 20px; color: var(--grey); }

/* FOOTER */
footer { background: #020202; border-top: 1px solid var(--border); }
.footer-grid { display: grid; grid-template-columns: 2fr 1fr 1fr 1fr; gap: 40px; padding: 70px 0; }
.footer-grid > div:first-child p { margin-top: 12px; color: var(--grey); }
.footer-grid h4 { margin-bottom: 15px; color: var(--yellow); font-size: 11px; letter-spacing: 1px; }
.footer-grid a:not(.logo) { display: block; margin: 8px 0; color: var(--grey); font-size: 13px; }
.footer-grid a:hover { color: var(--yellow); }
.footer-bottom { border-top: 1px solid var(--border); }
.footer-bottom .container { min-height: 65px; display: flex; align-items: center; justify-content: space-between; color: #666; font-size: 11px; }

/* MODAL */
.modal { position: fixed; inset: 0; z-index: 2000; display: none; align-items: center; justify-content: center; padding: 20px; background: rgba(0,0,0,0.85); }
.modal.active { display: flex; }
.modal-box { width: min(800px,100%); padding: 40px; background: var(--black-2); border: 1px solid var(--yellow); position: relative; }
.modal-close { position: absolute; top: 20px; right: 20px; padding: 8px 12px; background: transparent; border: 1px solid var(--border); color: var(--grey); cursor: pointer; font-size: 10px; font-weight: 900; }
.modal-close:hover { border-color: var(--yellow); color: var(--yellow); }
.modal-box h2 { font-size: 50px; }
.modal-box > p:not(.eyebrow) { color: var(--grey); }

/* FAKE GAME */
.fake-game { margin-top: 30px; border: 1px solid var(--border); padding: 20px; }
.game-score { color: var(--yellow); font-size: 12px; font-weight: 900; }
.game-stage { height: 250px; margin: 15px 0; position: relative; overflow: hidden; background: linear-gradient(90deg, transparent 49%, rgba(255,212,0,0.08) 50%, transparent 51%); border: 1px solid var(--border); }
.player, .target { width: 35px; height: 35px; position: absolute; }
.player { left: 30px; bottom: 30px; background: var(--yellow); }
.target { right: 40px; top: 50px; background: var(--white); }

/* RESPONSIVE */
@media (max-width: 1100px) {
    nav { display: none; }
    .mobile-menu { display: block; }
    .nav-button { display: none; }
    .game-layout { grid-template-columns: 1fr; }
    .game-panel.large { grid-row: auto; min-height: 400px; }
    .feature-grid, .games-grid, .creator-grid, .news-grid { grid-template-columns: repeat(2,1fr); }
    .community-box { flex-direction: column; align-items: flex-start; }
}
@media (max-width: 700px) {
    .container { width: min(100% - 28px, 1180px); }
    .section { padding: 80px 0; }
    .hero h1 { font-size: clamp(55px,18vw,100px); letter-spacing: -4px; }
    .hero-text { font-size: 16px; }
    .hero-stats { grid-template-columns: repeat(2,1fr); }
    .hero-stats div:nth-child(2) { border-right: 0; }
    .feature-grid, .games-grid, .creator-grid, .news-grid { grid-template-columns: 1fr; }
    .split-heading { display: block; }
    .split-heading > p { margin-top: 20px; }
    .community-box { padding: 35px 25px; }
    .event { grid-template-columns: 1fr; gap: 12px; }
    .leader-row { grid-template-columns: 55px 1fr 70px 90px; padding: 18px 12px; font-size: 11px; }
    .footer-grid { grid-template-columns: 1fr 1fr; }
    .footer-bottom .container { padding: 18px 0; flex-direction: column; align-items: flex-start; gap: 5px; }
    .modal-box { padding: 25px; }
    .modal-box h2 { font-size: 38px; }
}
