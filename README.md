# Urban Cognition Lab website

Plain HTML/CSS site hosted on GitHub Pages at https://lilyjohnsonulrich.com

## Pages
index, research, people, publications, in-the-news (News), dei (Outreach), photos, artscience, join

## Common edits
- **CV:** save your CV as `files/Johnson-Ulrich_CV.pdf` (exact name). Every "CV" button links there.
- **Lab update:** in `in-the-news.html`, copy one `<li>` in the "Lab updates" list and paste it at the top.
- **Student photo/bio:** put the photo in `images/` (e.g. `images/tracey.jpg`). In `people.html`, replace
  `<div class="avatar" aria-hidden="true">T</div>` with `<img class="avatar" src="images/tracey.jpg" alt="Tracey">`
  and replace "Bio coming soon." / "Student Researcher" with real text.
- **Coyote photo:** in `research.html`, replace the `<div class="project-img placeholder-img" ...>...</div>` block with
  `<div class="project-img"><img src="images/coyote.jpg" alt="A coyote"></div>`.
- The menu and footer repeat on every page; change all pages if you edit them.

## Publish changes
```
git add .
git commit -m "Describe change"
git push
```
