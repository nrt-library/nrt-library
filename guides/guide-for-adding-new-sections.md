# Instructions to add new content sections to the NRT-Library website

Here are the instructions to add new sections to the NRT-Library site.

It is recommended to work in your own branch of the project. Then merge with the master branch once your new section is ready.

## Prerequisities

Follow the instructions in the `guide-for-local-build.md` file. Then you should be ready to add new sections.

## Files to create or modify

### Section content

The content that will be displayed in the website for new section must be created in the `pages/` directoy. You first need to create a new directory with the name of your new-section, to then add the markdown files with the actual seciton content. There are two types of markdown files you need to create: (1) a landing-page file, which is the page people will see when first landing on the section, and (2) markdown files with the sub-section contents.

In the terminal, this will look something like:

```bash
# make sure you are in the nrt-library/ base directory
pwd

# make new directory
mkdir ./pages/my-new-section

# create landing-page
touch ./pages/my-new-section/my-sectionName-landing-page.md

# create subsection 01
touch ./pages/my-new-section/my-subsectionName-01.md

# create subsection 01
touch ./pages/my-new-section/my-subsectionName-01.md

# create as many subsections as you need
```

Section contents are plain Markdown files. The `html` diplayed in the website will be automatically generate in the `_site` folder.

## Section sidebar

Each section requieres a sidebar menu to be navigated. Sidebar are `.yml` files in the `_data/sidebars` directory.

In the terminal you can type:

```bash
# make sure you are in the nrt-library/ base directory
pwd

# create section sidebar .yml file
touch ./_data/sidebars/my_sectionNAme_sidebar.yml
```

Sidebars .yml file have the following structure:

```yml
entries:
- title: Sidebar # leave this as it is
  product: NLP # this is the first part of title at the top of the sidebar
  version: Intro # this is the second part of title at the top of the sidebar
  folders:

```


in _data/sidebars
create:
my-new-bar.yml
modify:
home_sidebar.yml

in _data/
modify:
topnav.yml
tags.yml



in pages/tags/
create:
tag_tagname.md

in nrt-lbrary/
modify:
_config.yml