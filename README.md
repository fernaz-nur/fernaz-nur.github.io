# Dr. Fernaz Narin Nur — Academic Website

A responsive academic website with a home page, a full publications page and an awards page. GitHub Pages builds it automatically with Jekyll, so nothing needs to be installed to publish or edit it.

## Common edits

All of these can be made in the browser on github.com. The site updates a minute or two after you save.

| To change | Edit |
|---|---|
| Bio, title, email, links, research interests, teaching, education, positions, fellowships, awards | `_data/profile.yml` |
| Add or change a paper, its image, or what appears on the home page | `_data/publications.yml` (instructions are at the top of the file) |
| Colours, text sizes, spacing | `style.css` |
| Page layout | `index.html`, `publications.html`, `awards.html`, `_layouts/`, `_includes/` |

## Adding the photo and CV

Add these two files to the `assets/` folder, using exactly these names:

- `assets/profile.png`: an approved portrait, square, with a transparent background
- `assets/cv.pdf`: the CV

The photo and the "CV (PDF)" link appear on their own. Until the files are added, the page leaves them out.

## Publication images

Six papers show a real figure from the paper, with a licence credit on the card. The rest have an illustration in `assets/publications/`, drawn from the title. Illustrations are decorative: they are not figures from the papers and show no results.

To use a real figure for another paper:

1. Check that the licence allows it. The papers shown with figures are under CC BY or CC BY-SA. Publishers often hold the copyright on other papers, even for the author's own figures.
2. Check that the paper doesn't credit the figure to another source, because the paper's licence may not cover it.
3. Add the image to `assets/publications/`. A wide image, about 16:10, fits best.
4. In `_data/publications.yml`, change that paper's `image:` line to the new file, then add `image_alt`, `image_credit`, `image_license` and `image_license_url`. Copy the pattern from a paper that already has a figure, and say in the credit if you changed the image.

To go back to an illustration, point `image:` at its `.svg` file and remove the other four lines. A new paper with no `image:` line gets a plain default picture.

## Where the site is published

The site is live at <https://fernaz-nur.github.io/>. GitHub Pages builds it from the `main` branch of this repository, folder `/ (root)`, and updates it a minute or two after each change.

The address comes from the `fernaz-nur` organization, which owns this repository. The repository must keep the name `fernaz-nur.github.io`. If either name changes, the address changes too, so update `url` in `_config.yml` to match.

## Previewing on your own computer (optional)

The pages are templates now, so opening `index.html` directly will show raw template code. To see the real site, you need Ruby, then run these from this folder:

```bash
bundle config set --local path vendor/bundle
```

```bash
bundle install
```

```bash
bundle exec jekyll serve
```

Then open <http://127.0.0.1:4000>.

## Where the content came from

The profile details and publication list come from the professor's [DIU faculty profile](https://faculty.daffodilvarsity.edu.bd/profile/cse/fernaz.html). DOI links, and corrections to some authors and titles, come from publisher records on [Crossref](https://www.crossref.org/).
