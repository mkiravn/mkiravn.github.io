# mkiravn.github.io

Personal academic site for Mariadaria Ianni-Ravn, served by GitHub Pages from the
`gh-pages` branch at <https://mkiravn.github.io>.

## Layout

```
index.html      All page content — there is no build step or generator.
css/main.css    Single stylesheet. Colours and type live in the :root block.
cv.pdf          Linked from the CV section and the footer.
profile.jpg     Header portrait, 500px square.
favicon.png
```

## Editing

Open `index.html` and edit it directly, then commit to `gh-pages`. Pages redeploys
within a minute or so.

Publications, talks, awards and volunteering entries all share the same markup:

```html
<li class="entry">
  <div class="entry-aside"><span class="entry-year">2025</span></div>
  <div>
    <p class="entry-title"><a href="https://doi.org/10.1234/example">Title</a></p>
    <p class="entry-meta">Authors <span class="entry-venue">· Venue</span></p>
  </div>
</li>
```

Wrap your own name in `<span class="me">` so it reads bolder than the co-authors.

## Updating the CV

Replace `cv.pdf` in the repository root. Both links point at that filename, so no
markup changes are needed.

## Replacing the portrait

Keep it square and around 500px. The source photo should be resized before
committing — the original was 21 MB, which made the page unusable on mobile:

```bash
sips -s format jpeg -s formatOptions 82 -Z 500 source.png --out profile.jpg
```

## Colours and type

Every colour is a custom property in the `:root` block of `css/main.css`. The palette is
Sanzo Wada combination 143 (Blue, Lilac, Warm Gray) on near-white paper, with IBM
Plex Sans for text and IBM Plex Mono for metadata.

The contour lines behind the header are an inline SVG in `index.html`; their
stroke colour is hardcoded to match `--contour`.
