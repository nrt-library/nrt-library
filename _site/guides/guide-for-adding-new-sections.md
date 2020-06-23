# Instructions to add new content sections to the NRT-Library website

Here are the instructions to add new sections to the NRT-Library site.

It is recommended to work in your own branch of the project. Then merge with the master branch once your new section is ready.

## Prerequisities

Follow the instructions in the `guide-for-local-build.md` file. Then you should be ready to add new sections.

## This to create or modify

in _data/sidebars
create:
my-new-bar.yml
modify:
home_sidebar.yml

in _data/
modify:
topnav.yml
tags.yml

in pages/
create:
my-new-section/
within that:
my-new-section-landing-page.md
sub-section-01.md
sub-section-02.md
sub-section-03.md
etc...

in pages/tags/
create:
tag_tagname.md

in nrt-lbrary/
modify:
_config.yml


