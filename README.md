# JHU Mechanical Engineering Dissertation Proposal Template

This is an unofficial LaTeX template for dissertation proposal in PhD in Mechanical Engineering program at Johns Hopkins University. The program does not require any specific formatting, but only provides some general guidelines on the sections with a tentative page limit to be included in the proposal. This template is created based on those general guidelines. The repository is also available as [Overleaf template](https://www.overleaf.com/latex/templates/johns-hopkins-meche-dissertation-proposal-template/ppqmcfvvpzsx).

**It is user's responsibility to discuss with their advisor(s) and committee members about the formatting. The author of this repository bears no responsibility regarding this.**




## Description of the repository

- `main.tex`: This is main file based on LaTeX article class in which you will write your proposal. This single file has all the packages, their settings, customized macros, and the main text section.
- `rebuttal.tex`: This is a plain article class file which you can use to prepare your response to committee members in case they make suggestions to your proposal. I hope you do not have to do this. Anyway, this is a general-purposed article class based .tex file which can be used for writing small report or even reponse to journal or conference artlce peer review.
- `references.bib`: This is a biblatex file which contains all the bibliographic item. Use Zotero or some other citation manager to generate the biblatex file with all the citations. I recommend adding all the citation files (for main proposal and subsequent rebuttal) to one single file that means update the same file when writing rebuttal to avoid clutter.
- `figures.pdf`: This pdf file contains all the figures for your proposal. In case you do not have all figures compiled in a single file, you can add multiple figure files as well in the main project directory. If you prefer to add a subdirectory for the figures, then you will have to specify `\graphicspath{}` in the preamble of the document.

I suggest going though both of the .tex files to see what packages have been included and what options are invoked to obtain the current formatting. You can the tweak the options or add more packages to format it your preference or domain-specific requirement.



## How to use the template on Overleaf

I prefer using Overleaf for all of my LaTeX compilation and I recommend it storngly since Johns Hopkins provides premium account to all students for Overleaf. Premium Overleaf does fast compilation, allows sharing the project with multiple people (advisor, committee members, collaborator, labmates, friends, or family), keep track history which is great. You can recover file if you break it (hopefully you won't). Follow one of the three approaches to get started with this project on Overleaf.

- To use it directly on Overleaf, [open the template here](https://www.overleaf.com/latex/templates/johns-hopkins-meche-dissertation-proposal-template/ppqmcfvvpzsx). Then click on **Open as Template** and proceed from there to go through the template and edit it.

- If the overleaf version is outdated for some reason (Overleaf takes a bit of time to update the templates), then you can download / clone this repository from GitHub, then compress it as a zip file. Go to Overleaf, Click on **New Project** -> **Upload Project**, then upload the zipped folder. Continue...
  
- If you have your Overleaf and GitHub account linked and want to have copies of the project in both places, you can **fork** this repository. Then go to Overleaf, Click on **New Project** -> **Import from GitHub**, it should list the forked project for listing. Once imported, you can start working... But Overleaf and GitHub will not sync automatically; you will have to do it.

Once the project is opened, for main proposal, compile `proposal.tex` and rebuttal compile `rebuttal.tex`. These files should compile separately without any errors; there might be warnings but you can ignore them.


**PS:** I stopped using local LaTeX compiler for a while now. If you would like to do it locally, you should a have LaTeX compiler installed and configured with multiple packages with a decent text editor. Unfortunately I did not try compiling this project locally, so will not be able to help out!



## Current formatting and suggestions

Format of the dissertation proposal document is inspired by the [thesis/ dissertation formatting provided by the Johns Hopkins Sheridan Library](https://www.library.jhu.edu/library-services/electronic-theses-dissertations/formatting-requirements/). However, because of the page limit and difference in the style of contents, it was heavily customized.

- The title page is customized to my preference inspired by Johns Hopkins dissertation template. If you have more than two committee members besides your advisor or have multiple advisors/ co-advisors, you may need to use `minipage` environment to fit the full committee in the title page.

- Tha main text of the both documents are single-spaced with listed front matter being one-half-spaced for the main.tex because of the page limitation. But you can space out the content if you prefer by using `\onehalfspacing` or `\doublespacing` instead of `\singlespacing` for the main text. Change other spacing accordingly. All the necessary variables that can customize the format of the template are declared in the very beginning of the document. Tweak them to obtain a more consistent format for Table, Figures, Paragraph, and Bibliographic items, etc.

- Margin used in both documents are 1.0in for all sides with no header and footer except for pagination at bottom center.

- The title page of the main proposal document does not have any pagination. For the main proposal document, the pagination counter starts from the abstract page with Roman numeral ii. For main text in the proposal document, the pagination resets in Arabic starting from 1. For the response document, the pagination is always is in Arabic from the beginning.

- There is no specific title page for the response document. Rather it uses standard `authblk` packagee to have a title, author name, and author affiliation.

- Table of contents, List of figures, List of tables are considered to be unnumbered sections in this template. `tocbasic` package was used to manage this formatting. Every section (numbered or unnumbered) is followed by a `\titlerule`. If you do not like the appearance of it, you can delete it to make it appear a little bit more cleaner and less distracting.

- Currently, the biblatex package is used with `nature` citation style (numbered). You may need to change it based on your research field such as IEEE, APA, or something else. While I prefer author-year format (such as APA) in most cases, but for this page-limited proposal document, I found numbered-style citation to be more appropriate and space saving.

- For the response document, the questions or suggestions from the committee members are written in a different color than the actual response to distinguish. `xcolor` package with `dvipsnames` option was used for this. You can change the color to your preference.

- For each committee member, a specific section is dedicated in the response document and questions are posed using a enumerated list.



## Contributing to the project

This template was kept sufficiently general purpose for with some customization examples for special packages or macros for demonstration purpose. Since there is no specific formatting requirements available, I do not plan on actively maintaining this repository. But if you have questions, I would be happy to help! Also, if any package becomes obsolete or you have better ideas to implement something, you can create a fork and make a `pull request`, or just let me know.
