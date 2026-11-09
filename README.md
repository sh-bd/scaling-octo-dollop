# Personal engineering portfolio

A responsive, static portfolio inspired by the supplied reference. All editable website content is stored in **`data/site.yml`**. The layout and interactions live in `index.html`, `css/site.css`, and `js/site.js`.

## Edit your content

1. Open `data/site.yml` on GitHub.
2. Edit your name, bio, links, education, experience, projects, skills, research interests, and contact details.
3. Commit the change. GitHub Pages will redeploy automatically.

YAML uses indentation to represent nesting. Keep spaces consistent (two spaces is a good convention). Put text containing `: ` in quotes. For a long paragraph, use a quoted string or YAML block scalar (`|`).

## Add images and your CV

Upload your files under `assets/` or `assets/projects/`, then update the corresponding image/CV paths in `data/site.yml`. Keep file names lowercase and avoid spaces. Example:

```yaml
profile:
  portrait: assets/shamim.jpg
  cv: assets/shamim-cv.pdf
```

The repository includes placeholder image paths only. Replace them with your own files. Missing images are hidden rather than breaking the page.

## Enable the contact form

The form uses Formspree. Create a form at https://formspree.io, copy its form ID, and replace `YOUR_FORMSPREE_ID` under `contact.formspree_id` in `data/site.yml`. The form will then submit without a backend server. Or leave the placeholder and use the email link only.

## Deploy to GitHub Pages

1. Create a GitHub repository. For the easiest URL, name it `YOUR_USERNAME.github.io`.
2. Upload the contents of this folder to the repository root and push to the `main` branch.
3. In GitHub, open **Settings → Pages** and select **GitHub Actions** as the build and deployment source.
4. The included workflow at `.github/workflows/pages.yml` will deploy on each push to `main`.

For a project repository instead of a `username.github.io` repository, this site uses relative asset/data paths and should work at the repository subpath too.

## Preview locally

Because the page fetches a YAML file, open it through a local server rather than double-clicking `index.html`:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Important

- Update all sample contact/social URLs before publishing.
- Review the project descriptions and replace placeholder images with real screenshots.
- The starter content is based on the information available in the conversation. Add missing details and links in `data/site.yml`.
