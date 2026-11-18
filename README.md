# Personal MCP Gateway site

Home: https://stantonmatt.github.io/

- Privacy policy: https://stantonmatt.github.io/privacy.html
- Terms of service: https://stantonmatt.github.io/terms.html

The primary repository is
[StantonMatt/stantonmatt.github.io](https://github.com/StantonMatt/stantonmatt.github.io).
The GitLab repository has a different name:
[StantonMatt/stantonmatt.gitlab.io](https://gitlab.com/StantonMatt/stantonmatt.gitlab.io).

## Pages

GitHub Pages serves the root of `main` directly. The site is plain HTML and CSS;
`.nojekyll` disables Jekyll processing, so no build workflow is needed. Keep
`index.html`, `privacy.html`, `terms.html`, `style.css` and `.nojekyll` at the root.
All site links are relative. Keep both Google site verification meta tags in
`index.html`.

Before publishing, check that the HTML and CSS files are nonempty and that local
links resolve. The former GitLab pipeline only copied these files and checked
their presence; it did not compile or transform them.

GitLab CI/CD is disabled. The already-published GitLab Pages site remains at
https://stantonmatt.gitlab.io/ and will not receive new deployments while CI is
disabled. Check Google Auth Platform branding links and domain verification
separately in the Google Cloud console when changing the site's public domain.

Local remotes use `origin` for GitHub and `gitlab` for GitLab. The different
repository names require mirror name mapping; do not add this repository to a
same-name mirror list.
