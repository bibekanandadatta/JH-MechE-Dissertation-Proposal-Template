# JHU Mechanical Engineering Dissertation Proposal Template

This is an unofficial LaTeX template for dissertation proposal in PhD in Mechanical Engineering program at Johns Hopkins University. The program does not require any specific formatting, but only provides some general guidelines on the sections with a tentative page limit to be included in the proposal. This template is created based on those general guidelines. The repository is also available as [Overleaf template](https://www.overleaf.com/latex/templates/johns-hopkins-meche-dissertation-proposal-template/ppqmcfvvpzsx). However, GitHub is likely to have the most updated repository. See below on how to use this repository on Overleaf.

**It is user's responsibility to discuss with their advisor(s) and committee members about the formatting. The author of this repository bears no responsibility regarding this.**



## Description of the repository

- `main.tex`: This is main file based on LaTeX article class in which you will write your proposal. This single file has all the packages, their settings, customized macros, and the main text section.
- `rebuttal.tex`: This is a plain article class file which you can use to prepare your response to committee members in case they make suggestions to your proposal. I hope you do not have to do this. Anyway, this is a general-purposed article class based .tex file which can be used for writing small report or even reponse to journal or conference artlce peer review.
- `references.bib`: This is a biblatex file which contains all the bibliographic item. Use Zotero or some other citation manager to generate the biblatex file with all the citations. I recommend adding all the citation files (for main proposal and subsequent rebuttal) to one single file that means update the same file when writing rebuttal to avoid clutter.
- `figures.pdf`: This pdf file contains all the figures for your proposal. In case you do not have all figures compiled in a single file, you can add multiple figure files as well in the main project directory. If you prefer to add a subdirectory for the figures, then you will have to specify `\graphicspath{}` in the preamble of the document.
- `README.md` is this file containing all the details related to the template.

I suggest going though both of the .tex files to see what packages have been included and what options are invoked to obtain the current formatting. You can the tweak the options or add more packages to format it your preference or field-specific requirement.



## How to use the template on Overleaf

I prefer using Overleaf for all of my LaTeX compilation and I recommend it storngly since Johns Hopkins provides premium account to all students for Overleaf. Premium Overleaf does fast compilation, allows sharing the project with multiple people (advisor, committee members, collaborator, labmates, friends, or family), keep track history which is great. You can recover file if you break it (hopefully you won't). Follow one of the three approaches to get started with this project on Overleaf.

- To use it directly on Overleaf, [open the template here](https://www.overleaf.com/latex/templates/johns-hopkins-meche-dissertation-proposal-template/ppqmcfvvpzsx). Then click on **Open as Template** and proceed from there to go through the template and edit it.

- If the overleaf version is outdated for some reason (Overleaf takes a bit of time to update the templates), then you can download / clone this repository from GitHub, then compress it as a zip file. Go to Overleaf, Click on **New Project** -> **Upload Project**, then upload the zipped folder. Continue...
  
- If you have your Overleaf and GitHub account linked and want to have copies of the project in both places, you can **fork** this repository. Then go to Overleaf, Click on **New Project** -> **Import from GitHub**, it should list the forked project for listing. Once imported, you can start working... But Overleaf and GitHub will not sync automatically; you will have to do it.

Once the project is opened, for main proposal document, compile `proposal.tex` and the response to the committee document compile `rebuttal.tex`. These files should compile separately without any errors; there might be warnings but you can ignore them.

**PS:** I stopped using local LaTeX compiler for a while now. If you would like to do it locally, you should a have LaTeX compiler installed and configured with multiple packages with a decent text editor. Unfortunately I did not try compiling this project locally, so will not be able to help out if you run into issues!



## Format of the proposal documents and suggestions on using the template

Overleaf has a huge collection of tutorials and examples on different LaTeX-related typesetting topics (margins and page size, math, table, footnote, bibliography management). You will most likely to find what you need there. Two other useful sources to find answer to any questions are StackExchange and StackOverflow. 

- The title page of the main proposal document is inspired by [thesis/ dissertation formatting provided by the Johns Hopkins Sheridan Library](https://www.library.jhu.edu/library-services/electronic-theses-dissertations/formatting-requirements/) but it was customized to my preference. If you have more than two committee members besides your advisor or have multiple advisors/ co-advisors, you may need to use `minipage` environment to fit the full committee in the title page. Or you may change the style of it entirely to fit to your necessity.
  - There is no specific title page for the response document. Rather it uses standard `authblk` package to manage document title, author name, and author affiliation.

- The title page of the main proposal document does not have any pagination. For the main proposal document, the pagination counter starts from the abstract page with Roman numeral ii. For main text in the proposal document, the pagination resets in Arabic starting from 1. For the response document, the pagination is always is in Arabic from the beginning.

- Most of the necessary variables to manage the formatting of the document has been declared in the beginning of the `.tex` files. If you prefer cutosmizing the format, you will likely to find the necessary variable there. But you are welcome to add more variables and settings in the document to your preference or need.
  
- Add your bibliographic file to the main directory and make sure to change the name of your bibliographic file or the variable related to it. Make sure your bibliography file is in biblatex format; use Zotero or some other citation manage to generate the biblatex file.

- Add all of your figures to the main directory. You can also add the figures to a specfic subdirectory if you would like. In that case, you will have to define the subdirectory in `\includegraphicspath{}` command.

- Most common and popular packages for writing dissertations are added in the `LaTeX Class and Package` sections. Check the packages; add any additional package you need and/or customize your options there.

- Margin used in both documents are **1.0in** for all sides with no header and footer except for the pagination at bottom center inside the margin. If you would like to change it, then look for `\geometry{}` command inside the `Document Formatting` section.

- I used `Latin Modern Roman` font for the document as it produces consistent typography for text and math environment. If you prefer, you can use some other font by loading that package using `\usepackage{}` command. However, you will have to be careful about the consistency of the typpgraphy, specially between text and math environment.

- Tha main text of the both documents are **single-spaced** with table of contents, list of figures, list of table being **one-half-spaced** in `main.tex`. If you find this too tightly-spaced, you can space out the content by using `\onehalfspacing` or `\doublespacing` instead of `\singlespacing` for the main text in both .tex files. In this case, you will have to change the spacing for other environments as well to have a consistently-formatted document. Most of the necessary variables that can customize the format of the template are declared in the very beginning of the .tex files. Tweak them to obtain a more consistent formatting for the tables, figures, paragraphs, and bibliographic items, etc. You are welcome to define more customized settings as well.

- Currently, the biblatex package is used with `nature` citation style (numbered). You may need to change it based on your research field such as IEEE, APA, or something else. While I prefer author-year format (such as APA) in most cases, but I found numbered-style citation to be more appropriate because of the page limitation. If you would like to change or customize it, look for the command where `biblatex` package is loaded in the `LaTeX Class and Package` section.

- Table of contents, List of figures, List of tables are considered to be unnumbered sections in this template. `tocbasic` package was used to manage this formatting. Every section (numbered or unnumbered) is followed by a `\titlerule`. If you do not like the appearance of it, you can delete it to make it appear a little bit more cleaner and less distracting. Check the `Document Formatting` section in the `main.tex` file.

- I used unnumbered `subsection*` and `subsubsection*` environment in the main proposal document to avoid confusion with the numbering scheme of my objectives, tasks, subtasks. However, to add them in the table of contents, I placed `\phantomsection` and `\addcontentsline` command before and after (respectively) declaring the environments. If you would like, you can change it to standard numbered section and subsection.

- Add your math macros and settings in the `Math Settings and Macros` section. There's a section for non-math LaTeX macros as well. Some examples of both types of macros are added there.

- You can use `\linenumbers` command from `lineno` package anywhere inside the main text document when you would like to have line numbers on the left margin. It might be useful during the drafting stage.

- If you find all the packages and their settings and macros to be overwhelming and distracting during the editing process, you can cut and paste all these contents to a separate `settings.tex` file (name it as you like) in the project directory. Then you can use the command `input{settings.tex}` to make your main file appear cleaner and less distracting. `\input{}` command literally pastes content from the source file. See [managing large project on Overleaf](https://www.overleaf.com/learn/latex/Management_in_a_large_project).

- Finally, you may consider using `microtype` package to have a better typography of your document. Check details on using [`microtype` package for writing thesis here](https://www.khirevich.com/latex/microtype/).

- For the response document, the questions or suggestions from the committee members are written in a different color than the actual response to distinguish. `xcolor` package with `dvipsnames` option was used for this. You can change the color to your preference. Additionally, for each committee member, a specific section is dedicated in the response document, and the questions are posed as an enumerated list.

- Keep writing ... and good luck :tada:!


## Contributing to the project

This template was kept sufficiently general purpose for with some customization examples for special packages or macros for demonstration purpose. Since there is no specific formatting requirements available, I do not plan on actively maintaining this repository. But if you have questions, I would be happy to help! Also, if any package becomes obsolete or you have better ideas to implement something, you can create a fork and make a `pull request`, or just let me know.
