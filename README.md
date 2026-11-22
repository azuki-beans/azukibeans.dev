# azukibeans.dev

Static landing page for the [azuki-beans](https://github.com/azuki-beans) projects:
English at `/`, Italian at `/it/`. Plain HTML + CSS, no build step, no JavaScript, no cookies.

## Deploy (Cloudflare Pages)

The `azukibeans.dev` zone is already on Cloudflare.

1. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git → `azuki-beans/azukibeans.dev`.
2. Framework preset: *None*, build command empty, output directory `/`.
3. Custom domains → add `azukibeans.dev` (and optionally `www.azukibeans.dev` with a redirect to the apex).

Every push to `main` publishes the site. `_headers` sets the security headers.

## Adding a project

Add a card to both `index.html` and `it/index.html` (and, for a web app, a `WebApplication`
entry in the JSON-LD of `index.html`). Then add the hub link to the new project's footer.
