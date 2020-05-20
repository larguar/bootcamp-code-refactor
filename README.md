# Code Refactor

One of the most common tasks for front-end and junior developers is to take existing code and refactor it to either meet a certain set of standards or implement a new technology. Web accessibility is an increasingly important consideration for businesses, ensuring that people with disabilities or socio-economic restrictions have access to their website, and helping them avoid litigation.

Horiseon, a fictional marketing and SEO agency wanted a codebase that follows accessibility standards so that their own site is optimized for search engines.

To do this, I've made the following updates:



## Page Title
```
WHEN I view the title element
THEN I find a concise, descriptive title
```
Providing unique, concise HTML page titles helps users with disabilities quickly understand a web page’s content and purpose. Well-written page titles are critical to users with visual disabilities because they are always the first page element announced by screen-reading software.

These measures allow users with visual disabilities to quickly determine if they are interested in a page’s content. They also provide a descriptive name for bookmarking the page, which doubles as an accurate description for search results.



## Logical Structure
```
WHEN I view the structure of the HTML elements
THEN I find that the elements follow a logical structure independent of styling and positioning
```
Well-structured content allows more efficient navigation and processing. Use HTML and WAI-ARIA to improve navigation and orientation on web pages and in applications. Mark up different regions of web pages and applications, so that they can be identified by web browsers and assistive technologies.

Pages with well-structured content are essential for many web users, for example:

1.   People with cognitive and learning disabilities can more easily find and prioritize content on the page.

2.   People using screen readers can skip to the main content directly and navigate to sections that are important to them.

3.   Keyboard users can browse pages and their sections more efficiently. Otherwise, users have to press the tab key multiple times to navigate through all links in each section.

4.   People using software that only shows the main content of a web page, such as people with cognitive disabilities, will receive better results if the page structure is correctly marked up.

5.   People with visual impairments, including people with low vision, have cues that provide orientation on the page and in the content.

6.   Mobile web users often have access to a so-called “reader” or “reading” mode that will only show the main content of the page if it is correctly marked up.

7.   People using certain browser plugins can use landmark roles to jump to specific sections on a page.

8.   Search engines can use the data to better index the content of a page.



## Semantic Elements
```
WHEN I view the source code
THEN I find semantic HTML elements
```
Semantic elements clearly describe the meaning to both the browser and the developer. Mark up website content semantically, so that the website is extensible. Valid semantics create content that is reusable and more meaningful to assistive technologies.

Examples of semantic elements include:
```
<form>
<table>
<article>
<aside>
<details>
<figcaption>
<figure>
<footer>
<header>
<main>
<mark>
<nav>
<section>
<summary>
<time>
```
Most current web browsers support the above HTML5 elements and convey the information to assistive technology through the accessibility APIs. However, to maximize compatibility with web browsers and assistive technologies that support WAI-ARIA but do not yet support HTML5, it is currently advisable to use both the HTML5 elements and the corresponding WAI-ARIA roles.

Examples of this include:
```
<header role="banner">…</header>
<main role="main">…</main>
<nav role="navigation">…</nav>
<footer role="contentinfo">…</footer>
```
 
 
## Heading Tags
```
WHEN I view the heading attributes
THEN they fall in sequential order
```
Headings communicate the organization of the content on the page. Web browsers, plug-ins, and assistive technologies can use them to provide in-page navigation.

Nest headings by their rank (or level). The most important heading has the rank 1 (H1), the least important heading rank 6 (H6). Headings with an equal or higher rank start a new section, headings with a lower rank start new subsections that are part of the higher ranked section.

Skipping heading ranks can be confusing and should be avoided where possible: Make sure that an H2 is not followed directly by an H4, for example. It is ok to skip ranks when closing subsections, for instance, a H2 beginning a new section, can follow an H4 as it closes the previous section.



## Alt Tags
```
WHEN I view the image elements
THEN I find accessible alt attributes
```
The required alt attribute specifies an alternate text for an image, if the image cannot be displayed. The alt attribute provides alternative information for an image if a user for some reason cannot view it due to slow connection, an error in the src attribute, or if the user uses a screen reader.
