# Bioschemas Sources
This repository is deprecated in favour of self-management of Bioschemas sources from within TeSS itself.

See: https://tess.elixir-europe.org/about/registering#sources

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

If you have implemented one or more of the above Bioschemas profiles, and you have a sitemap available, you can now submit your site as a "source" to be scraped, see: <https://tess.elixir-europe.org/about/registering#sources>
