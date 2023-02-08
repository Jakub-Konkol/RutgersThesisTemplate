# Rutgers Thesis Template
 A latex template formatted for Rutgers thesis/dissertations.
 
 This project is not affiliated with Rutgers.
 
 ## How to use
 
 Begin by downloading this folder and it's contents and then unzipping it. The following will list the 
 changes you will need to make to `main.tex` to use this template for your own thesis.
 
 ### RUTitle options
 The import of RUTitle (line 25) takes several options which will adjust the document as appropriate 
 for terminology and format.
 
To choose the field of engineering, replace ``CBE`` with any of the following:
| Code | Department |
| ---- | ---------- |
| CBE  | Chemical and Biochemical Engineering |
|  AE  | Aerospace Engineering |
| BME  | Biomedical Engineering |
| CEE  | Civil and Environmental Engineering | 
| ECE  | Electrical and Computer Engineering |
| EnvE | Environmental Engineering |
| ISE  | Industrial and Systems Engineering |
| MSE  | Materials Science and Engineering |
| MAE  | Mechincal Engineering |

To distinguish between a PhD dissertation and a Master Thesis, replace ``PhD`` with
| Code | Document Type |
| ---- | ------------- |
| PhD  | Doctor of Philosophy Dissertation |
| MS   | Master of Science Thesis |
| ME   | Master of Engineering Thesis |

If this is your proposal, you may include ``proposal`` as a third option.

Some examples:

- A masters student in the ECE department preparing their thesis will have 
`\usepackage[ECE,ME]{RuTitle}`

 - A BME doctoral student preparing their proposal will have
 `\usepackage[BME,PhD,proposal]{RuTitle}`

It is VERY IMPORTANT there are no spaces between the import options.

### Author details section
1. Replace the contents of `\author` with your name.
2. Replace the contents of `\title` with the title.
3. Replace the contents of `\graduationDate` with your intended graudation date (October, January, or May and year) or when your proposal defense is.
4. Replace the contents of `\supervisor` with your professor's name. If you are co-advised, write both as `XXX and YYYY`.

### Copyright page
If you are preparing a thesis or dissertation, you include a copyright page using the command `\copyrightPage`. If you are preparing your proposal, delete the command from the template.

### Abstract
Enter your abstract into an `abstract` environment. 

The way you use it is:

```
\begin{abstract}
 Here is a summary of my work...
\end{abstract}
```

You may type directly into the environment or write it in another .tex file and incorporate it using `\input`. Don't use include.

This section is always after the title page.

### Acknowledgements
If you would like to make a larger acknowledgement, you may use the `acknowledgements` environment. The way you use it is:

```
\begin{acknowledgements}
 I would like to thank...
\end{acknowledgements}
```
This section is always after the abstract.

### Dedication
If you would like to make a smaller dedication, you may use the `\dedication{}` command and enter your dedication between the `{}`.

I've seen this after the acknowledgements if there is both, but I don't know if there is any set order. Either way, this is after the abstract.

### Main body content
I would recommend you make individual .tex files for your chapters and incorporate them into main.tex using `\include{}` commands. The template currently some things written into the document, but that's only to show what the chapters look like.

### Bibliography
I leave this up to you in case you have a preference of BibLaTeX vs. BibTex. The guidelines state to "conform to generally accepted practice in the discipline," so it's on you to get the .bst and incorporate your bib file.

# Sources
The information for the formatting is sourced from the Electronic Thesis and Disseration Style Guide from the Rutgers School of Graduate Studies. You can find that resource here: https://grad.rutgers.edu/academics/graduation/electronic-thesis-and-dissertation-style-guide

# Limitations
- I made this from the standpoint of an engineer so I included the engineering degrees. If you are interested in using this template outside of engineering, let me know and I can incorporate your field for you.
- If you are co-advised, the abstract currently does not change to acknowledge there is more than one advisor. You can change the RUAbstract.sty file to add an `s` to Director on line 36.
- I'm testing this as I work on my thesis so errors may exist.
- It's on you to verify that the template is acceptable for your department.

# License
I am publishing this under the LaTeX Project Public License 1.3c. A copy may be seen here: https://www.latex-project.org/lppl.txt.
