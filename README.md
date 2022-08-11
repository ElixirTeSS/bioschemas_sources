# Bioschemas Sources
A list of sources for TeSS to scrape for relevant Bioschemas-marked-up resources.

## How to add a source
[Edit the `sources.yml` file](https://github.com/ElixirTeSS/bioschemas_sources/edit/main/sources.yml) and add your content provider details along with the URL to your sitemap.

Example:
```yml
  - title: Galaxy Training # The title of your Content Provider on TeSS
    url: http://galaxyproject.github.io/training-material # The URL of your Content Provider on TeSS
    source: https://training.galaxyproject.org/training-material/sitemap.xml # The URL to your sitemap.xml file that TeSS should crawl
```

*It's important to make sure the title and URL exactly match the Content Provider's title and URL on TeSS*

After making your change, click the button to open a pull request, which will then be reviewed.
