## Welcome to Minfei's GitHub Pages

For this page you can find some alternatives for documentation tools. 
```
- jekyll
- docsify
- Mark
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


## Jekyll

Jekyll is a static site generator with built-in support for GitHub Pages and a simplified build process. Jekyll takes Markdown and HTML files and creates a complete static website based on your choice of layouts. Jekyll supports Markdown and Liquid, a templating language that loads dynamic content on your site. For more information, see Jekyll.

We recommend using Jekyll with,
```
- Github pages
```
[Instructions & Reference](https://docs.github.com/en/pages).

## Docsify
docsify generates your documentation website on the fly. Unlike GitBook, it does not generate static html files. Instead, it smartly loads and parses your Markdown files and displays them as a website. To start using it, all you need to do is create an index.html and deploy it on
```
- Github pages
- Containerized environment in AKS cluster, exposed via Ingress
```
[Instructions & Reference](https://docsify.js.org/#/quickstart).

## Mark
Mark reads your Markdown file, creates a Confluence page if it doesn’t, uploads attachments if any, translates Markdown into HTML, and updates the contents of the page via REST API.

Mark uses an extended file format, which, still being valid markdown, contains several HTML-ish metadata headers, which can be used to locate page inside Confluence instance and update it accordingly.

```
- Confluence
```
[Instructions & Reference](https://samizdat.dev/use-markdown-for-confluence/).

## DocZ and other similar doc site generator
There are a list of static site generator for documentations. They are hosted in a containerised environment, exposed via Kubernetes ingress. 
