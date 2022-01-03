---
title: INDEX
layout: template
filename: index.md
--- 
## Welcome to Minfei's GitHub Pages

For this page you can find some alternatives for documentation tools. 
```
- GitHub Pages and Jekyll
- Mark
- Docsify, DocZ and other site generator
```

## Why

We looking into documentation tools that supports markdown and proper documentation management, updates management and version controll.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).


## GitHub Pages and Jekyll

Jekyll is a static site generator with built-in support for GitHub Pages and a simplified build process. Jekyll takes Markdown and HTML files and creates a complete static website based on your choice of layouts. Jekyll supports Markdown and Liquid, a templating language that loads dynamic content on your site. For more information, see Jekyll.

We recommend using Jekyll with,
```
- Github pages
```
Github pages can create the protect the site [visibility](https://docs.github.com/en/pages/getting-started-with-github-pages/changing-the-visibility-of-your-github-pages-site) with granted user access. Besides, the Github pages provides managed cert for HTTPS connection.
[Instructions & Reference](https://docs.github.com/en/pages).

We can use a centralised GitHub repo to host all Lanes@Scale documentations, in which case, we need to maintain it with an additional PR from a code PR. Alternatively, we can also host dedicated documentations in the code repo with Path `./docs/index.md`. In this case, the default URL is randomized. Here is an exmaple of ADPU-infra [doc](https://upgraded-chainsaw-a4b14c57.pages.github.io/).

Pros:
- Driven by git code best practices and managed in a GitHub repo.
- SaaS hosted on GitHub, easy to use and config.
- Pre-defined themes.
- Simple integration with 404 page.
- Same visibility management as code repositories.
- HTTPS protected by GitHub certificate management.
- Markdown supported and not frontend coding.

Cons:
- No priviledge to set up organizational-level custom domain.

## Mark
Mark reads your Markdown file, creates a Confluence page if it doesn’t, uploads attachments if any, translates Markdown into HTML, and updates the contents of the page via REST API.

Mark uses an extended file format, which, still being valid markdown, contains several HTML-ish metadata headers, which can be used to locate page inside Confluence instance and update it accordingly.

```
- Confluence
```
[Instructions & Reference](https://samizdat.dev/use-markdown-for-confluence/).

Pros:
- Driven by git code best practices and managed in a GitHub repo.
- Markdown supported.
- Post docs to confluence, where visbility management, TLS certs are already in place.

Cons:
- CI/CD needs to be configured for deployment.
- Posting to confluence requires personal confluence token.
- GitHub code version control doesn't align with Conluence's version.

## Docsify, DocZ and other similar doc site generator
There are a list of static site generator for documentations. They are hosted in a containerised environment, exposed via Kubernetes ingress. For example, `Docsify` generates your documentation website on the fly. Unlike GitBook, it does not generate static html files. Instead, it smartly loads and parses your Markdown files and displays them as a website. To start using it, all you need to do is create an index.html and deploy it on
```
- Containerized environment in AKS cluster, exposed via Ingress
```
Pros:
- Driven by git code best practices and managed in a GitHub repo.
- Markdown supported.
- Flexibility to customise site design with frontend coding.

Cons:
- Hosted on Kubernetes cluster, where efforts expected from stability, observebility and computing resources.
- CI/CD needs to be configured for deployment.
- No Handy HTTPS, taking efforts to provision and manage TT internal certificate.
- Visibility management.
- Involving frontend coding.
