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

## Implementing semantic HTML elements

    <div class="content">
        <div class="search-engine-optimization">
            <img src="./assets/images/search-engine-optimization.jpg" class="float-left" />
            <h2>Search Engine Optimization</h2>
            <p>
                The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
            </p>
        </div>
        <div id="online-reputation-management" class="online-reputation-management">
            <img src="./assets/images/online-reputation-management.jpg" class="float-right" />
            <h2>Online Reputation Management</h2>
            <p>
                The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
            </p>
        </div>
        <div id="social-media-marketing" class="social-media-marketing">
            <img src="./assets/images/social-media-marketing.jpg" class="float-left" />
            <h2>Social Media Marketing</h2>
            <p>
                Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.
            </p>
        </div>
    </div>






