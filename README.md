# intro-ds-and-chaos

[![][logo]][logo-large]

*Introduction to Dynamical Systems and Chaos*


## About

This repo holds text, notes, and code created while taking the
[Sante Fe Institute][sfi]'s [Complexity Explorer][ce] course
[Introduction to Dynamical Systems and Chaos][intro-ds-and-chaos].


## Notebooks

The list below links to sections (typically once section is released per week)
where I have created notebooks for this course. All notebooks, unless otherwise indicated, have been created using the [Maxima CAS][maxima]
(see also the [Maxima Wikipedia article][maxima-wiki]) in conjunction with
[jupyter][jupyter]. Most of the code samples in the notebooks are written in
Common Lisp ([SBCL][sbcl]).

* [Section 1][nbviewer-section1] (Fixed points and stability)
* [Section 2][nbviewer-section2] (Differential equations)

Those links use the [jupyter notebook viewer online service][nbviewer] to render
the notebooks in this repository.

If you are interested in learning more about running Maxima on your machine or
in a notebook, be sure to check out [these resources][nbviewer-resources] (which
includes some fun history/backstory on Maxima!). If you'd like to use more Lisp
in Maxima notebooks, be sure to check out the [tutorial here][lisp-in-maxima].


## Running Locally

If you'd like to run these notebooks, I suggest using `docker` in the following
manner:

1. `git clone git@github.com:oubiwann/intro-ds-and-chaos.git`
1. `cd intro-ds-and-chaos`
1. Then run:
	```shell
	docker run -it \
	    -v "`pwd`/notebooks":/home/oubiwann/maxima-jupyter/examples \
	    -p 8888:8888 \
	    calyau/maxima-jupyter \
	    notebook --ip=0.0.0.0 --port=8888
	```
1. Once Jupyter starts, you'll see a link with a token displayed in your
   terminal; copy and paste that into your browser, and you're ready to go!


## License

Copyright © 2019, Duncan McGreggor

Apache License, Version 2.0.

<!-- Named page links below: /-->

[logo]: https://raw.githubusercontent.com/oubiwann/intro-abm/master/resources/images/complexity-explorer-logo-x250.jpg
[logo-large]: https://raw.githubusercontent.com/oubiwann/intro-abm/master/resources/images/complexity-explorer-logo-x800.png
[sfi]: https://www.santafe.edu/
[ce]: https://www.complexityexplorer.org/
[intro-ds-and-chaos]: https://www.complexityexplorer.org/courses/97-introduction-to-complexity/
[maxima]: http://maxima.sourceforge.net/
[maxima-wiki]: https://en.wikipedia.org/wiki/Maxima_(software)
[jupyter]: https://jupyter.org/
[sbcl]: http://www.sbcl.org/
[nbviewer-section1]: https://nbviewer.jupyter.org/github/oubiwann/intro-ds-and-chaos/blob/master/notebooks/Fixed%20Points%20and%20Stability.ipynb
[nbviewer-section2]: https://nbviewer.jupyter.org/github/oubiwann/intro-ds-and-chaos/blob/master/notebooks/Calc%20Refresh%20and%20DiffEq%20Intro.ipynb
[nbviewer-resources]: https://nbviewer.jupyter.org/github/oubiwann/intro-ds-and-chaos/blob/master/notebooks/Maxima%20Resources.ipynb
[nbviewer]: https://nbviewer.jupyter.org/
[lisp-in-maxima]: https://nbviewer.jupyter.org/github/calyau/maxima-tutorial-notebooks/blob/master/notebooks/Use%20of%20Lisp.ipynb
