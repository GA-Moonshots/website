# Moonshots website

The public site for Moonshots, FTC #21681: https://ga-moonshots.netlify.app/

It's plain HTML. There's no build step: edit `index.html`, commit, push to `main`, and Netlify
publishes it within a minute or so.

## Editing

- **Words**: `index.html`. Each section starts with a comment like `<!-- PAST ROBOTS -->`.
- **Photos**: `static/images/team/`. Resize to at most 1600 px on the long side before adding a
  photo (on a Mac: `sips -Z 1600 photo.jpg`). A phone photo is 4–6 MB, and a slow page ranks lower
  in search.
- **Every `<img>` needs an `alt`** describing it. Screen readers and search engines both read it.

## Search engines

The `<head>` of `index.html` carries what Google shows: the title, the description, the link
preview (`og:` tags), and a structured-data block saying we're FTC team #21681. Keep them accurate
when the season changes. `robots.txt` and `sitemap.xml` point crawlers at the page.

The error pages (`403`, `404`, `500`) are marked `noindex` so they never show up in results.
