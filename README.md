# Overhang

**An opinionated course on the money behind the AI boom.**

Overhang is a course/blog on the economics, financing, and politics of the AI buildout — how the
hyperscaler CapEx is financed, where private credit hides risk, and how shifting public opinion and
policy could reprice it all. Read it as a blog post-by-post, or take it as a course with per-post
quizzes, module tests, a glossary, and slide decks.

It is the sister course to **[Drift](https://wesslen.github.io/)**, a course on banking GenAI risk.

🔗 **Live:** https://wesslen.github.io/overhang/

## Local development

This is a static site — no build step required to view it. Serve the folder and open it:

```bash
python -m http.server 8000
# then visit http://localhost:8000/
```

## Tooling

```bash
npm install            # dev dependencies (linting, theme/quiz tooling)

npm run build:theme    # regenerate CSS variables from theme.yaml
npm run build:quiz     # validate + test quiz question pools
npm run build:search   # regenerate the search index from posts
npm run lint           # html + markdown + format checks
```

## Structure

```
posts/            Markdown posts + index.json manifest
quizzes/          Quiz engine + per-post pools + module manifests
slides/           Static-exported slide decks + slides.json manifest
img/              Image assets
glossary.json     Glossary terms (rendered by glossary.html)
theme.yaml        Theme config (build-theme.js → style.css)
scripts/          Build/validation tooling
```

## License

Content © 2026 Ryan Wesslen, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
Code under [MIT](LICENSE).
