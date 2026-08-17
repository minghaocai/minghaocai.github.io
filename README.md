# Mark (Minghao) Cai

Personal academic website. Source for [minghaocai.github.io](https://minghaocai.github.io).

Visual layout follows the HCI homepage pattern of [Parastoo Abtahi](https://parastooabtahi.com/). Content migrated from the previous Google Site.

## Local preview

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://127.0.0.1:4000`.

## Custom domain

The site is first published at `https://minghaocai.github.io`. To point `minghaocai.com` at GitHub Pages later:

1. Add a `CNAME` file in the repo root containing `minghaocai.com`
2. In the domain registrar, set GitHub Pages DNS records ([docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site))
3. In the repo: Settings → Pages → Custom domain → `minghaocai.com`
