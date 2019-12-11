## Sweave/TeX template for poster presentations


This Sweave template for poster presentations uses three colors, mainly a theme color (blue), an alert color (orange) and a third color (green) that are easily customizable. R code and outputs fit with the colors defined in the template.
    
The poster is based on the TeX template created by [Nathaniel Johnston](http://www.njohnston.ca/2009/08/latex-poster-template/). You can find his template on [ShareLaTeX](https://www.sharelatex.com/templates/presentations/nathaniel-johnston's-poster).

For more information about **knitr** and options of R code chunks, see https://yihui.name/knitr/ or the [R Markdown cheat sheet](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf). 

## Define new colors


If you want to change the three colors to create another color theme, set new RGB color codes in both the Sweave file (.Rnw) and LaTeX style file (.sty) with the following commands:

```tex
% Define colors
\definecolor{mgreen}{rgb}{0,0.6,0.35}
\definecolor{mblue}{rgb}{0,0.4,0.6}
\definecolor{mred}{rgb}{0.9,0.3,0}
\definecolor{mgrey}{rgb}{0.85,0.85,0.85}
\definecolor{mblack}{rgb}{0,0,0}
```

Make sure to modify RGB codes in the first R chunk of the Sweave file accordingly so that your R outputs fit with the color theme:

```r
mblue <- function(alpha = 1){rgb(0,0.4,0.6,alpha)}
mred <- function(alpha = 1){rgb(0.9,0.3,0,alpha)}
mgreen <- function(alpha = 1){rgb(0,0.6,0.35,alpha)}
```

To customize even more this beamer template, you can modify commands in the "colors customization" section of the LaTeX style file. You can either create new environments with different colors, redefine colors of R code or change every color displayed in the template from the text to the background.


If you change several colors or add customization commands, feel free to contribute to this template to enhance its look and usefulness! This template is still under construction.


### Authors


- Anthony Coache *(creator, author)*