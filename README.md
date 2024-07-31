<img src="https://img.shields.io/badge/Material_for_MkDocs-526CFE?style=for-the-badge&logo=MaterialForMkDocs&logoColor=white" />

## Description

Repository to collect my notes, build static HTML documentation using MkDocs-Material, and publish them on (GitHub for now) Pages.

This choice was a bit arbitrary, I was setting up a documentation system for work, using MkDocs, at the time. There are probably better alternatives that work better in the Obsidian ecosystem, that I am generally using to compose notes. MkDocs has to be extended and configured a fair bit to achieve reasonable compatibility with Obsidian Markdown.
See [[obsidian#publishing|my notes on publishing Obsidian notes]] for alternatives.
I used the [`mkdocs-publisher-template`](https://github.com/ObsidianPublisher/mkdocs-publisher-template) to improve and extend my MkDocs based solution

By using Markdown and keeping notes in a separate repository, this system is very pluggable and switching to a different publishing tool should be as pain free ass possible. Sources are incorporated as Git submodules.


## To Do

- [ ] trigger build from notes Markdown repo instead of schedule
- [ ] transfer Markdown+YAML linters to stand-alone repo and use them for `pre-commit` hooks (Git or [pre-commit framework](https://pre-commit.com/))
- [ ] ensure Nerd Font is available in online version
- [ ] style internal and external links differently - use Javascript to classify, e.g.

    ```js
    document.querySelectorAll('a').forEach(link => {
        const url = link.href;
        if (url.includes('http')) {
            link.classList.add('external-link');
        } else {
            link.classList.add('internal-link');
        }
    });
    ```

    or with CSS

    ```css
    a[href^=http] {
        /* external link style */
    }
    a[href^=http]::after {
        /* external link icon */
    }
    ```


