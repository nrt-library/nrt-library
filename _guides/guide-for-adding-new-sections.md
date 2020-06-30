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

### New section contents

The content that will be displayed in the website for new section must be created in the `pages/` directoy. You first need to create a new directory with the name of your new-section, to then add the Markdown files with the actual section contents. There are two types of Markdown files you need to create: (1) a **landing-page** file, which is the page people will see when first landing on the section, and (2) Markdown files with the **sub-section contents**.

In the terminal, this can be done as:

**NOTE**: from now on I will assumme you work in the terminal under the `nrt-library/` base directory. This allows me to use relative paths, such that you can copy-paste and things work in your terminal.  

```bash
# make sure you are in the nrt-library/ base directory
pwd # in Mac/Linux
cd # in Windows Command Prompt

# make new directory
mkdir ./pages/my_new_section

# create landing-page file
touch ./pages/my_new_section/my_sectionName_landing_page.md # in Linux/Mac
call >> ./pages/my_new_section/my_sectionName_landing_page.md # in Windows Command Prompt

# create subsection 01 file
touch ./pages/my-new-section/my_subsectionName_01.md # in Linux/Windows
call >> ./pages/my-new-section/my_subsectionName_01.md  # in Windows Command Prompt

# create subsection 02 file
touch ./pages/my_new_section/my_subsectionName_02.md # in Linux/Windows
call >> ./pages/my_new_section/my_subsectionName_02.md # in Windows Command Prompt

# create as many subsections as you need
```

Section contents are simply Markdown files. The `html` file diplayed in the website will be automatically generate in the `_site` folder. The content of your Markdown files won't render just yet. A **frontmatter** section is needed at the top.

## Markdown Frontmatter

For the Markdown files to be displayed in the website, you have to add a **frontmatter** at the top of each Markdown file as:

```yml
# For the landing page
---
title: Title New Section
tags: [tag1, tag2] # assuming the tag exist. More on than latter
keywords: "topic" # new keywords requiere to create a new tag file
last_updated: "June 17, 2020" # current date
summary: "Summary of the new section"
published: true
sidebar: my_sectionNAme_sidebar # name of yml sidebar file withouth extension
permalink: my_sectionName_landing_page.html # Markdown file name with a html extension
folder: my_new_section # folder where Markdown files are saved
---

Here goes some regular Mardown text
```

Below the frontmatter you can add the Markdown content as you would normally do. Subsections follow the same structure: fontmatter and then Markdown text. Just change the content of the fields in the fontmatter to match the subsection. Be sure the permalink match the subsection Markdown filename.

### Section sidebar

Each section requieres a sidebar menu to be navigated. Sidebar are `.yml` files in the `_data/sidebars` directory.

In the terminal you can type:

```bash
# make sure you are in the nrt-library/ base directory
pwd # in Mac/Linux
cd # in Windows Command Prompt

# create section sidebar .yml file
touch ./_data/sidebars/my_sectionNAme_sidebar.yml # in Mac/Linux
call >> ./_data/sidebars/my_sectionNAme_sidebar.yml # in Windows Command Prompt
```

Sidebars `.yml` file have the following structure:

```yml
entries:
- title: Sidebar # leave this as it is
  product: My # this is the first part of title at the top of the sidebar
  version: Section # this is the second part of title at the top of the sidebar
  folders:

  - title: My Section Name # name of the sidebar in the top blue tab
    output: web # leave it as it is
    folderitems:
    - title: My Section # name of the first gray-tab redirecting to the landing page
      url: /my_sectionName_landing_page.html # url to the landing page for the section. Same name as the Markdown file, but with a `.html` extension
      output: web # leave it as it is

    - title: Subsection 01 name in the sidebar
      url: /my_subsectionName_01.html # url to the sub-section-01 file. Same name as the Markdown file, but with a `.html` extension
      output: web # leave it as it is

    - title: Subsection 02 name in the sidebar
      url: /my_subsectionName_02.html # url to the sub-section-02 file. Same name as the Markdown file, but with a `.html` extension
      output: web # leave it as it is

    # you can add more sub-sections in the same manner
```

You can copy-paste the block of code above to fill into your `.yml` file as a template, and then modify for your new content.

### Home sidebar

The home sidebar is the sidebar for the `News` section. To the new section to show up in the `News` sidebar, you have to add a new sub-section at the end of the file.

First open the file in your favorite editor. For instance:

```bash
code ./_data/home_sidebar.yml
```

Then modify the file as:

```yml

# you will see something like:
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
    - title: My new section name
      url: /my_sectionName_landing_page.html # same as makrdown file but with html extension
      output: web
```

You can alter the order in which topics show up in the `News` sidebar by rearranging the order in the `folderitems` section.

### Top navigation bar

The `topnav.yml` file controls the contents of the top navigation menu of the site. You need to change this so the new sections shows up in the topics drop-down menu.

First open the file in your favorite editor. For instance:

```bash
code ./_data/topnav.yml
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
        - title: My Section Title
          url: /my_sectionName_landing_page.html # same as makrdown file but with html extension
```

You can alter the order in whic topics show up in the drop-down menu by rearranging the order in the `folderitems` section.

### Adding tags to sections

Pages can be grouped and searched by **tags**. Tags are added in the frontmatter (top section in each Markdown file) as:

```yml
---
title:  "My Section Title"
published: true
permalink: my_sectionName_landing_page.html
summary: "My Section Summary"
tags: [tag_1, tag_2, new_tag] # here you add tags separated by commas
---
```

To prevent arbitrary tags to be created and to get tags to work, you need to do two things:

- To add the tag name to the `./_data/tags.yml` file as:

```yml
# you will see something like:
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
touch ./pages/tags/my_newTag.md # in Linux/MAc
call >> ./pages/tags/my_newTag.md # in Windows Command Prompt
```

Then open the file and fill in with:

```yml
---
title: "Tag Name"
search: exclude # leave it as it is
tagName: new_tag # this is your new tag name
permalink: my_newTag.html # same as Markdown file
sidebar: mydoc_sidebar # leave it as it is
folder: tags # leave it as it is
---
{% include taglogic.html %} # leave it as it is

{% include links.html %} # leave as it is
```

That's all. If the tag does not show up or work after saving, close the browser, kill the process and rebuild the site.
