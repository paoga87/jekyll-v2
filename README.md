# README
## jekyll-v2 Repository
This codebase uses [Jekyll](https://jekyllrb.com/) to write up the markup of the site content, then renders the static HTML content to the `_site` directory. The theme used is called [Personal by Jekyll Themes](https://jekyllthemes.io/theme/personal-website-jekyll-theme).

**Please note:** in order to use the Personal Theme, you need to purchase a license.

This is the main code used for my personal website at https://paolagarcia.com. It is also setup to detect merges to the `master` branch and automatically deploy to serve the `github-pages` environment at https://paoga87.github.io/jekyll-v2/.

---

## Getting started
Copy this theme files to a directory.

To run the theme locally, navigate to the theme directory in your terminal and run `bundle install` to install the theme's dependencies. Then run `bundle exec jekyll serve` to start the Jekyll server. Once you have tested locally and are satisfied with the changes, you need to prepare the pages for production, so you would want to run `bundle exec jekyll build` to get rid of any `localhost` instances replaced in `{{ site.url }}` when working locally.
## Jekyll basics

If you're not familiar with how Jekyll works, check out [jekyllrb.com](https://jekyllrb.com/) for all the details, or read up on just the basics of [front matter](https://jekyllrb.com/docs/frontmatter/), [writing posts](https://jekyllrb.com/docs/posts/), and [creating pages](https://jekyllrb.com/docs/pages/).

