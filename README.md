# Mark Jastin M. Andaya — Portfolio

Version: 0.1.0. A temporary contact page that can grow into a complete portfolio.

## Publish free with GitHub Pages

1. Sign in at https://github.com/MarkJastinAndaya.
2. Create a **public** repository named exactly `MarkJastinAndaya.github.io`. If it already exists, inspect it before changing anything; do not overwrite an existing website.
3. Upload this folder's contents directly to the repository root. `index.html` must be at the top level, not inside a `portfolio-placeholder` folder. Include `.nojekyll` and `.gitignore` if using Git; the website still works if the browser uploader omits these two files.
4. Open **Settings → Pages**. Under Build and deployment, select **Deploy from a branch**, branch **main**, folder **/(root)**, then Save.
5. Wait for the Pages deployment to succeed. Open the URL shown in Settings → Pages and check it on your phone.

Expected URL after successful publishing:
https://markjastinandaya.github.io/

The URL is not live merely because these files exist. Use it in the application after verifying it loads publicly.

## Use Git from the beginning (alternative to browser upload)

Create the empty repository above without generating a README, license, or .gitignore on GitHub. Open this extracted folder in VS Code, then run:

```sh
git init -b main
git add .
git commit -m "Create portfolio placeholder v0.1.0"
git remote add origin https://github.com/MarkJastinAndaya/MarkJastinAndaya.github.io.git
git push -u origin main
git tag v0.1.0
git push origin v0.1.0
```

Git may ask you to configure your name/email or sign in through your browser. Authenticate through GitHub; do not store passwords or tokens in the repository. Enable Pages using step 4 above.

If you already uploaded using the browser, clone the existing repository instead of initializing and pushing unrelated history:

```sh
git clone https://github.com/MarkJastinAndaya/MarkJastinAndaya.github.io.git
cd MarkJastinAndaya.github.io
```

## Preview locally

Open `index.html` directly, or from this folder run:

```sh
python -m http.server 8000
```

Then visit http://localhost:8000. No npm packages, API keys, or build commands are needed.

## Update safely

Keep `main` as the published version. Start future work with:

```sh
git switch main
git pull --ff-only
git switch -c portfolio-development
```

Edit locally and preview before committing. Push your development branch and open a pull request to `main`. Merge when ready to publish; GitHub Pages will redeploy the updated site. The same URL stays valid.

Use `v0.2.0` for the initial project/about sections, and `v1.0.0` for the first complete portfolio. Update CHANGELOG.md for each release. Tags mark releases; commits preserve the detailed history. To undo a published change, use `git revert <commit-hash>` and push the new commit.

## Edit content

- `index.html`: name, message, contact details, and metadata.
- `styles.css`: colors, typography, and responsive layout.
- `favicon.svg`: browser tab mark.

The telephone displays in Philippine local format and links using `+639654729034`. Email and telephone links open the visitor's configured applications. LinkedIn and GitHub open in new tabs. The page has no contact form, analytics, external font dependencies, or tracking scripts.
