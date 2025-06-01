---
layout: default
title: Home
---
<div class="parallax-section grid items-center justify-center h-screen" id="section1">
    <div>
        <h1 class="typed text-6xl">Oh yeah, it's all coming together.</h1>
        <div class="bottom-left">
            <h1 class="text-4xl">Daniel Giebink</h1>
            <p class="text-2xl">Sr Security Architect, Full-stack Developer & Cybersecurity Pro</p>
        </div>
    </div>
</div>
<div class="grid flex items-center justify-center h-screen section-light" id="about">
    <div class="background-text">About</div>
    <div class="w-full">
    <p>Hey, I'm Daniel! 👋</p>
    <br/>
    <p>I love to design, build, grow, and create.</p>
    <p>I am a creative and energetic full-stack developer with a solid background in React, Node.js, Python, AWS, and Azure. Experienced in designing and implementing cutting-edge web apps, cloud solutions, and secure systems. Also a cybersecurity ace with a history as an analyst, SIEM engineer, trainer, speaker, penetration tester, and solutions architect at a leading managed security services provider. Passionate about blending technology, security, and storytelling to deliver user-friendly, resilient systems.</p>
    <p>I think great communication, collaboration, sharing and storyteling are paramount to the success of any endeavor.</p>
    <br/>
    <p>I feel like we could make something great together!</p>
    <p>Interested?</p>  
    </div>
    <!-- </div> -->
</div>
<div class="parallax-section grid items-center justify-center h-screen section-dark" id="skills">
    <div class="background-text">Skills</div>
    <div class="">
        <p>Curious by nature, skilled by discipline.</p>
        <br/>
        <div class="prose flex">
            <div class="w-1/3">
                <h2>Architecture</h2>
            </div>
            <div class="w-1/3">
                <h2>Programming Languages & Frameworks</h2>
                <ul>
                    <li>React</li>
                    <li>Node.js</li>
                    <li>JavaScript</li>
                    <li>Express.js</li>
                    <li>PHP</li>
                    <li>Python</li>
                    <li>and more...</li>
                </ul>
            </div>
            <div class="w-1/3">
                <h2>Data Engineering</h2>
                <ul>
                    <li>PowerBI</li>
                    <li>Fabric</li>
                </ul>
            </div>
        </div>
    </div>
</div>
<div class="section grid items-center justify-center h-screen section-light" id="experience">
    <div class="background-text">Experience</div>
    <h2>The best yet? Where I’ve made an impact so far</h2>
</div>
<div class="parallax-section grid items-center justify-center h-screen section-dark" id="projects">
    <div class="background-text">Projects</div>
    <div class="prose columns-3">
            <div>
                <h2>Architecture</h2>
            </div>
            <div>
                <h2>Development</h2>
            </div>
            <div>
                <h2>Data Engineering</h2>
            </div>
        </div>
</div>
<div class="parallax-section grid items-center justify-center h-screen section-light" id="contact">
    <div class="background-text">Contact</div>
    <div class="content">
        <h2>Contact</h2>
        <p>Your contact details...</p>
    </div>
</div>

<style>
    .floating-link {
        position: fixed;
        bottom: 20px;
        right: 20px;
        width: 60px;
        height: 60px;
        background-color: #333;
        color: #fff;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        text-decoration: none;
        z-index: 1000;
        transition: background-color 0.3s ease;
    }

    .floating-link:hover {
        background-color: #555;
    }

    .floating-link svg {
        width: 24px;
        height: 24px;
    }
</style>

<a href="/terminal" target="_blank" class="floating-link" aria-label="Open Terminal">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="4 17 10 11 4 5"></polyline>
        <line x1="12" y1="19" x2="20" y2="19"></line>
    </svg>
</a>
