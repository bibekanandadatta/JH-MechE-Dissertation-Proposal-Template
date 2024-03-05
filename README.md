# JHU Mechanical Engineering Dissertation Proposal Template

This is an unofficial LaTeX template for dissertation proposal in PhD in Mechanical Engineering program at Johns Hopkins University. The program does not require any specific formatting, but only provides some general guidelines on the sections to be included in the proposal.

**It is user's responsibility to discuss with their advisor and committee members about the formatting.**

This repository is also available as [Overleaf template](https://www.overleaf.com/latex/templates/johns-hopkins-meche-dissertation-proposal-template/ppqmcfvvpzsx).


## Description of the repository

- `main.tex`: This is main file based on LaTeX article class in which you will write your proposal. This single file has all the packages, their settings, customized macros, and the main text section.
- `rebuttal.tex`: This is a plain article class file which you can use to prepare your response to committee members in case they make suggestions to your proposal. I hope you do not have to do this. Anyway, this is a general-purposed article class based .tex file which can be used for writing small report or even reponse to journal or conference artlce peer review.
- `references.bib`: This is a biblatex file which contains all the bibliographic item. Use Zotero or some other citation manager to generate the biblatex file with all the citations. I recommend adding all the citation files (for main proposal and subsequent rebuttal) to one single file that means update the same file when writing rebuttal to avoid clutter.
- `figures.pdf`: This pdf file contains all the figures for your proposal. In case you do not have all figures compiled in a single file, you can add multiple figure files as well in the main project directory. If you prefer to add a subdirectory for the figures, then you will have to specify `\graphicspath{}` in the preamble of the document.


## How to use the template on Overleaf

I prefer using Overleaf for all of my LaTeX compilation and I recommend it storngly since Johns Hopkins provides premium account to all students for Overleaf. Premium Overleaf does fast compilation, allows sharing the project with multiple people (advisor, committee members, collaborator, labmates, friends, or family), keep track history which is great. You can recover file if you break it (hopefully you won't). Follow one of the three approaches to get started with this project on Overleaf.

- To use it directly on Overleaf, [open the template here](https://www.overleaf.com/latex/templates/johns-hopkins-meche-dissertation-proposal-template/ppqmcfvvpzsx). Then click on **Open as Template** and proceed from there to go through the template and edit it.

- If the overleaf version is outdated for some reason (Overleaf takes a bit of time to update the templates), then you can download / clone this repository from GitHub, then compress it as a zip file. Go to Overleaf, Click on **New Project** -> **Upload Project**, then upload the zipped folder. Continue...
  
- If you have your Overleaf and GitHub account linked and want to have copies of the project in both places, you can **fork** this repository. Then go to Overleaf, Click on **New Project** -> **Import from GitHub**, it should list the forked project for listing. Once imported, you can start working... But Overleaf and GitHub will not sync automatically; you will have to do it.

Once the project is opened, for main proposal, compile `proposal.tex` and rebuttal compile `rebuttal.tex`. These files should compile separately without any errors; there might be warnings but you can ignore them.


**PS:** I stopped using local LaTeX compiler for a while now. If you would like to do it locally, you should a have LaTeX compiler installed and configured with multiple packages with a decent text editor. Unfortunately I did not try compiling this project locally, so will not be able to help out!


## Some useful suggestions for using the template




## Contributing to the project

This template was kept sufficiently general purpose for  with some customization examples for special packages or macros for demonstration purpose. Since there exists any specific requirements related to dissertation proposal, I do not plan on updating this repository frequently. But if any package becomes obsolete or you have better ideas to implement something, you can create a fork and make a `pull request`, or just let me know.
