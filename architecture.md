Working with the project Gutenberg website has its complexities.

The site is served at ibiblio, on multiple virtualized machines running Apache behind a load balancer. Static content is stored in a file system, most dynamic content is served by a python application, Autocat3, https://github.com/gutenbergtools/autocat3 .  Autocat3 talks to a Postgres backend.

Static web content is generated from markdown by Jekyll; static book content is stored in 2 directories, one for source files (the "1/2/3" tree, and one for generated files (the "cache/epub" tree). Generated files are regenerated from source files one a month. 
Most of static site content is maintained in https://github.com/gutenbergtools/gutenbergsite

There also remain a few PHP scripts that are used, one to maintain the database, another to provide assistance to people wanting to mirror the content part of the website.
