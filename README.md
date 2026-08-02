# Blog

Personal blog. Plain HTML and one stylesheet — no build step, no dependencies.

```
index.html          post list (edit this when you publish)
about.html
404.html
style.css           all styling, light + dark
posts/
  hello-world.html
  _template.html    copy this to start a new post
images/             put post images here
.nojekyll           tells GitHub Pages to serve files as-is
```

## Publishing a post

1. Copy `posts/_template.html` to `posts/your-post-slug.html`.
2. Fill in the four numbered spots marked in the template's comments
   (title, date, body, index entry).
3. Add an entry at the **top** of the `<ul class="posts">` list in `index.html`:

   ```html
   <li>
     <time datetime="2026-08-15">August 15, 2026</time>
     <h2><a href="posts/your-post-slug.html">Your Post Title</a></h2>
     <p>One sentence of summary.</p>
   </li>
   ```

4. Push:

   ```
   git add .
   git commit -m "Post: Your Post Title"
   git push
   ```

The site rebuilds automatically; changes are usually live within a minute.

## Previewing locally

Just double-click `index.html` — it opens in your browser and works fully.
Refresh after each edit.

## Notes

- Dark mode follows the reader's system setting. There's no toggle by design.
- The favicon is an inline SVG in each page's `<head>`; change the `✎` character
  to swap it.
- Keep the reading width alone unless you mean it — `--measure` in `style.css`
  is set to roughly 65 characters per line, which is the comfortable range for
  body text.
