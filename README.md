# JHU Mechanical Engineering Dissertation Proposal Template

This is an unofficial LaTeX template for the dissertation proposal in PhD in Mechanical Engineering program at Johns Hopkins University. The program does not require any specific formatting, however, provides some general guidelines on the sections with a suggested page limit to be included in the proposal. This template is created based on those general guidelines. The repository is also available as [Overleaf template](https://www.overleaf.com/latex/templates/johns-hopkins-meche-dissertation-proposal-template/ppqmcfvvpzsx). However, GitHub is likely to have the most updated repository. See below for how to use this repository on Overleaf.

**It is the user's responsibility to discuss with their advisor(s) and committee members about the formatting and styles of the proposal.**



## Description of the repository

- `01-main.tex`: This is the main file based on the LaTeX article class in which you will write your proposal. This single file has all the packages, their settings, customized macros, and the main text section.
- `02-response.tex`: This is a plain article class file that you can use to prepare your response to committee members in case they make suggestions for your proposal. I hope you do not have to do this. Anyway, this is a general-purpose article class-based .tex file that can be used for writing small reports or even responses to journal or conference article peer reviews.
- `references.bib`: This is a biblatex file that contains all the bibliographic items. Use Zotero or some other citation manager to generate the biblatex file with all the citations. I recommend adding all the citation files (for the main proposal and subsequent response) to one single file which means updating the same file when writing the response to avoid clutter.
- `figures.pdf`: This pdf file contains all the figures for your proposal. In case you do not have all figures compiled in a single file, you can add multiple figure files as well in the main project directory. If you prefer to add a subdirectory for the figures, then you will have to specify `\graphicspath{}` in the preamble of the document.
- `README.md` is this file containing all the details related to the template.

Go through both of the `.tex` files to see what packages have been included and what options are invoked to obtain the current formatting. The structure of the `.tex` files is almost identical except for a few minor changes to serve separate purposes. You can tweak the options or add more packages to format the document to your preference or field-specific requirements.



## How to use the template on Overleaf

I prefer using Overleaf for all of my LaTeX compilation and I recommend it strongly since Johns Hopkins provides the premium account to all students for Overleaf. Premium Overleaf does fast compilation, allows sharing the project with multiple people (advisor, committee members, collaborator, labmates, friends, or family), and tracks history. You can recover files if you break them (hopefully you won't). Follow one of the three approaches for getting started with this project on Overleaf.

- To use it directly on Overleaf, [open the template here](https://www.overleaf.com/latex/templates/johns-hopkins-meche-dissertation-proposal-template/ppqmcfvvpzsx). Then click on **Open as Template** and proceed from there to go through the template and edit it.

- If the Overleaf version is outdated for some reason (Overleaf takes a bit of time to update the templates), then you can download/clone this repository from GitHub, and compress it as a zip file. Go to Overleaf, Click on **New Project** -> **Upload Project**, then upload the zipped folder. Continue...
  
- If you have your Overleaf and GitHub account linked and want to have copies of the project in both places, you can **fork** this repository. Then go to Overleaf and click on **New Project** -> **Import from GitHub**, it should list the forked project for listing. Once imported, you can start working... But Overleaf and GitHub will not sync automatically; you will have to do it.

- Once the project is opened, for the main proposal document, compile `proposal.tex` and for the response to the committee document, compile `02-response.tex`. You will have to compile them separately. These files should compile separately without any errors; you may ignore warnings (if any). In your first submission to the thesis proposal committee, response text should not be necessary. During resubmission (if your committee members require you to do so), compile them separately and if you need to submit them as one document, just merge them using the Preview app on macOS or online PDF tools.

> [!TIP]
>
> Although it is very convenient to write your document on Overleaf, consider backing up your work on Overleaf using Git or GitHub integration or the Dropbox sync feature.



## Document formatting

### Main proposal document

- The margin used in both documents (proposal and response) is **1.0in** for all sides with no header and special footer except for the pagination at the bottom center inside the margin.
  - The title page of the main proposal document does not have any pagination. The pagination counter starts from the abstract page with the Roman numeral ii and continues this way throughout the front matter. For the main text in the proposal document, the pagination resets in Arabic starting from 1. The pagination is placed in the footer of the document.
 
- The document is typeset using Latin Modern Roman font (loaded using the `lmodern` package) with a single-spaced 12 pt font size for the main text.
  - For the proposal title, I used `\Large\bfseries\MakeUppercase` (**boldface 17.28 pt**).
  - For the section headings, I used `\singlespacing\large\bfseries` (**boldface 14.4 pt**) with an underline throughout the width of the page.
  - For the subsection headings, I used `\normalsize\bfseries` (**boldface 12 pt**) whereas for the subsubsection headings, I used `\normalsize\itshape` (*italic 12 pt*).
  - For the table and figure captions, I used `\small` (10.95 pt).
  - For the footnotes, I used `\footnotesize` (10 pt), and footnotes are single-spaced with `0.5\baselineskip` spacing between each footnote.

- The title page of the main proposal document is inspired by [thesis/ dissertation formatting provided by the Johns Hopkins Sheridan Library](https://www.library.jhu.edu/library-services/electronic-theses-dissertations/formatting-requirements/) but it was customized to my preference since there is no specific guideline to it. If you have more than two committee members besides your advisor or have multiple advisors/ co-advisors, you may need to use the `minipage` environment to fit the full committee on the title page. Or you may change the style of it entirely to fit your necessity.
  - The title page starts with a statement that is placed 1 inch from the top of the page followed by a tentative title for the thesis and the author placed with 0.5 inches and 0.25 inches spacing relative to each other. These contents are center-justified on the page.
  - Thesis advisor and proposal committee members with their affiliations are included next in a left justified on the page. Depending on the situation, you may need to change the format of this (see below).
  - Location and date are placed in two different single-spaced lines followed by the committee members.
  - An optional copyright statement is placed 1.5 inches from the bottom of the place in a single line.

- Front matters are placed following the title page in this order: Abstract, Table of Contents (ToC), List of Tables (LoT), and List of Figures (LoF).
  - The section headings for these environments are placed 1 inch from the top of the page.
  - Text in the Abstract is single-spaced.
  - The Table of Contents (ToC), List of Tables (LoT), and List of Figures (LoF) are **one-half-spaced**. The titles of these environments are treated as of a similar type as the section headings, i.e., the same font size and type with underlining below them.
 
- Following the suggested outline by the department, in the main proposal document, the following sections are included, however, you can include other sections by consulting your advisor or committee members.
  - **Background and significance:** the suggested page limit is 2 pages.
  - **Research objectives:** the suggested page limit is 1 page.
  - **Proposed methodology and results:** the suggested page limit is 4 pages.
  - **Planned publications:** no specific limits on the pages.
  - **Timeline:** no specific format/ limits on the page
  - **Acknowledgement**: this is optional - thank the people who helped you along the way and funding sources as well.
  - **Bibliographic references**: add all the citations following a specific format based on your discipline

- For the main text of the main proposal document, there are **three** levels of paragraph-style environments (section, subsection, subsubsection) for writing. All of them are shown in the Table of Contents as well.
  - The spacing around the section, subsection, and subsubsection headings are chosen to be default offered by the `parskip` package. The paragraphs do not have any indentation with `\baselineskip` spacing in between them.

- The default spacing between rows inside a table environment is single-spaced.
  
- Captions for the table and figure environments are placed at the bottom of the environments. The caption starts with boldfaced **Figure** and **Table** labels, respectively, for Figure and Table, and uses chapter-wise numbering separated by a period between the section label and the number of the corresponding environment followed by a colon before the long caption.

- Equation numbers are also preceded by section numbers as defined by the following command:
```
\numberwithin{equation}{section}       
```

- The back matter includes the bibliographic references in a single-spaced format with 6 pt (`0.4\baselineskip`) between each bibliographic item.
  - Default bibliography style is numbered-based `Nature` style citation. Depending on the discipline, you may have to change it; the details are given below.


### Response document

- The response document is based on the standard LaTeX article class that does not have any specialized title page. The document has a standard title-author block at the beginning of the document. The document has a 1.0-inch margin on every side. Arabic numeral 1 is used for pagination from the first page placed in the bottom center inside the margin with no header.

- For each member of the committee, the document has a dedicated section that starts on a new page and contains the questions and responses as numbered items. To provide your response, you can add figures, tables, citations, etc. as needed.
  - Tables and Figures also have the same format as the main document.
  - Bibliographic reference has the same format as the main proposal document, i.e., single-spaced bibliographic items with `0.4\baselineskip` between them.
 

## User guidelines

### Proposal document

Overleaf has a huge collection of tutorials and examples on different LaTeX-related typesetting topics (margins and page size, math, table, footnote, and bibliography management). You will most likely find what you need there. If you would like to do something specific, your best friend is Google; someone on [TeX StackExchange](https://tex.stackexchange.com) has perhaps done it. The preamble section of both of the `.tex` files has been subdivided into multiple sections to make the code understandable and readable. A simple descriptions of the sections are below:

- Most of the necessary variables to customize the format and the style of the document are included at the beginning of the `.tex` file in the `LIST OF VARIABLES FOR FORMATTING` section. You can customize different spacing and font style options using these variables. For most cases, tweaking these variables to your needs and preferences will be enough to get the desired formatting.
    
- The most common and popular packages for writing your dissertation proposal are added in the `LaTeX CLASS AND PACKAGES` sections. Check the packages; add any additional package you need and/or customize your options there. For some packages, they are already loaded with the options specified in that section. For some other packages, options are specified in the `PACKAGE OPTIONS` section. Based on the declared variables and loaded packages and their options, formatting-related customized settings are available in the `DOCUMENT FORMATTING` section.

- If you change any formatting or do further customization, one of the best possible ways to check consistency in spacing is to load the `fgruler` package as below in the preamble (you can change the options by looking into the documentation of this package).
```
\usepackage[unit=in,type=upperleft,color=red,showframe]{fgruler}
``` 

- Add your math macros and settings in the `MATH SETTINGS AND MACROS` section. There's a section for non-math `OTHER MACROS` as well. Some examples of both types of macros are added there in the template.

- To change the default font to another font of your preference, you can load the font package using the `\usepackage{}` command. However, you will have to be careful about the consistency of the typography, especially between text and math environments. [Follow this discussion on StackExchange to learn more about fonts in LaTeX](https://tex.stackexchange.com/questions/59702/suggest-a-nice-font-family-for-my-basic-latex-template-text-and-math).

-  If you find the main text is too tightly spaced, you can space out the content by using `\onehalfspacing` or `\doublespacing` instead of `\singlespacing` for the main text in both `.tex` files. In this case, you will have to change the spacing for other environments as well to have a consistently formatted document.
  - In case you change text spacing, you most likely would need to change the spacing around the headings of different environments that are managed by the `parskip` package. I found the default settings to be working fine for me. But if you would like to customize it, you can add the following command in the preamble:
  ```
  \titlespacing*{<environment-name>}{<space-left>}{<space-before>}{<space-after>}
  ```
- The table of contents (ToC), list of figures (LoF), and list of tables (LoT) are considered to be equivalent to unnumbered sections in this template. The `tocloft` package was used to manage this typesetting for the title. If you do not want any or one of these items to appear in your document to keep the document concise, you can comment out or delete the relevant commands in the `FRONT MATTER` section of the `01-main.tex` file.

- Every section (numbered or unnumbered) is followed by a `\titlerule`. If you do not like the appearance of it, you can delete it to make it appear a little bit more cleaner and less distracting. Check the `DOCUMENT FORMATTING` section in the `01-main.tex` file.
  - However, the `\hrule` command is added to the ToC, LoF, and LoT in the front matter section of the `01-main.tex` file manually. If you would like to remove them, look into the `FRONT MATTER` section in the `01-main.tex` file.

- I used the unnumbered `subsection*` and `subsubsection*` environment in the main proposal document to avoid confusion with the numbering scheme of my objectives, tasks, and subtasks. However, to add them to the table of contents, I placed the `\phantomsection` and `\addcontentsline` commands before and after (respectively) declaring the environments. If you would like, you can change it to a standard numbered section and subsection by using the default `\subsection` and `\subsubsection` commands.

- Add all of your figures to the main directory. You can also add the figures to a specific subdirectory if you would like. In that case, you will have to define the subdirectory in `\includegraphicspath{}` command.
  - Regardless of the file extension and program you use to produce the figure, it is a good practice to ensure the fonts within the images are embedded.

 - If you would like to customize the spacing inside a table globally throughout the document, you can change the variable `\GlobalTableSpacing`. However, I suggest doing it locally by defining a group for each table (StackExhange or StackOverflow is your friend here) where you can redefine `\arraystretch` for the individual tables as needed. Also if the table is wider than the page during editing, you may want to use the landscape tables which are placed sideways and may go over multiple pages (someone on StackExhange or StackOverflow has done it for sure).
  - For wide tables, you can use the `sideways` environment from the `rotating` package which will print our table in landscape mode.

- For `enumerate` and `itemize` environments, customize the spacing to ensure it is consistent with the spacing of the document (the default is single-spaced, however, you can change it as mentioned before).

-The name of your bib file has to be specified in the `BibFileName` variable in the `LIST OF VARIABLES FOR FORMATTING` section. If your bib file has a different name than the given file, then change the variable name. The bibliography file is based on BibLaTeX which is a more modern and flexible package compared to BibTeX and natbib. Perhaps consider using Zotero, Mendely, EndNote, or some other citation manager to generate a standard BibLaTeX file. Learn about [citation styles in BibLaTeX](https://www.overleaf.com/learn/latex/Biblatex_citation_styles).

  - Currently, the biblatex package is used with the `nature` citation style (numbered). You may need to change it based on your research field such as IEEE, APA, or something else. While I prefer author-year format (such as APA) in most cases, I found numbered-style citations to be more appropriate because of the page limitation. If you would like to change or customize it, look for the command where the `biblatex` package is loaded in the `LaTeX CLASS AND PACKAGES` section.
  ```
  \usepackage[ ... ]{biblatex}
  ```
  - In the list of planned (or already published) publications, use the `\fullcite` command to print the bibliography directly in the document. However, if that citation does not appear anywhere in the document and you do not want to include it in the final bibliography in the back matter, use the following command alongside `\fullcite`.
  ```
  \mybibexclude{citation-key}
  ```
  - Bibliographic references are printed using the following command which will ensure the citations included in the `\mybibexlude{}` command are not printed.
  ```
  \printbibliography[heading=none,notcategory=mypapers]
  ```
- To use colors in your writing (such as hyperlinking or text coloring) or drawing, you can consider using the `xcolor` package with the `dvipsnames` option (already loaded with this option in the preamble). Check [using colors in LaTeX on Overleaf](https://www.overleaf.com/learn/latex/Using_colors_in_LaTeX).

- You can use the `\linenumbers` command from the `lineno` (already loaded) package anywhere inside the main text document when you would like to have line numbers on the left margin. It might be useful during the drafting stage.

- Finally, you may consider using the `microtype` package to have a better typography of your document. Check details on using [microtype package for writing a thesis here](https://www.khirevich.com/latex/microtype/).

- Keep writing ... and good luck :tada:!


### Response document

- Questions or suggestions are written in a different color `(royalblue)` than the actual response using the `xcolor` package with the `dvipsnames` option. You can change the color to your preference. You can use this package to add colors in other cases as well; check [using colors in LaTeX on Overleaf](https://www.overleaf.com/learn/latex/Using_colors_in_LaTeX).

- For tables, figures, bibliography, footnotes, and any other special environments, follow the suggested format given above for the main proposal document.


### Final note on organizing

If you find all the packages and their settings and macros to be overwhelming and distracting during writing and editing, you can cut and paste all these contents to a separate `my-preamble.tex` file (name it as you like) in the project directory. Then you can use the command `input{my-preamble.tex}` to make your main file appear cleaner and less distracting. See [managing a large project on Overleaf](https://www.overleaf.com/learn/latex/Management_in_a_large_project). You can also upgrade the template-related settings to make a LaTeX package for the thesis using the `.sty` file.

## Contributing to the project

This template was kept sufficiently general purpose for with some customization examples for special packages or macros for demonstration purposes. Since there are no specific formatting requirements available, I do not plan on actively maintaining this repository. But if you have questions, I would be happy to help! Also, if any package becomes obsolete or you have better ideas to implement something, you can create a fork and make a `pull request`, or just let me know.
