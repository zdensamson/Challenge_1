# Horseoin code refactor

## Description 

The hypothetical marketing agency _Horiseon_ requested a code refactor for their landing page. 

My task as the front-end developer was to update the existing code base to follow accessibility standards so that the website is both **accessible** and **optimized for search engines**.

In order to accomplish this goal (and impress the _client_) I implemented the following steps: 
1. Reviewed the index.HTML file in both VScode & Chrome Dev Tools to ensure all links functioned properly
2. Replaced non-semantic elements with semantic elements in HTML
3. Provided every `<img>` tag with an `alt` attribute 
4. Provided a concise & descriptive `title` to the `<head>` tag
5. Consolidated the CSS rules to make the stylesheet more efficient 

In order to both consolidate the description of my work and highlight what I found to be "most important"-- I will only be providing exapmples from steps __#2__ & __#5__.

**The final refactored site can be found here:** https://zdensamson.github.io/Code-Refactor-Horiseon/

## Implementing semantic HTML elements

The existing site "functioned" properly with non-semantic elements, but the following exapmles demonstrate the edits I provided for both **accessibility** & **SEO**.

### Header edits
**Before the refactor**-- the starting index.HTML did not have a semantically titled header nor any idication that the nested `<a>` tags contained navigation links referencing content within the page.

    <div class="header">
        <h1>Hori<span class="seo">seo</span>n</h1>
        <div>
            <ul>
                <li>
                    <a></a>
                </li>
            </ul>
        </div>
    </div>

**Header after** code refactor:

    <header class="header">
        <h1>Hori<span class="seo">seo</span>n</h1>
        <nav>
            <ul>
                <li>
                    <a></a>
                </li>
            </ul>
        </nav>
    </header>

### Main body edits
**Before the refactor** the "content/services" section implemented a parent `<div>` that contained three related nested `<div>`'s. The three child `<div>`'s were all services that _Horiseon_ offered and their relation to one another called for their parent to be changed to a `<section>` tag. The three child `<div>`'s each contained a unique header, image, and descriprtion that related to one another making each a standalone element-- for this reason I changed the three child `<div>`'s to `<article>`'s.

    <div class="content">
        <div class="search-engine-optimization">
            <img src="./assets/images/search-engine-optimization.jpg" class="float-left" />
            <h2>Search Engine Optimization</h2>
            <p>
            </p>
        </div>
        <div id="online-reputation-management" class="online-reputation-management">
            <img src="./assets/images/online-reputation-management.jpg" class="float-right" />
            <h2>Online Reputation Management</h2>
            <p>
            </p>
        </div>
        <div id="social-media-marketing" class="social-media-marketing">
            <img src="./assets/images/social-media-marketing.jpg" class="float-left" />
            <h2>Social Media Marketing</h2>
            <p>
            </p>
        </div>
    </div>

**Main body after** the refactor:

    <section class="content">
        <article class="search-engine-optimization">
            <img src="./assets/images/search-engine-optimization.jpg" class="float-left" />
            <h2>Search Engine Optimization</h2>
            <p>
            </p>
        </article>
        <article id="online-reputation-management" class="online-reputation-management">
            <img src="./assets/images/online-reputation-management.jpg" class="float-right" />
            <h2>Online Reputation Management</h2>
            <p>
            </p>
        </article>
        <article id="social-media-marketing" class="social-media-marketing">
            <img src="./assets/images/social-media-marketing.jpg" class="float-left" />
            <h2>Social Media Marketing</h2>
            <p>
            </p>
        </article>
    </section>
    
## Consolidating CSS stylesheet
