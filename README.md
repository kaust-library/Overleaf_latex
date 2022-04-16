# Overleaf and Latex

This is a supporting material for the slides. Here you will find the examples for training.

The goal of this training is Overleaf, the LaTeX part will be very basic.

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
