# RND Recruitment Task

### Technologies to be used
- TypeScript
- React 16 or later
- Node.js 16 or later
- SASS or Styled Components


### General Criteria
- Layout should be responsible
- Highest possible PageSpeed Insights Scores
- Provide documentation how to run the project locally
- DRY and KISS
- Write tests with Jest
- Validate the data you receive from the backend / catch errors if data is wrongly formatted
- SEO Metadata should be set (even if you are using CSR)
- Navigation should be implemented via BrowserRouter (no "hash links").

### Nice to have
- Storybook
- deploy your page (and storybook)
- Integrate GitHub Actions (e.g. linting, testing, deploying)
- Next.js (you don't have to learn it for this task, if you've never used it!)


### Overall Layout

Each page should have a header with the name of the tenant. You can choose that name completely free for this task (doesn't even need to be a real tenant).
The Header should have a different color than the page background, which should be white.
Additionally, each page should have a footer containing the topics you fetched from the topics.json (this should be dynamically loaded).
The footer should always stick to the bottom, even if the page content is not high enough.

### Landing Page

The landing page should inherit the overall layout. Also, below the header a horizontal (scrollable) bar should be rendered containing the topics (`data/topics.json`). 
These do not need to be clickable. Since this data can change, it should be fetched dynamically on page load.
Below the header you should show the teasers. These should also be fetched dynamically from the backend (`data/teaser.json`).

Make sure to show all relevant data in a teaser (e.g. title, hero, published date...).
A click on the whole teaser should link to the article page.

### Article Page

The article page renders an article. It inherits the overall layout.
Make sure that the URL contains the Article Id. You can fetch the article from `data/articles/<id>.json`.

The article's json file provides you with all information needed. If you need inspiration for a layout head over to [one of our pages](https://www.rnd.de/politik/tv-triell-baerbock-laschet-und-scholz-zu-klima-steuer-corona-und-moegliche-koalitionen-BXBPJNRAZYLGC3JLQO4YKM46RY.html).

The most important part here is the `content`-Array. It provides you with everything you need to render an article.
For this task there are four types:

|type|what it does|
|:-----:|:------:|
|plaintext|A simple text which you can just render. One Plaintext items equals one paragraph. The `content`-Attribute provides you with the text.|
|image|Images contain `src`, `alt` and `copyright` attributes which you'll need to render the image. Make sure to also show the copyright, as it's important!|
|headline|Headlines contain a `level` and the `content`. The level specifies which h-tag you should use. Content is the text.|
