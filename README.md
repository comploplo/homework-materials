# Homework template

The files in repository are meant to be used with Markdown and Pandoc to produce beautiful looking
homework assignments. The files imported in homework.tex are meant for linguistics homework, but
may easily be changed to support other kinds of documents based on user needs.

This repository is meant to be used with gnu's [stow](https://www.gnu.org/software/stow/) utility,
specifically with the command `stow -S homework-materials`, which creates symlinks between this
repository's files and the home folder. The file structure in this repository reflects that which
must be in your home directory for the template, and pandoc, to work.

The texmf directory contains files from [the kaobook template](https://www.latextemplates.com/template/kaobook)
, which is a variation on the [Tufte handout template](https://rstudio.github.io/tufte/), texmf's 
structure may be better understood [here](www.texdoc.net/texmf-dist/doc/generic/tds/tds.pdf). 

Dependencies: stow, some latex packages, pandoc.
Tested only on Linux systems.

Once symlinks are in place and dependencies are installed, the template may be used to compile
markdown files to pdf with the following command: `pandoc path-to-file.md -o path-to-output.pdf --template homework.tex`.

The template has the following inputs, which may be a part of the yaml preamble on input markdown 
files, but have defaults if they are not addressed. The homeworkProblem enviroment cannot be used
with markdown's # based header system, but will number your homework problems automatically if 
used.

date: defaults to \today.

title: defaults to assignment.

assignment: defaults to 'assignment hmm'.

classname: defaults to 'Your Class'.

problemtitle: defaults to 'Exercise', prefix on homeworkProblem enviroment. 

author: defaults to 'Gabe Oppenheimer'.

numbersecitons: defaults to non-numbered sections, toggle numbered sections.
