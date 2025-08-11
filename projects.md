---
layout: default
title: Projects
permalink: /projects/
---

<div class="container">
    <div class="projects-page">
        <h1 class="page-title">Our Family Projects 🛠️</h1>
        <p class="page-intro">Explore the amazing things we've built together!</p>

        <div class="projects-grid">
            {% for project in site.projects %}
            <div class="project-card">
                {% if project.featured_image %}
                <div class="project-image">
                    <img src="{{ project.featured_image | relative_url }}" alt="{{ project.title }}">
                </div>
                {% endif %}
                <div class="project-content">
                    <h2>{{ project.title }}</h2>
                    <div class="project-meta">
                        <span class="project-date">{{ project.date | date: "%B %Y" }}</span>
                        {% if project.collaborators %}
                        <span class="project-collaborators">
                            👥 {{ project.collaborators | join: ", " }}
                        </span>
                        {% endif %}
                    </div>
                    <p>{{ project.excerpt | strip_html | truncate: 150 }}</p>
                    {% if project.technologies %}
                    <div class="project-tech">
                        {% for tech in project.technologies %}
                        <span class="tech-tag">{{ tech }}</span>
                        {% endfor %}
                    </div>
                    {% endif %}
                    <a href="{{ project.url | relative_url }}" class="project-link">View Project →</a>
                </div>
            </div>
            {% endfor %}
        </div>

        {% if site.projects.size == 0 %}
        <div class="empty-state">
            <span class="empty-icon">📦</span>
            <h2>No projects yet!</h2>
            <p>We're working on some amazing things. Check back soon!</p>
            <a href="{{ '/how-to' | relative_url }}" class="btn">Learn how to add projects</a>
        </div>
        {% endif %}
    </div>
</div>

<style>
.projects-page {
    padding: 3rem 0;
}

.page-intro {
    text-align: center;
    font-size: 1.2rem;
    color: var(--text-dark);
    margin-bottom: 3rem;
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
    gap: 2rem;
    margin-bottom: 3rem;
}

.project-card {
    background: white;
    border-radius: var(--border-radius);
    overflow: hidden;
    box-shadow: 0 5px 15px var(--shadow);
    transition: transform 0.3s ease;
}

.project-card:hover {
    transform: translateY(-5px);
}

.project-image {
    height: 200px;
    overflow: hidden;
    background: linear-gradient(135deg, var(--light-green), var(--pond-blue));
}

.project-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.project-content {
    padding: 1.5rem;
}

.project-content h2 {
    color: var(--dark-green);
    margin-bottom: 0.5rem;
}

.project-meta {
    display: flex;
    gap: 1rem;
    margin-bottom: 1rem;
    font-size: 0.9rem;
    color: #666;
}

.project-tech {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin: 1rem 0;
}

.tech-tag {
    background: var(--light-green);
    color: var(--dark-green);
    padding: 0.25rem 0.75rem;
    border-radius: 15px;
    font-size: 0.85rem;
}

.project-link {
    display: inline-block;
    color: var(--primary-green);
    text-decoration: none;
    font-weight: 600;
    margin-top: 1rem;
    transition: color 0.3s ease;
}

.project-link:hover {
    color: var(--dark-green);
}

.empty-state {
    text-align: center;
    padding: 4rem 2rem;
    background: white;
    border-radius: var(--border-radius);
    box-shadow: 0 5px 15px var(--shadow);
}

.empty-icon {
    font-size: 4rem;
    display: block;
    margin-bottom: 1rem;
}

.empty-state h2 {
    color: var(--dark-green);
    margin-bottom: 0.5rem;
}

.empty-state p {
    color: var(--text-dark);
    margin-bottom: 2rem;
}

.btn {
    display: inline-block;
    padding: 0.75rem 2rem;
    background: var(--primary-green);
    color: white;
    text-decoration: none;
    border-radius: 25px;
    transition: background 0.3s ease;
}

.btn:hover {
    background: var(--dark-green);
}
</style>
