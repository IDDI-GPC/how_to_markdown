# Write and publish Markdown documentation

Markdown is a lighweight markup language, easier to deal with than html, and designed for the web.

```mermaid
%%{init: {'theme': 'forest' } }%%
  graph LR
      A(Mardown \n file) --> B(Markdown \n Processor)
      B --> C(HTML doc \n generation)
      C -->D(Website)
```

To create webpages from Markdown files, we first need a static site generator. We work with [MkDocs](https://www.mkdocs.org/).

The generated documentation should be version-controlled and pushed on the web. We work with a GitHub repository.

## Creating documentation with MkDocs 

### Installation

To install MkDocs, run the following command from the command line:

```
pip install mkdocs
```

To create your documentation project (navigate to your repo folder first):

```
python -m mkdocs new my-doc
```

The `my-doc` folder that was just created should look like this:

```
<repo>\my-doc
                      |
                      |- docs\index.md
                      |- mkdocs.yml
                                                                          
```
There's a single configuration file named `mkdocs.yml`, and a folder named `docs` that will contain your documentation source files.

### Local build

To preview documentation:

```
python -m mkdocs serve
```

Preview is available at `http://127.0.0.1:8000/`.

You can learn more about how to edit the site [here](https://www.mkdocs.org/getting-started/#creating-a-new-project).

Finalyl, to build html documentation, type:

```
python -m mkdocs build
```
A `site` folder is created in `my-doc` with all the html files.

### Deploy pages on GitHub

If you want to push the documentation on GitHub, so you can get update the online documentation, type:

```
python -m mkdocs gh-deploy
```

This command will commit the documentation directly to your GitHub repository. The updated GitHub webpage should be available within few minutes.

### Interesting packages to install

+ [`markdown-include`](https://github.com/cmacmackin/markdown-include)
+ [`mkdocs-video`](https://github.com/soulless-viewer/mkdocs-video)
