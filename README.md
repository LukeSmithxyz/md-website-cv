# Luke's Markdown/LaTeX/pdf CV/Website

This is just a little experiment that I might implement for my own website and CV. Here's what I wanted:

+ Simplification: I don't have to update both my CV and website differently.
+ Printability: My website should have a printable, handout-able counterpart for personal info (CV) and other writings.
+ Automatic formatting: I want to be able to change the structure, and all the formatting, the nav bar and sections, should be natural.

## This is the solution

It's simple. There's one markdown file `index.md`, which has *all* of my personal information and details in nice litte sections and subsections.

I use a makefile to compile it into a LaTeX .pdf and an HTML file via pandoc.

For the HTML conversion I use a CSS stylesheet (`style.css`) which:

+ Gives a custom background and div settings for the content area.
+ Creates a "table of contents" from the section headings and converts that into a menu bar where the subsections drop down.
+ Hides some longer content away to reappear on mouseover.

For the LaTeX/pdf conversion, I use a pandoc LaTeX template file with some custom settings as well.
These are located in the `template.tex` file.

## Use

Make changes to the markdown file `index.md`. Run `make` (or `make compile`) and it will produce a .pdf and .html.

## Dependencies

pandoc, LaTeX, and if you want to use the makefile, make (you can copy the commands and run them manually if you want).
