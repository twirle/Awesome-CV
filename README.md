# Resume Printer

Used this formatter to generate my neatly formatted [CV](https://github.com/twirle/Awesome-CV/blob/master/resume.pdf).

Friend showed me this after exchanging resumes and realised this was a smarter way of updating resumes without having to deal with formatting manually. Requires some packages, LaTex and Google Roboto fonts.

If you're fresh to LaTeX, this might require quite a bit of setup to print and have formatting run locally, or you can use an online LateX formatting/editor and have this print it for you through a Docker container.

`resume.tex` and `awesome-cv.cls` are your config files, amend details in there.
Store your .tex files in `/resume`, or w/e you specify in `resume.tex`

## Reqs

- `sudo apt install texlive-xetex texlive-fonts-extra`
- Original Awesome-CV does not come with Roboto, will need to manually add to files.

## Compiling

1. Based on the examples provided, prepare your .tex files.
2. Run `xelatex resume.tex`
3. Will then have a bunch of packages to install, and outputs resume.pdf.

or for Docker:
`docker run --rm --user $(id -u):$(id -g) -i -w "/doc" -v "$PWD":/doc thomasweise/texlive make`

## Issues

Some alignment issues, will need to add ~5mm of `vspace` at the end of every pointer as bandaid fix.
