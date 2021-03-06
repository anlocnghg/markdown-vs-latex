# Markdown vs LaTeX / TeX Markup

_Markdown vs Markup_

---

Note:  Why? LaTeX / TeX markup works great for producing high-quality typesetting for articles, research papers, manuals, books, etc.
Markdown works great for distraction-free focus-on-what-you-want-to-say writing.

Using tools such as [pandoc](http://pandoc.org) or [kramdown](http://kramdown.gettalong.org/converter/latex.html) you can (auto-)convert plain text in markdown to LaTeX for further processing. Get the best of both worlds! We ♥ Markdown & LaTeX.

---


## Article

```latex
\documentclass{article}

\begin{document}
Hello world!
\end{document}
```

vs

```
Hello world!
```

</>

Note: In LaTeX "standard" title infos include: title, author, date
(and thanks).


```latex
\documentclass{article}
\title{How to Structure a LaTeX Document}
\author{Andrew Roberts}
\date{December 2016}
\begin{document}
   \maketitle
   Hello world!
\end{document}
```

vs


```
---
title:  How to Structure a LaTeX Document
author: Andrew Roberts
date:   December 2016
---

Hello world!
```

</>


## Book

Note: In LaTeX "standard" sections include:

Level | Section       | Used by
----- | ------------- | ---------- 
(-1)  | part          | book, (report?)
0     | chapter       | book
1     | section       | book, article, report
2     | subsection    | book, article, report
3     | subsubsection | book, article, report
4     | paragraph     | book, article, report
5     | subparagraph  | book, article, report

Sections in letters include: address, opening, closing, signature, etc.;
in presentations (e.g. beamer) include: frame, etc.; in posters include: ??


```latex
\documentclass{book}
\begin{document}

\chapter{Introduction}
This chapter's content...

\section{Structure}
This section's content...

\subsection{Top Matter}
This subsection's content...

\subsubsection{Article Information}
This subsubsection's content...
\end{document}
```

vs

```
# Introduction

This chapter's content...

## Structure

This section's content...

### Top Matter

This subsection's content...

#### Article Information

This subsubsection's content...
```

</>


## Paragraphs and White Space

```
The ends  of words and sentences are marked 
  by   spaces. It  doesn't matter how many 
spaces    you type; one is as good as 100.  The
end of   a line counts as a space.

One   or more   blank lines denote the  end 
of  a paragraph.  
```

Note: The same in LaTeX and Markdown.
However, indentation by four or more spaces starts a code block/verbatim text block
in Markdown.

</>


## Verbatim Text / Code Blocks

```latex
\begin{verbatim}
The verbatim environment
  simply reproduces every
 character you input,
including all  s p a c e s!
\end{verbatim}
```

vs

```
····The verbatim environment
····  simply reproduces every
···· character you input,
····including all  s p a c e s!
```

Note: Dots (`····`) used for showing (invisible) leading four spaces.

</>


## (Hard) Line Breaks

```latex
Andrew Roberts\\
School of Computing,\\
University of Leeds,\\
Leeds,\\
United Kingdom,\\
LS2 1HE
```

vs

```
Andrew Roberts··
School of Computing,··
University of Leeds,··
Leeds,··
United Kingdom,··
LS2 1HE
```

Note: Dots (`··`) used for showing (invisible) trailing two spaces.

or

```
Andrew Roberts       \
School of Computing, \
University of Leeds, \
Leeds,               \
United Kingdom,      \
LS2 1HE
```

</>


## (Inline) Text Formatting (Bold & Italics)

Note: In LaTeX text formatting styles include:

Macro                              | Environment      | Comments
---------------------------------- | ---------------- | -------------
`\textbf{text}`                    | `\bfseries`      | Bold
`\textit{text}` or `\emph{text}`   | `\itshape`       | Italic
`\texttt{text}`                    | `\ttfamily`      | Monospaced


```latex
A \textbf{bold \textit{Hello LaTeX}} to start!
```

vs

```
A **bold _Hello LaTeX_** to start!
```

</>


## Bulleted List

```latex
\begin{itemize}  
  \item The first item
  \item The second item
  \item The third etc.
\end{itemize}
```

vs

```
* The first item
* The second item
* The third etc.
```

or

```
- The first item
- The second item
- The third etc.
```

</>


## Numbered List

```latex
\begin{enumerate}  
  \item The first item
  \item The second item
  \item The third etc.
\end{enumerate}
```

vs

```
1. The first item
2. The second item
3. The third etc.
```

</>

```latex
\begin{enumerate}  
  \item The first item
  \begin{enumerate}
    \item Nested item 1
    \item Nested item 2
  \end{enumerate}
  \item The second item
  \item The third etc.
\end{enumerate}
```

vs

```
1. The first item
   a. Nested item 1
   b. Nested item 2
2. The second item
3. The third etc.
```

</>



## Simple Table

```latex
\begin{tabular}{ l l l }
  Day       & Min Temp & Max Temp \\
  Monday    &    11° C &  22° C \\
  Tuesday   &     9° C &  19° C \\
  Wednesday &    10° C &  21° C \\
\end{tabular}
```

vs

```
Day       | Min Temp | Max Temp
--------- | -------- | --------
Monday    |  11° C   |  22° C
Tuesday   |   9° C   |  19° C
Wednesday |  10° C   |  21° C
```

</>



## Quotes & Dashes

```latex
Quotation marks like
       ``this'' 
have to be handled specially, as do quotes within
quotes:
       ``\,`this'            % \, separates the double and single quote.
        is what I just 
        wrote, not  `that'\,''.  
```

vs

```
Quotation marks like
  "this" 
have to be handled specially, as do quotes within
quotes:
  "'this'            
   is what I just 
   wrote, not  'that'".  

```

Note: Markdown uses a text filter (smarty pants) to pretty print quotes.

</>

```latex
Dashes come in three sizes: an 
       intra-word 
dash, a medium dash for number ranges like 
       1--2, 
and a punctuation 
       dash---like 
this.
```

Note: In LaTeX `-` is always a dash (hyphen); use `$-$` for minus (in numbers/mathematics)

```
Dashes come in three sizes: an
  intra-word 
dash, a medium dash for number ranges like 
  1--2, 
and a punctuation 
  dash---like 
this.
```

Note: Markdown uses a text filter (smarty pants) to pretty print dashes.

</>

## Comments

```latex
% This is a sample LaTeX input file.  (Version of 12 August 2004.)
%
% A '%' character causes TeX to ignore all remaining text on the line,
% and is used for comments like this one.
```

vs

```
<!--
  This is a sample LaTeX input file.  (Version of 12 August 2004.)
  A '%' character causes TeX to ignore all remaining text on the line,
  and is used for comments like this one.
  -->
```

Note: Markdown uses HTML comments.


</>


## Reserved "Special" Characters

Notes:

```
\    =>    \textbackslash (*)            -- used for macros   
{    =>    \{                            -- used for begin group
}    =>    \}                            -- used for end group
#    =>    \#                            -- used for macro parameters
%    =>    \%                            -- used for comments
~    =>    \~{} (**) or \textasciitilde  -- used for non-breaking space
&    =>    \&                            -- used for cell/column separator in tables

$    =>    \$                            -- used for math(ematics) mode
^    =>    \^{} (***)                    -- used for superscript (math modes only)
_    =>    \_                            -- used for subscript (math modes only)


*:   note \\ cannot be used; already in use for hard line breaks
**:  note \~ followed by character used for accented chars e.g. \~n gives ñ  
***: note \^ followed by character used for accented chars with hat e.g. \^a gives â
```

vs

```
\    =>   \\        -- backslash
`    =>   \`        -- backtick
*    =>   \*        -- asterisk
_    =>   \_        -- underscore
{}   =>   \{ or \}  -- curly braces
[]   =>   \[ or \]  -- square brackets
()   =>   \( or \)  -- parentheses
#    =>   \#        -- hash mark
+    =>   \+        -- plus sign
-    =>   \-        -- minus sign (hyphen)
.    =>   \.        -- dot 
!    =>   \!        -- exclamation mark

add | (pipe?) and : (colon?) others? (see commanmark spec for recommendation?)

todo: Check for chars with special meaning in verbatim (code/code block) mode
```

</>

