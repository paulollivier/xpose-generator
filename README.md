# xpose-generator

This simple script is something I did rather quickly to generate the website we
needed to create in the context of the [presentations done in third year of CS
engineering at ESIPE][1].

It is very simple: it takes the information describe in `a`, a text file
containing meta-information, and every markdown file it finds in `content`, and
generates the proper html tree in `build`.

## Installation

    git clone <url_of_the_git_repository_you_are_viewing_this_file_on>
    cd xpose-generator
    pip install .

Once this is done, you can call `xposegen`, in the directory of your choice.

## How to write content:

Write the `a` file required by ESIPE's integration system, following the
instructions [here][2].

Simply write a .md file in `content/`, write a line `Title: My Title Here` on
top of the file, and then write your content. Note: For presentation purpose,
don't write `<h1>` tags, aka `#`, in markdown. 

Here be samples (and dragons):

    Title: This is my test page
    ## Hello, world

    Hello, world. I am writing some stuff in markdown.
    [This is a link to another page, with header][hello.html#title]

If you have images, etc... Just put it in `content/` with everything else.

So you have (approximately, you may have more files in `content/`...) this structure:

    [paul@styx:xpose] master ± tree
    .
    ├── a
    └── content
        └── index.md


# Contributing

Please, feel free to clone the repository, make your stuff, and eventually make
a pull request to merge what you did? That would be nice.

Also, even if you don't want to merge your code, an email will be appreciated.

## TODO

* Support directory use in `content/`
* Add support for custom css
* do not hard-code everything; add support for cli args, or conffile
* Decrease every header if a `# title` is detected.


[1]: http://www-igm.univ-mlv.fr/~dr/xall.php
[2]: http://www-igm.univ-mlv.fr/~dr/XPOSE/modalites.html
