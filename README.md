# Learning Latex with Overleaf

Or how to learn basic LaTeX with Overleaf in 30 minutes.

## Overleaf Login

[Overveaf login page](https://www.overleaf.com)

<img src="img/overleaf_login.png" alt="Overleaf login page" width="600"/>

Next use the option to "Log in through your institution" to login using your KAUST credentials

<img src="img/overleaf_login_institution.png" alt="Login via institution" width="600"/>

## New Article

Once you login, you can create a new blank project

<img src="img/overleaf_new_project_2.png" alt="New Blank Project" width="600"/>

Notice that there are several options of templates, including the official KAUST templates for thesis and dissertation template. There are options for letters, books, CV/Resume, and others.

We will start with the blank template, and we will add content to our article.

After choosing the blank template, Overleaf will ask for a name for your project. You can give any meaninful name, like _my first article_. And your new article should looks like the following picture

![Blank template](img/overleaf_template_blank_article.png)

Try to compile the text, and have a look at the PDF file.

### The Preamble

Everything that comes before the `\begin{document}` is the _preamble_. The preamble starts by defining what kind of document we are doing, via the `documentclass` clause. There are several kinds of document: article, book, letter, etc. It's also possible to define the paper size of the document. The default is US letter, but it's possible to change to A4 paper size, [among others](https://www.overleaf.com/learn/latex/Page_size_and_margins). 

Try to change the paper size to A4

```LaTeX
\documentclass[a4paper]{article}
```

You can go one step further, and add font size, like 11pt or 12pt

```LaTeX
\documentclass[10pt,a4paper]{article}
```

Next comes the list of packages that the text will use. In this case we are defining only the _encoding_, and `utf8` is the recommended. Unless a very specific need, don't remove the line. 

```LaTeX
\usepackage[utf8]{inputenc}
```

Next comes the title, the author(s) and the date. There isn't much to write about the title, but the others deserver some attention. 

How to add a second (or third author)? One could simply list the authors like

```LaTeX
\author{Athos, Aramis, and Porthos}
```

It will work, but a better approach is to use the `\and` clause

```LaTeX
\author{Athos \and Aramis \and Porthos}
```

Try for yourself by compiling the text.

If don't include the `\date`, the document will have the date of the compilation, or you can set the date. Finally, if you want to remove the date completely, set an empty date

```LaTeX
\date{}   % For no date
\date{1st January 2000} 
\date{\today} % To explicity set to the date of compilation.
```

### Bold, italics and underlining

To emphasize text in \LaTeX{} use the formatting commands: `\textbf{...}`, `\textit{...}`, and `\underline{...}.` Add the following text to your article

```LaTeX

\section{Text Formatting}

This text is in \textbf{bold}, and this is in \textit{italic}, and this one has \underline{underline.}

```



---

## KAUST Portal

To create your first article, go to the [KAUST portal](https://www.overleaf.com/edu/kaust) in Overleaf

![KAUST porta](img/overleaf_kaust_portal_medium.png)

You can go to the _Quick Start_ or _Templates_ pages. The _Templates_ include the official KAUST thesis template, so it's a good idea to have a look, and familiarize yourself with the document. On the _Quick Start_ there is a simple article (or _paper_ as Overleaf call it) with the basic LaTeX.

## Hands-On

### Articles

On the _Quick Start_ tab of KAUST portal, click on the "Create a new paper." Enter your KAUST credentials, and you will be presented with your first article. The kind of document is define at the very beginning of the document

```
\documentclass[a4paper]{article}
```

The `a4paper` defines the size of the page. There are several [sizes available](https://www.overleaf.com/learn/latex/Page_size_and_margins): a3paper, a4paper, a5paper, letterpaper, executivepaper, legalpaper, etc.

>Note:\
> Overleaf uses European \LaTeX{} distribution with default paper size to `a4paper` whereas, the default for \LaTeX{} is the US size `letter`.

Try to remove the `a4paper` to change to `US letter`.

The `documentclass` defines the type of document: article, book, letter, etc.

Next comes the _preamble_ where you add your packages with `usepackage.` For example, the following packages set the environment to use English. It's possible to change to other languages like [German](https://www.overleaf.com/learn/latex/German),  or [Arabic](https://www.overleaf.com/learn/latex/Arabic), and [many others](https://www.overleaf.com/learn/latex/International_language_support).

```
%% Language and font encodings
\usepackage[english]{babel}
\usepackage[utf8x]{inputenc}
\usepackage[T1]{fontenc}
```
