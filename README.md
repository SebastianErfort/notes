<img src="https://img.shields.io/badge/Material_for_MkDocs-526CFE?style=for-the-badge&logo=MaterialForMkDocs&logoColor=white" />

## Description

Repository to collect my notes, build static HTML documentation using MkDocs-Material, and publish them on (GitHub for now) Pages.

Sources are plug and play as Git submodules in `docs/`.


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


## Alternatives

- [ObsidianPublisher](https://github.com/ObsidianPublisher/mkdocs-publisher-template): I used the `mkdocs-publisher-template` to improve and extend my MkDocs based solution
- [Quartz](https://quartz.jzhao.xyz/)
    > Quartz is a fast, batteries-included static-site generator that transforms Markdown content into fully functional websites. Thousands of students, developers, and teachers are already using Quartz to publish personal notes, websites, and digital gardens to the web.
