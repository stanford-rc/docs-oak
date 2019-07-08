# Oak (Public) Documentation

This is the Oak Storage public documentation base. It is
driven by [mkdocs-jekyll](https://www.github.com/vsoch/mkdocs-jekyll).

<div style="width:50%; align:center">
     <img src="assets/img/logo/oak.png">
</div><br>

## Usage

### 1. Get the code

You can clone the repository right to where you want to host the docs:

```bash
git clone https://github.com/stanford-rc/docs-oak.git docs
cd docs
```

### 2. Customize

Generally, you should see the the [getting started guide](https://vsoch.github.io/mkdocs-jekyll/getting-started)
for the template to better understand how to add custom elements, link to 
pages, create page tags, etc. A brief overview is provided here.


#### How do I add pages?

Documentation pages are found in [_docs/docs], and you can add them as links 
to other pages, or in the navigation directly by editing [_data/toc.myl](_data/toc.yml).
For more regular pages (e.g., "About") you can put them in the [pages](pages)
folder, and optionally add a `permalink` value to define the URL.

### How do I edit metadata?

To edit configuration values, customize the [_config.yml](_config.yml).
Most of the configuration values in the [_config.yml](_config.yml) are self explanatory,
and for more details, see the [about page](https://vsoch.github.io/mkdocs-jekyll/about/)
rendered on the site.

### How do I add alerts, boxes, and other elements?

See the [getting started guide](https://vsoch.github.io/mkdocs-jekyll/getting-started)
for the template.


### 3. Serve

Depending on how you installed jekyll:

```bash
jekyll serve
# or
bundle exec jekyll serve
```

## Development

The Drupal site hosted at [here](https://srcc.stanford.edu/oak-storage) was first extracted 
manually via the web interface. First,
we needed to download the scripts to help with conversion. We just needed to 
convert from html:

```bash
$ wget -O scripts/mw2md.py https://raw.githubusercontent.com/vsoch/mw2md.py/master/html2md.py
```

Install dependencies for the html conversion (markdownify):

```bash
$ pip install -r scripts/requirements.txt
```

Create the docs folder:

```bash
$ mkdir -p _docs
```

And then convert the html file:

```bash
for filename in $(ls src/*.html); do
    name=$(basename -- "$filename")
    name="${name%.*}"
    markdown="docs/${name}.md"
    if [ ! -f "${markdown}" ]; then
        echo "Converting $filename to $markdown"
        python scripts/html2md.py $filename $markdown
    fi
done
```

Note that after conversion, some manual work was done to fix tables (which
weren't parsed) and code blocks.
