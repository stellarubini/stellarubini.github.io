# stellarubini.github.io

Source code of my personal website: **[stellarubini.github.io](https://stellarubini.github.io)**.

I'm Stella Rubini, a Data Scientist at Intesa Sanpaolo and currently a Visiting Scholar at the Sky Computing Lab, UC Berkeley. The site is a short introduction to who I am, with my publications, projects and talks.

It is a static site built with [Jekyll](https://jekyllrb.com/) on top of the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template, and hosted on GitHub Pages.

## Run it locally

Requirements: Ruby 3.x and Bundler.

```bash
bundle config set --local path vendor/bundle   # keep gems inside the project
bundle install
bundle exec jekyll serve -l -H localhost
```

The site is then available at <http://localhost:4000> and reloads automatically on every change, except for `_config.yml`, which requires restarting the server.

> **macOS note:** if `bundle install` fails while compiling native extensions with `ld: tapi error: malformed file` / `unknown architecture`, the Command Line Tools linker does not support the newest macOS SDK. Point the build to an older SDK, e.g.
> `SDKROOT=/Library/Developer/CommandLineTools/SDKs/MacOSX26.5.sdk bundle install`

As an alternative, the repository includes a `Dockerfile`, `docker-compose.yaml` and a VS Code dev container: `docker compose up` serves the site on the same port.

## Where things live

| What | Where |
|---|---|
| Homepage text | `_pages/about.md` |
| News (homepage) | `_data/news.yml`, most recent first |
| Experience (homepage) | `_data/experience.yml` |
| Publications | `_publications/`, one Markdown file per paper |
| Projects | `_portfolio/` |
| Talks & lectures | `_talks/` |
| Menu | `_data/navigation.yml` |
| Sidebar (bio, links, photo) | `author` section of `_config.yml`, photo in `images/profile.jpg` |
| Style (colors, fonts, spacing) | `_sass/_custom.scss` and `_sass/_custom_variables.scss` |

Adding a news item only requires two lines at the top of `_data/news.yml`:

```yaml
- date: "Oct 2026"
  text: "Something happened, with an optional [link](https://example.com)"
```

## Workflow

`master` is what GitHub Pages publishes, so changes go through a branch and a pull request:

1. create a branch from `master`, named after the kind of change (`feat/…` for new content or features, `fix/…` for corrections, `style/…` for visual changes, `docs/…` for documentation), and commit there using [Conventional Commits](https://www.conventionalcommits.org/) messages;
2. open a pull request: the **Jekyll build** workflow checks that the site builds in production mode;
3. merge into `master`: GitHub Pages rebuilds and deploys the site in a couple of minutes.

## Credits

Based on [Academic Pages](https://github.com/academicpages/academicpages.github.io), itself a fork of [Minimal Mistakes](https://mademistakes.com/work/minimal-mistakes-jekyll-theme/) by Michael Rose, both released under the [MIT License](LICENSE).
