# my-writings

Personal site built with Jekyll. No theme gem: the layouts in `_layouts/` and
the one stylesheet at `assets/css/main.css` are everything.

## Preview locally

    bundle exec jekyll serve

Then open http://localhost:4000. Restart after editing `_config.yml`.

## Publish

    bin/deploy

Builds the site and pushes the built files to the `gh-pages` branch, which
GitHub Pages serves at https://christiankf7.github.io/. Run it whenever you
want the live site updated. Separately, `git push` saves the source to `main`.

## Write a blog post

    bin/new-post "Post Title" climbing

This creates `_posts/YYYY-MM-DD-post-title.md` with the front matter filled in.
Write Markdown below the second `---`.

Front matter fields:

| Field      | Required | Notes                                                        |
| ---------- | -------- | ------------------------------------------------------------ |
| `title`    | yes      |                                                              |
| `date`     | yes      | `YYYY-MM-DD`                                                 |
| `category` | yes      | One word or phrase. New categories appear on /blog/ on their own. |
| `quote`    | no       | Epigraph shown under the title.                              |
| `quote_by` | no       | Who said it.                                                 |
| `math`     | no       | `true` loads MathJax for LaTeX on that post.                 |

Images go in `assets/images/` and are referenced as
`![alt text]({{ '/assets/images/name.jpg' | relative_url }})`.

## Edit media recommendations

Edit `_data/media.yml`. Each list is ranked top to bottom; an entry is a
`title` and a `genre` line.

## Other things to edit

- Site title, tagline, header links, footer links: `_config.yml`
- Home page intro text: `index.markdown`
- About page: `about.markdown`
- Colors and fonts: the `:root` block at the top of `assets/css/main.css`
