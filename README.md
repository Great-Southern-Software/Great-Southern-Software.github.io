# Great Southern Software - company site

Company front door for [Great Southern Software](https://greatsouthernsoftware.com.au),
built with [Quarkus Roq](https://iamroq.dev/) and deployed to GitHub Pages at
`greatsouthernsoftware.com.au`.

The GitHub repository must be named exactly `Great-Southern-Software.github.io`
(the magic name for an organisation site), public, publishing via the
`deploy.yml` workflow.

## Layout

- `src/main/resources/content/` - pages (`index.html`, `404.html`)
- `src/main/resources/templates/layouts/` - Qute layouts (`default.html`)
- `src/main/resources/public/` - static assets served as-is (CSS, fonts, brand
  assets, favicons, `CNAME`)

Brand assets and the brand guide live in `src/main/resources/public/assets/brand/`.
Fonts (Space Grotesk, Inter - both SIL OFL) are self-hosted variable woff2 files;
no third-party requests, no analytics, no cookies.

## Local dev

```shell
mvn quarkus:dev
```

Then open <http://localhost:8080>. Live reload applies content and CSS changes.

## Static build

```shell
QUARKUS_ROQ_GENERATOR_BATCH=true mvn package quarkus:run -DskipTests
```

The generated site lands in `target/roq/`.

## Deploy

Pushes to `main` trigger `.github/workflows/deploy.yml`, which uses the official
`quarkiverse/quarkus-roq` GitHub Action to build the site and publish it to
GitHub Pages.

## TODO before go-live

- Create `hello@greatsouthernsoftware.com.au` as an alias/group in Google Workspace.
- Add the GoDaddy DNS records (A/AAAA at apex + `www` CNAME), set the custom
  domain in repo Settings → Pages, and enable **Enforce HTTPS** once the
  certificate provisions.
- No ™/® anywhere until the IP Australia trade mark search (classes 9 and 42)
  is done.
