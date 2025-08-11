---
layout: default
title: About Us
permalink: /about/
---

<div class="container">
    <div class="about-page">
        <h1 class="page-title">About The Froggy Family 🐸</h1>

        <div class="about-hero">
            <img src="{{ '/assets/images/family.png' | relative_url }}" alt="The Froggy Family" class="about-image">
            <div class="about-intro">
                <p>Welcome to our lily pad! We're a family of four frogs who love to create, learn, and share our adventures with the world. Each of us brings something special to our pond.</p>
            </div>
        </div>

        <div class="family-stories">
            <div class="member-story">
                <div class="member-header">
                    <span class="member-icon">🐸</span>
                    <h2>Daddy Frog</h2>
                </div>
                <p>The wise frog of the family, Daddy Frog loves to code and create amazing things. He teaches Smart Frog about programming and helps Baby Robot Frog with technical projects. When he's not coding, you can find him telling stories about the old pond days or working on the next family project.</p>
            </div>

            <div class="member-story">
                <div class="member-header">
                    <span class="member-icon">🌸</span>
                    <h2>Mommy Frog</h2>
                </div>
                <p>The heart of our lily pad, Mommy Frog keeps everything organized and running smoothly. She has a magical way of turning our crazy ideas into beautiful realities. Her creativity and care make every project special, and she always knows how to add that perfect finishing touch.</p>
            </div>

            <div class="member-story">
                <div class="member-header">
                    <span class="member-icon">🎓</span>
                    <h2>Smart Frog</h2>
                </div>
                <p>Our clever young frog is always eager to learn something new. Whether it's solving puzzles, building with blocks, or learning to code, Smart Frog approaches everything with curiosity and enthusiasm. Every day is a new adventure and a chance to discover something amazing!</p>
            </div>

            <div class="member-story">
                <div class="member-header">
                    <span class="member-icon">🤖</span>
                    <h2>Baby Robot Frog</h2>
                </div>
                <p>The newest addition to our family, Baby Robot Frog is a tech-savvy little one with circuits and charm. Part frog, part robot, all adorable! Baby Robot Frog loves blinking lights, beeping sounds, and learning about the world through sensors and code.</p>
            </div>
        </div>

        <div class="our-mission">
            <h2>Our Mission</h2>
            <div class="mission-content">
                <p>At The Froggy House, we believe in:</p>
                <ul>
                    <li>🌟 <strong>Learning Together</strong> - Every project is a chance to grow</li>
                    <li>💚 <strong>Family First</strong> - Making memories while making things</li>
                    <li>🎨 <strong>Creativity</strong> - Letting imagination guide our projects</li>
                    <li>🤝 <strong>Sharing</strong> - Inspiring others with our journey</li>
                    <li>🎉 <strong>Fun</strong> - If it's not fun, why do it?</li>
                </ul>
            </div>
        </div>

        <div class="what-we-do">
            <h2>What We Create</h2>
            <div class="activities-grid">
                <div class="activity-card">
                    <span class="activity-icon">💻</span>
                    <h3>Coding Projects</h3>
                    <p>From simple scripts to complex applications, we love to code together.</p>
                </div>
                <div class="activity-card">
                    <span class="activity-icon">🎨</span>
                    <h3>Art & Crafts</h3>
                    <p>Creative projects that combine technology with traditional crafts.</p>
                </div>
                <div class="activity-card">
                    <span class="activity-icon">🤖</span>
                    <h3>Robotics</h3>
                    <p>Building and programming robots that hop, swim, and explore.</p>
                </div>
                <div class="activity-card">
                    <span class="activity-icon">📚</span>
                    <h3>Learning Adventures</h3>
                    <p>Documenting our educational journey and discoveries.</p>
                </div>
            </div>
        </div>

        <div class="join-us">
            <h2>Join Our Journey</h2>
            <p>We're always excited to connect with other families, creators, and curious minds. Feel free to explore our projects, try our tutorials, and share your own creations inspired by our work!</p>
            <p>Remember: In our pond, every frog has something special to contribute, and that includes you! 🐸💚</p>
        </div>
    </div>
</div>

<style>
.about-page {
    max-width: 900px;
    margin: 0 auto;
    padding: 3rem 0;
}

.page-title {
    color: var(--dark-green);
    text-align: center;
    margin-bottom: 2rem;
    font-size: 2.5rem;
}

.about-hero {
    background: white;
    border-radius: var(--border-radius);
    padding: 2rem;
    box-shadow: 0 5px 15px var(--shadow);
    margin-bottom: 3rem;
    text-align: center;
}

.about-image {
    max-width: 100%;
    height: auto;
    border-radius: var(--border-radius);
    margin-bottom: 2rem;
}

.about-intro {
    font-size: 1.2rem;
    color: var(--text-dark);
    line-height: 1.8;
}

.family-stories {
    display: grid;
    gap: 2rem;
    margin-bottom: 3rem;
}

.member-story {
    background: white;
    padding: 2rem;
    border-radius: var(--border-radius);
    box-shadow: 0 5px 15px var(--shadow);
    position: relative;
    overflow: hidden;
}

.member-story::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 5px;
    background: linear-gradient(90deg, var(--primary-green), var(--pond-blue), var(--lily-pink));
}

.member-header {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 1rem;
}

.member-icon {
    font-size: 2.5rem;
}

.member-story h2 {
    color: var(--dark-green);
    margin: 0;
}

.member-story p {
    color: var(--text-dark);
    line-height: 1.8;
}

.our-mission {
    background: linear-gradient(135deg, #E8F5E9, #F1F8E9);
    padding: 2rem;
    border-radius: var(--border-radius);
    margin-bottom: 3rem;
}

.our-mission h2 {
    color: var(--dark-green);
    text-align: center;
    margin-bottom: 1.5rem;
}

.mission-content ul {
    list-style: none;
    padding: 0;
}

.mission-content li {
    padding: 0.75rem 0;
    font-size: 1.1rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.what-we-do {
    margin-bottom: 3rem;
}

.what-we-do h2 {
    color: var(--dark-green);
    text-align: center;
    margin-bottom: 2rem;
}

.activities-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1.5rem;
}

.activity-card {
    background: white;
    padding: 1.5rem;
    border-radius: var(--border-radius);
    box-shadow: 0 5px 15px var(--shadow);
    text-align: center;
    transition: transform 0.3s ease;
}

.activity-card:hover {
    transform: translateY(-5px);
}

.activity-icon {
    font-size: 2.5rem;
    display: block;
    margin-bottom: 1rem;
}

.activity-card h3 {
    color: var(--primary-green);
    margin-bottom: 0.5rem;
}

.activity-card p {
    color: var(--text-dark);
    font-size: 0.95rem;
}

.join-us {
    background: white;
    padding: 2rem;
    border-radius: var(--border-radius);
    box-shadow: 0 5px 15px var(--shadow);
    text-align: center;
}

.join-us h2 {
    color: var(--dark-green);
    margin-bottom: 1rem;
}

.join-us p {
    color: var(--text-dark);
    line-height: 1.8;
    font-size: 1.1rem;
    margin-bottom: 1rem;
}
</style>
