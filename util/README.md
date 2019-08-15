# Usage

## Automatic Mode

### Install

**Installation and Build requires `python3` and `nodejs`**

1. Install latest [node and npm](https://nodejs.org/en/download/package-manager/)

2. Install latest [python3](https://www.python.org/downloads/).

3. Run `./install.sh`

### Build

1. Go to root directory

2. Run `./build.sh`

### Deploy (Run after build)

3. `git add .; git commit -m "Add writeup"`

4. `git push origin master`

-----

## Manual Mode

## Install

### markdown-toc-generator

Generate table of contents in Markdown.

Install: Python 3.7 is required.

### markdown-to-html

Render Markdown to stunning responsive web page with LaTeX support.

```sh
cd markdown-to-html
# Install Markdown to static HTML generator (https://github.com/mixu/markdown-styles)
npm install markdown-styles
# Install customized layout 
cp -r r3kapig node_modules/markdown-styles/layouts/
```

## Generate a CTF Writeup

### Manually

Make sure your working directory is the root of Git repository.

1. `mkdir YYYYMMDD-ctfname`
2. `cp your-ctf-writeup.md YYYYMMDD-ctfname/README.md`
3. `./util/markdown-to-html/node_modules/markdown-styles/bin/generate-md --layout r3kapig —input YYYYMMDD-ctfname/README.md --output YYYYMMDD-ctfname`
4. `mv YYYYMMDD-ctfname/README.html YYYYMMDD-ctfname/index.html`
5. `./util/markdown-to-html/gen-sidebar.py YYYYMMDD-ctfname/index.html`
6. `./util/markdown-toc-generator/gen-toc.py YYYYMMDD-ctfname/README.md`


# Markdown Format

### TOC

In order to generate table of contents correctly in Markdown, your input should like this:

```markdown
# r3kapig CTF

[TOC]

## Web

### web 1

## Reverse

### reverse 1
```
