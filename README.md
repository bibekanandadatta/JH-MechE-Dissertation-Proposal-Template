# JHU Mechanical Engineering Dissertation Proposal Template

This is an unofficial LaTeX template for the dissertation proposal in PhD in Mechanical Engineering program at Johns Hopkins University. The program does not require any specific formatting but only provides some general guidelines on the sections with a tentative page limit to be included in the proposal. This template is created based on those general guidelines. The repository is also available as [Overleaf template](https://www.overleaf.com/latex/templates/johns-hopkins-meche-dissertation-proposal-template/ppqmcfvvpzsx). However, GitHub is likely to have the most updated repository. See below for how to use this repository on Overleaf.

**It is the user's responsibility to discuss with their advisor(s) and committee members about the formatting. The author of this repository bears no responsibility regarding this.**



## Description of the repository

- `main.tex`: This is the main file based on the LaTeX article class in which you will write your proposal. This single file has all the packages, their settings, customized macros, and the main text section.
- `rebuttal.tex`: This is a plain article class file that you can use to prepare your response to committee members in case they make suggestions for your proposal. I hope you do not have to do this. Anyway, this is a general-purpose article class-based .tex file that can be used for writing small reports or even responses to journal or conference article peer reviews.
- `references.bib`: This is a biblatex file that contains all the bibliographic items. Use Zotero or some other citation manager to generate the biblatex file with all the citations. I recommend adding all the citation files (for the main proposal and subsequent rebuttal) to one single file which means updating the same file when writing a rebuttal to avoid clutter.
- `figures.pdf`: This pdf file contains all the figures for your proposal. In case you do not have all figures compiled in a single file, you can add multiple figure files as well in the main project directory. If you prefer to add a subdirectory for the figures, then you will have to specify `\graphicspath{}` in the preamble of the document.
- `README.md` is this file containing all the details related to the template.

I suggest going through both of the .tex files to see what packages have been included and what options are invoked to obtain the current formatting. The structure of the .tex files are almost identical except for a few minor changes to serve separate purposes. You can tweak the options or add more packages to format the document to your preference or field-specific requirements.



## How to use the template on Overleaf

I prefer using Overleaf for all of my LaTeX compilation and I recommend it strongly since Johns Hopkins provides the premium account to all students for Overleaf. Premium Overleaf does fast compilation, allows sharing the project with multiple people (advisor, committee members, collaborator, labmates, friends, or family), and tracks history. You can recover files if you break them (hopefully you won't). Follow one of the three approaches to get started with this project on Overleaf.

- To use it directly on Overleaf, [open the template here](https://www.overleaf.com/latex/templates/johns-hopkins-meche-dissertation-proposal-template/ppqmcfvvpzsx). Then click on **Open as Template** and proceed from there to go through the template and edit it.

- If the Overleaf version is outdated for some reason (Overleaf takes a bit of time to update the templates), then you can download/clone this repository from GitHub, and compress it as a zip file. Go to Overleaf, Click on **New Project** -> **Upload Project**, then upload the zipped folder. Continue...
  
- If you have your Overleaf and GitHub account linked and want to have copies of the project in both places, you can **fork** this repository. Then go to Overleaf and click on **New Project** -> **Import from GitHub**, it should list the forked project for listing. Once imported, you can start working... But Overleaf and GitHub will not sync automatically; you will have to do it.

Once the project is opened, for the main proposal document, compile `proposal.tex` and for the response to the committee document, compile `rebuttal.tex`. You will have to compile them separately. These files should compile separately without any errors; there might be warnings but you can ignore them. In your first submission to thesis proposal committee, response text should not be necessary. During resubmission (if your committee members require you to do so), compile them separately and if you need to submit them as one document, just merge them using Preview app on macOS or online PDF tools.

**PS:** I stopped using the local LaTeX compiler for a while now. If you would like to do it locally, you should a have LaTeX compiler installed and configured with multiple packages with a decent text editor. Unfortunately, I did not try compiling this project locally, so will not be able to help out if you run into issues!



## Format of the proposal documents and suggestions on using the template

Overleaf has a huge collection of tutorials and examples on different LaTeX-related typesetting topics (margins and page size, math, table, footnote, and bibliography management). You will most likely find what you need there. Two other useful sources to find answers to any questions are StackExchange and StackOverflow. 

- The title page of the main proposal document is inspired by [thesis/ dissertation formatting provided by the Johns Hopkins Sheridan Library](https://www.library.jhu.edu/library-services/electronic-theses-dissertations/formatting-requirements/) but it was customized to my preference since there is no specific guideline to it. If you have more than two committee members besides your advisor or have multiple advisors/ co-advisors, you may need to use the `minipage` environment to fit the full committee on the title page. Or you may change the style of it entirely to fit your necessity.
  - There is no specific title page for the response document. Rather it uses the standard `authblk` package to manage document title, author name, and author affiliation.

- The title page of the main proposal document does not have any pagination. For the main proposal document, the pagination counter starts from the abstract page with the Roman numeral ii. For the main text in the proposal document, the pagination resets in Arabic starting from 1. For the response document, the pagination is always in Arabic from the beginning.

- Most of the necessary variables to manage the formatting of the document have been declared at the beginning of the `.tex` files. If you prefer customizing the format, you will likely find the necessary variable there. But you are welcome to add more variables and settings in the document to your preference or need.
  
- Add your bibliographic file to the main directory and make sure to change the name of your bibliographic file or the variable related to it. Make sure your bibliography file is in biblatex format; use Zotero or some other citation manager to generate the biblatex file.

- Add all of your figures to the main directory. You can also add the figures to a specific subdirectory if you would like. In that case, you will have to define the subdirectory in `\includegraphicspath{}` command.

The most common and popular packages for writing the dissertation proposal and response are added in the `LaTeX CLASS AND PACKAGES` sections. Check the packages; add any additional package you need and/or customize your options there.

The margin used in both documents is **1.0in** for all sides with no header and footer except for the pagination at the bottom center inside the margin. If you would like to change it, then look for the `\geometry{}` command inside the `DOCUMENT FORMATTING` section.

- I used Latin Modern Roman font (loaded using the `lmodern` package) for the document as it produces consistent typography for text and math environment. If you prefer, you can use some other font by loading that package using the `\usepackage{}` command. However, you will have to be careful about the consistency of the typography, especially between text and math environments. [Follow this discussion on StackExchange to learn more about fonts in LaTeX](https://tex.stackexchange.com/questions/59702/suggest-a-nice-font-family-for-my-basic-latex-template-text-and-math).

- The main text sections of both documents are **single-spaced** except the table of contents, list of figures, and list of tables being **one-half-spaced** in `main.tex`. If you find the main text is too tightly spaced, you can space out the content by using `\onehalfspacing` or `\doublespacing` instead of `\singlespacing` for the main text in both .tex files. In this case, you will have to change the spacing for other environments as well to have a consistently formatted document. Most of the necessary variables that can customize the format of the template are declared at the very beginning of the .tex files. Tweak them to obtain more consistent formatting for the tables, figures, paragraphs, bibliographic items, etc. You are welcome to define more customized preamble settings as well.

  - In case you change text spacing, you most likely would need to change the spacing around the headings of different environments that are managed by the `parskip` package. I found the default settings to be working fine for me. But if you would like to customize it, you can add the following command in the preamble:
  ```
  \titlespacing*{<environment-name>}{<space-left>}{<space-before>}{<space-after>}
  ```

- Currently, the biblatex package is used with the `nature` citation style (numbered). You may need to change it based on your research field such as IEEE, APA, or something else. While I prefer author-year format (such as APA) in most cases, I found numbered-style citations to be more appropriate because of the page limitation. If you would like to change or customize it, look for the command where the `biblatex` package is loaded in the `LaTeX CLASS AND PACKAGES` section.

- The table of contents (ToC), list of figures (LoF), and list of tables (LoT) are considered to be equivalent to unnumbered sections in this template. The `tocloft` package was used to manage this typesetting for the title. If you do not want any or one of these items to appear in your document to keep the document concise, you can comment out or delete the relevant commands in the `FRONT MATTER` section of the `main.tex` file.

- Every section (numbered or unnumbered) is followed by a `\titlerule`. If you do not like the appearance of it, you can delete it to make it appear a little bit more cleaner and less distracting. Check the `DOCUMENT FORMATTING` section in the `main.tex` file.
  - However, the `\hrule` command is added to the ToC, LoF, and LoT in the front matter section of the `main.tex` file manually. If you would like to remove them, look into the `FRONT MATTER` section in the `main.tex` file.

- I used the unnumbered `subsection*` and `subsubsection*` environment in the main proposal document to avoid confusion with the numbering scheme of my objectives, tasks, and subtasks. However, to add them to the table of contents, I placed the `\phantomsection` and `\addcontentsline` commands before and after (respectively) declaring the environments. If you would like, you can change it to a standard numbered section and subsection, use the default `\subsection` and `\subsubsection` commands.

- Add your math macros and settings in the `MATH SETTINGS AND MACROS` section. There's a section for non-math LaTeX macros as well. Some examples of both types of macros are added there.

- You can use the `\linenumbers` command from the `lineno` (already loaded) package anywhere inside the main text document when you would like to have line numbers on the left margin. It might be useful during the drafting stage.

- If you find all the packages and their settings and macros to be overwhelming and distracting during the editing process, you can cut and paste all these contents to a separate `my-preamble.tex` file (name it as you like) in the project directory. Then you can use the command `input{my-preamble.tex}` to make your main file appear cleaner and less distracting. `\input{}` command pastes content from the source file. See [managing the large project on Overleaf](https://www.overleaf.com/learn/latex/Management_in_a_large_project).

- Finally, you may consider using the `microtype` package to have a better typography of your document. Check details on using [microtype package for writing a thesis here](https://www.khirevich.com/latex/microtype/).

- All of these suggestions also apply to the `rebuttal.tex` file. In the response document, for each committee member, a specific section is dedicated, and the questions are posed as an enumerated list. Additionally, questions or suggestions are written in a different color `(royalblue)` than the actual response using the `xcolor` package with the `dvipsnames` option. You can change the color to your preference. You can use this package to add colors in other cases as well; check on [using colors in LaTeX on Overleaf](https://www.overleaf.com/learn/latex/Using_colors_in_LaTeX).

- Keep writing ... and good luck :tada:!


## Contributing to the project

This template was kept sufficiently general purpose for with some customization examples for special packages or macros for demonstration purposes. Since there are no specific formatting requirements available, I do not plan on actively maintaining this repository. But if you have questions, I would be happy to help! Also, if any package becomes obsolete or you have better ideas to implement something, you can create a fork and make a `pull request`, or just let me know.
