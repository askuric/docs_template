# This is the simplefoc documentation theme based on jekyll documentation theme just-the-docs

It is used to generate the documentation website for the SimpleFOC project. See the [SimpleFOC documentation](https://docs.simplefoc.com) for more information.

## Usage

To use this theme, add `remote_theme: simplefoc/simplefoc-jekyll-theme` to your `_config.yml` file.

```yaml
remote_theme: simplefoc/simplefoc-jekyll-theme
```

## Running the site using anaconda environement

Nice tutorial: https://s-canchi.github.io/2021-04-30-jekyll-conda/

First create the new anaconda environmnet using the `environment.yaml`file

```
conda env create -f environement.yaml
conda activate simpledocs
```

Once in the environment `simpledocs` install jekyll

```
gem install jekyll bundler
```

Then install necessary jekyll dependencies of the simplefoc docs:

```
# Optionally specify "--path /some/other/dir" to avoid needing root.
bundle install
```

And you're ready to go!

Just make sure that whenever you open your terminal to generate the website to activate the conda environment:
```
conda activate simpledocs
```

## Generating the website

To generate the site locally clone the repo to your local directory and then open terminal inside the repo folder and run:

```
bundle exec jekyll serve
```

Since the site is quiet large sometimes the `--incremental` flag helps with faster execution

```
bundle exec jekyll serve --incremental
```

## Olddocs generating 

1) Add the library version to the index.md 
2) modify the `_config.yaml`
    - `url: "http://olddocs.simplefoc.com" `
    - `baseurl: "v2.2.3"`  
3) run `bundle exec jekyll build`
4) in `_site` you have the generated html
