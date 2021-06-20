# Horiseon code refactor

## Description 

The hypothetical marketing agency _Horiseon_ requested a code refactor for their landing page. 

My task as the front-end developer was to update the existing code base to follow accessibility standards so that the website is both **accessible** and **optimized for search engines**.

In order to accomplish this goal (and impress the _client_) I implemented the following steps: 
1. Reviewed the index.HTML file in both VScode & Chrome Dev Tools to ensure all links functioned properly
2. **Replaced non-semantic elements with semantic elements in HTML**
3. Provided every `<img>` tag with an `alt` attribute 
4. Provided a concise & descriptive `title` to the `<head>` tag
5. **Consolidated the CSS rules to make the stylesheet more efficient** 

In order to both consolidate the description of my work and highlight what I found to be "most important"-- I will only be providing exapmples from steps __#2__ & __#5__.

**The final refactored site can be found here:** https://zdensamson.github.io/Code-Refactor-Horiseon/

### Implementing semantic HTML elements

The existing site "functioned" properly with non-semantic elements, but the following exapmles demonstrate the edits I provided for both **accessibility** & **SEO**.

#### Header edits
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

#### Main body edits
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
    
### Consolidating the CSS stylesheet

After reviewing both the CSS rule set-- and the respective HTML elements they styled-- it became clear that the original CSS code was implementing the exact same style to multiple elements utilizing uneccessary unique class selectors that could all be consolidated into a single class. 

For instance when styling the benefit section's `<div>` & `<h3>` elements-- the initial CSS created 6 unique style rules (with 3 unique class selectors) that can condensed into 2 seperate rules (with a single class selector). The first code snippet shows the initial CSS style, and the second code snippet shows where I replaced the `.benefit-lead`, `.benefit-brand`, & `.benefit-cost` classes with a single __`.benefit-description`__ class.

__Before code refactor__

    .benefit-lead {
    margin-bottom: 32px;
    color: #ffffff;
    }

    .benefit-brand {
        margin-bottom: 32px;
        color: #ffffff;
    }

    .benefit-cost {
        margin-bottom: 32px;
        color: #ffffff;
    }

    .benefit-lead h3 {
        margin-bottom: 10px;
        text-align: center;
    }

    .benefit-brand h3 {
        margin-bottom: 10px;
        text-align: center;
    }

    .benefit-cost h3 {
        margin-bottom: 10px;
        text-align: center;
    }
    
__After code refactor__

    .benefit-description {
        margin-bottom: 32px;
        color: #ffffff;
    }
    .benefit-description h3 {
        margin-bottom: 10px;
        text-align: center;
    }
## License 

Copyright (c) 2021 Zachary Dennis Samson

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
