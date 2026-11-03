# Personal MCP Gateway site

Home: https://stantonmatthewj.gitlab.io/

- Privacy policy: https://stantonmatthewj.gitlab.io/privacy.html
- Terms of service: https://stantonmatthewj.gitlab.io/terms.html

The GitLab project is
[stantonmatthewj/stantonmatthewj.gitlab.io](https://gitlab.com/stantonmatthewj/stantonmatthewj.gitlab.io).
GitLab redirects its former project path, `stantonmatthewj/stantonmatt.github.io`,
to this project. That redirect does not redirect the old GitHub Pages website.
The local folder remains `stantonmatt.github.io`.

## CI and Pages

`.gitlab-ci.yml` checks the static copy for merge requests and publishes pushes
to `main` using an Alpine image on the `ci-public` Docker runner. Only
`index.html`, `privacy.html`, `terms.html`, `style.css` and `.nojekyll` enter the
`public/` artifact. All site links are relative, so no base-path change is needed.
Keep the Google site verification meta tag in `index.html`.

Google Auth Platform branding links and domain verification must be updated
separately in the Google Cloud console when the new site is online.

## If moving back to GitHub

The `github` remote is retained. Restore it as `origin`, enable GitHub Pages
from the root of `main`, and point links back to https://stantonmatt.github.io/.
This repository had no `.github/workflows` to preserve. If GitHub workflows
are added later, they are inactive while GitLab hosts CI and must be kept in
sync by hand if switching back.
