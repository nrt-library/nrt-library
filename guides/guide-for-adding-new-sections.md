# Instructions to add new content sections to the NRT-Library website

Here are the instructions to add new sections to the NRT-Library site.

It is recommended to work in your own branch of the project. Then merge with the master branch once your new section is ready.

## Prerequisities

Follow the instructions in the `guide-for-local-build.md` file. Then you should be ready to add new sections.

## Files to create or modify

This is the sequence of files that need to be created or modified:

- New section contents
- New section sidebar
- Home sidebar
- Top navigation bar
- Tags
- Config

### New section contents

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

### Section sidebar

Each section requieres a sidebar menu to be navigated. Sidebar are `.yml` files in the `_data/sidebars` directory.

In the terminal you can type:

```bash
# make sure you are in the nrt-library/ base directory
pwd

# create section sidebar .yml file
touch ./_data/sidebars/my_sectionNAme_sidebar.yml
```

Sidebars `.yml` file have the following structure:

```yml
entries:
- title: Sidebar # leave this as it is
  product: SectionName # this is the first part of title at the top of the sidebar
  version: SectionName # this is the second part of title at the top of the sidebar
  folders:

  - title: SectionName # name of the sidebar in the top blue tab
    output: web # leave it as it is
    folderitems:
    - title: Intro to Data Science # name of the first gray-tab redirecting to the landing page
      url: /intro_ds_landing_page.html # url to the landing page for the section. Same name as the markdown file, but with a `.html` extension
      output: web # leave it as it is

    - title: sub-section-01 name in the sidebar
      url: /sub_section-01.html # url to the sub-section-01 file. Same name as the markdown file, but with a `.html` extension
      output: web # leave it as it is

    - title: sub-section-02 name in the sidebar
      url: /sub_section-02.html # url to the sub-section-02 file. Same name as the markdown file, but with a `.html` extension
      output: web # leave it as it is

    # you can add more sub-sections in the same manner
```

You can copy-paste the block of code above to fill into your `.yml` file

### Home sidebar

The home sidebar is the sidebar for the `News` section. To the new section to show up in the `News` sidebar, you have to add a new sub-section at the end of file as.

First open the file in your favorite editor. For instance:

```bash
code ./_data/home_sidebar.yml
```

Then modify the file as:

```yml

# you will see 
  - title: Topics
    output: web
    folderitems:
    - title: News
      url: /news.html
      output: web
    - title: NRT Library Intro
      url: /index.html
      output: web
    - title: Some topic
      url: /someTopic_landing_page.html
      output: web
    # etc ....
    # at the end add
    - title: My new section title
      url: /new_sectionName_landing_page.html # same as makrdown file but with html extension
      output: web
```

You can alter the order in whic topics show up in the News sidebar by rearranging the order in the `foleritems` section.

### Top navigation bar

The `topnav.yml` file controls the contents of the top navigation menu of the site. You need to change this so the new sections shows up in the topics drop-down menu.

First open the file in your favorite editor. For instance:

```bash
code ./topnav.yml
```

Then modify the file as:

```yml

# you will see something like:

#Topnav dropdowns
topnav_dropdowns:
- title: Topnav dropdowns
  folders:
    - title: Topics
      folderitems:
        - title: NRT Library Intro
          url: /index.html
        - title: Some topic title
          url: /someTopic_landing_page.html
          # etc...
          # Then add at the end
        - title: Section title
          url: /new_sectionName_landing_page.html # same as makrdown file but with html extension
```

You can alter the order in whic topics show up in the drop-down menu by rearranging the order in the `folderitems` section.

### Adding tags to sections

Pages can be grouped and searched by tags. Tags are added in the frontmatter (top section on each markdown file) as:

```yml
---
title:  "Section title"
published: true
permalink: page_link.html
summary: "Section summary"
tags: [tag_1, tag_2, new_tag] # here you add tags after the comma
---
```

To prevent arbitrary tags to be created and to get tags to work, you need to do two things:

- To add the tag name to the `./_data/tags.yml` file as:

```yml
# you will see
allowed-tags:
  - getting_started
  - content_types
  - navigation
  # etc...
  # then add at the end
  - my_new_tag
```

- To create a tag file for the new tag in the `./pages/tags/` directory as:

```bash
touch ./pages/tags/my_newTag.md
```

Then open the file and fill in with:

```yml
---
title: "Tag Name"
search: exclude # leave it as it is
tagName: new_tag # this is your new tag name
permalink: my_newTag.html # same as markdown file
sidebar: mydoc_sidebar # leave it as it is
folder: tags # leave it as it is
---
{% include taglogic.html %} # leave it as it is

{% include links.html %} # leave as it is
```

That's all. If the tag does not show up or work after saving, close the browser, kill the process and rebuild the site.

### Config file
