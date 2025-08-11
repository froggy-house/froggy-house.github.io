---
layout: default
title: Family Moments
permalink: /moments/
---

<div class="container">
    <div class="moments-page">
        <h1 class="page-title">Family Moments 📸</h1>
        <p class="page-intro">Precious memories from our froggy adventures!</p>

        <div class="moments-grid">
            {% for moment in site.family_moments %}
            <div class="moment-card">
                {% if moment.photo %}
                <div class="moment-photo">
                    <img src="{{ moment.photo | relative_url }}" alt="{{ moment.title }}">
                </div>
                {% endif %}
                <div class="moment-content">
                    <h3>{{ moment.title }}</h3>
                    <div class="moment-date">{{ moment.date | date: "%B %d, %Y" }}</div>
                    {% if moment.family_members %}
                    <div class="moment-members">
                        {% for member in moment.family_members %}
                        <span class="member-tag">{{ member }}</span>
                        {% endfor %}
                    </div>
                    {% endif %}
                    <p>{{ moment.excerpt | strip_html | truncate: 100 }}</p>
                    <a href="{{ moment.url | relative_url }}" class="moment-link">View Memory →</a>
                </div>
            </div>
            {% endfor %}
        </div>

        {% if site.family_moments.size == 0 %}
        <div class="empty-state">
            <span class="empty-icon">📷</span>
            <h2>No moments captured yet!</h2>
            <p>Start documenting your family memories today!</p>
            <a href="{{ '/how-to' | relative_url }}" class="btn">Learn how to add moments</a>
        </div>
        {% endif %}
    </div>
</div>

<style>
.moments-page {
    padding: 3rem 0;
}

.moments-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.5rem;
    margin-bottom: 3rem;
}

.moment-card {
    background: white;
    border-radius: var(--border-radius);
    overflow: hidden;
    box-shadow: 0 5px 15px var(--shadow);
    transition: transform 0.3s ease;
}

.moment-card:hover {
    transform: translateY(-5px);
}

.moment-photo {
    height: 200px;
    overflow: hidden;
}

.moment-photo img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.moment-content {
    padding: 1.5rem;
}

.moment-content h3 {
    color: var(--dark-green);
    margin-bottom: 0.5rem;
}

.moment-date {
    color: #666;
    font-size: 0.9rem;
    margin-bottom: 0.5rem;
}

.moment-members {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin: 0.5rem 0;
}

.member-tag {
    background: var(--lily-pink);
    color: white;
    padding: 0.25rem 0.75rem;
    border-radius: 15px;
    font-size: 0.85rem;
}

.moment-link {
    display: inline-block;
    color: var(--primary-green);
    text-decoration: none;
    font-weight: 600;
    margin-top: 0.5rem;
    transition: color 0.3s ease;
}

.moment-link:hover {
    color: var(--dark-green);
}
</style>
