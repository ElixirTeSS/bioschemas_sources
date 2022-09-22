# Bioschemas Sources
This repository contains a list of sources that [TeSS](https://tess.elixir-europe.org/) will scrape for relevant Bioschemas-marked-up resources.

Each source will be scraped once per day at ~3AM UTC.

## Bioschemas
TeSS currently understands the following Bioschemas profiles:
* [CourseInstance](https://bioschemas.org/profiles/CourseInstance/0.9-DRAFT) - Will be registered as TeSS events.
* [Course](https://bioschemas.org/profiles/Course/0.10-DRAFT) - Each `CourseInstance` under the `hasCourseInstance` property will be registered as a TeSS event, with any missing metadata pulled in from the `Course`.
* [Event](https://bioschemas.org/profiles/Event/0.2-DRAFT-2019_06_14) - Will be registered as TeSS events.
* [TrainingMaterial](https://bioschemas.org/profiles/TrainingMaterial/1.0-RELEASE) - Will be registered as TeSS materials.

Information on how to implement Bioschemas on your site can be found [in the Bioschemas documentation](https://bioschemas.org/tutorials/howto/howto_add_markup).

## Sitemap
Your site will also need a [sitemap](https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview), which is basically a directory listing of all the pages on your site. TeSS crawls through each page of the sitemap and checks for markup from the above Bioschemas profiles.

Sitemaps are an established standard, and there should be sitemap libraries and plugins available for whichever system you are using to provide your website.

## How to add a source

If you have implemented one or more of the above Bioschemas profiles, and you have a sitemap available, you can now submit your site as a "source" to be scraped:

1. [Register a Content Provider in TeSS](https://tess.elixir-europe.org/content_providers/new) (requires a TeSS account) if you have not already.

2. Make note of your Content Provider's exact Title and URL, which you can copy from the "Edit" page, e.g.
![image](https://user-images.githubusercontent.com/503373/191801899-c6dde1bc-c802-4c3c-b7f1-96665abe7178.png)

3. [Click here to edit the `sources.yml` file](https://github.com/ElixirTeSS/bioschemas_sources/edit/main/sources.yml) and add your content provider details along with the URL to your sitemap, e.g.
```yml
  - title: Galaxy Training # The title of your Content Provider on TeSS
    url: http://galaxyproject.github.io/training-material # The URL of your Content Provider on TeSS
    source: https://training.galaxyproject.org/training-material/sitemap.xml # The URL to your sitemap.xml file that TeSS should crawl
```

*It's important to make sure the title and URL exactly match the Content Provider's title and URL on TeSS*

4. After making your change, click the button to open a pull request, which will then be reviewed. If everything worked correctly, your content should appear in TeSS the following day.
