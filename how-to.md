---
layout: default
title: How to Add Content
permalink: /how-to/
---

<div class="container">
    <div class="documentation">
        <h1 class="page-title">🐸 How to Add and Publish Content</h1>

        <p class="intro">Welcome to our content publishing guide! This page will teach you how to add your own projects, stories, and memories to The Froggy House.</p>

        <div class="doc-section">
            <h2>📝 Creating a New Post</h2>
            
            <h3>Step 1: Create a New File</h3>
            <p>Posts go in the <code>_posts</code> folder with a specific naming format:</p>
            <pre><code>YYYY-MM-DD-your-post-title.md</code></pre>
            <p>Example: <code>2024-01-15-our-first-robot.md</code></p>

            <h3>Step 2: Add Front Matter</h3>
            <p>Every post starts with front matter (metadata). Copy this template:</p>
            <pre><code>---
layout: post
title: "Your Amazing Title Here"
date: 2024-01-15
categories: [Project]
tags: [coding, fun, family]
author: "Smart Frog"
author_emoji: "🎓"
---</code></pre>

            <h3>Step 3: Write Your Content</h3>
            <p>After the front matter, write your post using Markdown:</p>
            <pre><code># This is a heading

This is a paragraph.

## This is a smaller heading

- This is a bullet point
- Another bullet point

**This is bold text**
*This is italic text*

![Image description](/assets/images/your-image.jpg)</code></pre>

            <h3>Step 4: Add Images</h3>
            <p>Place images in <code>assets/images/</code> and reference them like this:</p>
            <pre><code>![Our robot project](/assets/images/robot-project.jpg)</code></pre>
        </div>

        <div class="doc-section">
            <h2>🎨 Creating a Project Page</h2>
            
            <p>For bigger projects, create a file in the <code>_projects</code> folder:</p>
            
            <h3>Example: <code>_projects/robot-frog.md</code></h3>
            <pre><code>---

layout: project
title: "Building Baby Robot Frog"
date: 2024-01-15
featured_image: /assets/images/robot-frog.jpg
technologies: [Arduino, LEDs, Love]
collaborators: ["Daddy Frog", "Smart Frog"]
---

Project description goes here...</code></pre>
        </div>

        <div class="doc-section">
            <h2>📸 Adding Family Moments</h2>
            
            <p>Special memories go in the <code>_family_moments</code> folder:</p>
            
            <pre><code>---

layout: moment
title: "First Day of Frog School"
date: 2024-01-10
photo: /assets/images/first-day.jpg
family_members: ["Smart Frog", "Mommy Frog"]
---

Memory description...</code></pre>
        </div>

        <div class="doc-section">
            <h2>🚀 Publishing Your Content</h2>
            
            <h3>Option 1: Using GitHub Web Interface</h3>
            <ol>
                <li>Go to your repository on GitHub</li>
                <li>Navigate to the correct folder (_posts, _projects, etc.)</li>
                <li>Click "Add file" → "Create new file"</li>
                <li>Name your file and add content</li>
                <li>Click "Commit new file"</li>
                <li>GitHub Pages will automatically build and publish!</li>
            </ol>

            <h3>Option 2: Using Git Command Line</h3>
            <pre><code># Clone the repository
git clone <https://github.com/froggy-house/froggy-house.github.io.git>

# Create your post

cd froggy-house.github.io/_posts
nano 2024-01-15-my-post.md

# Add and commit

git add .
git commit -m "Add new post about our robot project"

# Push to GitHub

git push origin main</code></pre>

            <h3>Option 3: Using GitHub Desktop</h3>
            <ol>
                <li>Clone the repository using GitHub Desktop</li>
                <li>Create your files locally</li>
                <li>Commit changes with a descriptive message</li>
                <li>Push to origin</li>
            </ol>
        </div>

        <div class="doc-section">
            <h2>🧪 Testing Locally</h2>
            
            <p>To preview your changes before publishing:</p>
            
            <pre><code># Install Jekyll (one time)
gem install bundler jekyll

# Install dependencies

bundle install

# Run local server

bundle exec jekyll serve

# Visit <http://localhost:4000> in your browser</code></pre>

        </div>

        <div class="doc-section">
            <h2>💡 Tips for Great Content</h2>
            
            <ul class="tips-list">
                <li><strong>Use descriptive titles:</strong> Make them fun and froggy!</li>
                <li><strong>Add images:</strong> Pictures make posts more engaging</li>
                <li><strong>Tag appropriately:</strong> Help others find related content</li>
                <li><strong>Write for the family:</strong> Keep it friendly and accessible</li>
                <li><strong>Document the process:</strong> Share how you made things, not just the result</li>
                <li><strong>Include everyone:</strong> Mention who helped or participated</li>
            </ul>
        </div>

        <div class="doc-section">
            <h2>📚 Markdown Quick Reference</h2>
            
            <table class="markdown-reference">
                <thead>
                    <tr>
                        <th>Element</th>
                        <th>Markdown Syntax</th>
                        <th>Result</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Heading 1</td>
                        <td><code># Heading</code></td>
                        <td><h1 style="font-size: 1.5rem;">Heading</h1></td>
                    </tr>
                    <tr>
                        <td>Heading 2</td>
                        <td><code>## Heading</code></td>
                        <td><h2 style="font-size: 1.3rem;">Heading</h2></td>
                    </tr>
                    <tr>
                        <td>Bold</td>
                        <td><code>**bold text**</code></td>
                        <td><strong>bold text</strong></td>
                    </tr>
                    <tr>
                        <td>Italic</td>
                        <td><code>*italic text*</code></td>
                        <td><em>italic text</em></td>
                    </tr>
                    <tr>
                        <td>Link</td>
                        <td><code>[text](url)</code></td>
                        <td><a href="#">text</a></td>
                    </tr>
                    <tr>
                        <td>Image</td>
                        <td><code>![alt](url)</code></td>
                        <td>🖼️ Image</td>
                    </tr>
                    <tr>
                        <td>Code</td>
                        <td><code>`code`</code></td>
                        <td><code>code</code></td>
                    </tr>
                    <tr>
                        <td>List</td>
                        <td><code>- Item</code></td>
                        <td>• Item</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <div class="doc-section">
            <h2>🆘 Need Help?</h2>
            
            <p>If you get stuck:</p>
            <ul>
                <li>Check the <a href="https://jekyllrb.com/docs/">Jekyll Documentation</a></li>
                <li>Look at existing posts for examples</li>
                <li>Ask another family member for help!</li>
                <li>Remember: mistakes are how we learn 🐸</li>
            </ul>
        </div>
    </div>
</div>

<style>
.documentation {
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

.intro {
    font-size: 1.2rem;
    text-align: center;
    color: var(--text-dark);
    margin-bottom: 3rem;
    padding: 1.5rem;
    background: white;
    border-radius: var(--border-radius);
    box-shadow: 0 5px 15px var(--shadow);
}

.doc-section {
    background: white;
    padding: 2rem;
    margin-bottom: 2rem;
    border-radius: var(--border-radius);
    box-shadow: 0 5px 15px var(--shadow);
}

.doc-section h2 {
    color: var(--dark-green);
    margin-bottom: 1.5rem;
    padding-bottom: 0.5rem;
    border-bottom: 3px solid var(--light-green);
}

.doc-section h3 {
    color: var(--primary-green);
    margin: 1.5rem 0 1rem;
}

.doc-section pre {
    background: #f8f9fa;
    border: 1px solid #dee2e6;
    border-radius: 8px;
    padding: 1rem;
    overflow-x: auto;
    margin: 1rem 0;
}

.doc-section code {
    background: #f8f9fa;
    padding: 0.2rem 0.5rem;
    border-radius: 4px;
    font-family: 'Courier New', monospace;
    color: var(--dark-green);
}

.doc-section pre code {
    background: none;
    padding: 0;
}

.doc-section ol, .doc-section ul {
    margin: 1rem 0;
    padding-left: 2rem;
}

.doc-section li {
    margin: 0.5rem 0;
    line-height: 1.6;
}

.tips-list {
    background: linear-gradient(135deg, #E8F5E9, #F1F8E9);
    padding: 1.5rem 2rem;
    border-radius: var(--border-radius);
    list-style: none;
}

.tips-list li {
    position: relative;
    padding-left: 1.5rem;
    margin: 0.75rem 0;
}

.tips-list li::before {
    content: "💡";
    position: absolute;
    left: 0;
}

.markdown-reference {
    width: 100%;
    border-collapse: collapse;
    margin: 1rem 0;
}

.markdown-reference th {
    background: var(--primary-green);
    color: white;
    padding: 0.75rem;
    text-align: left;
}

.markdown-reference td {
    padding: 0.75rem;
    border-bottom: 1px solid #dee2e6;
}

.markdown-reference tr:hover {
    background: #f8f9fa;
}
</style>
