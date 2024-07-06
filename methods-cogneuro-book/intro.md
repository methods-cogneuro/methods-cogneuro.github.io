---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Introduction

This book, "Methods in cognitive neurosciences", presents the main neuroimaging techniques used to study cognition in humans (and non-human animals) with a good spatial resolution:
 * magnetic resonance imaging (structural, functional, and diffusion),
 * positron emission tomography,
 * optical imaging.

This book is intended as an introduction for readers discovering these neuroimaging methods for the first time, This book will provide the theoretical knowledge of the physical and physiological bases of these neuroimaging techniques. It also provides an introduction to the main image processing and statistical analysis techniques involved. Each chapter includes a series of exercises with examples of applications in cognitive neuroscience research projects. 

```{warning}
The aim of this resource is not to be a reference tool of the "specialist book" type, explaining all the specific details associated with a given technique. Rather, the goal of this book is to present an overview of the most conventional techniques in cognitive neuroscience in a concise manner, so that readers can appreciate their strengths and weaknesses, as well as understand how to choose the technique best suited to a specific type of research.
```

## Contributing

This project is being developed collaboratively. We welcome all suggestions! You can use the "[issue](https://github.com/methods-cogneuro/methods-cogneuro.github.io/issues)" page on Github to make a request to the team, or describe your problem. You can also propose a change directly by making a "pull request" on the book's [Github page](https://github.com/methods-cogneuro/methods-cogneuro.github.io).

## Contributors

The development of this book was initiated to serve as a reference tool for the PSY3018 course, given at the Université de Montréal's bachelor's degree program in cognitive neuroscience. The course is taught primarily by Dr. Pierre Bellec, with contributions from teaching assistants and many additional contributors. This book also benefits from constructive feedback from students who have taken the PSY3018 course since its inception in 2018. The general contributions are presented below. Specific contributions are listed within each chapter.

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/pbellec">
        <img src="https://avatars.githubusercontent.com/u/1670887?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Pierre bellec</b></sub>
      </a>
      <br />
        <a title="Content">🤔</a>
        <a title="Code">💻</a>
        <a title="Quiz">⚠️</a>
        <a title="Text revision">👀</a>
    </td>
    <td align="center">
      <a href="https://github.com/eddyfortier">
        <img src="https://avatars.githubusercontent.com/u/72314243?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Eddy Fortier</b></sub>
      </a>
      <br />
        <a title="Content">🤔</a>
        <a title="Text revision">👀</a>
    </td>
    <td align="center">
      <a href="https://github.com/danjgale">
        <img src="https://avatars.githubusercontent.com/u/14634382?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Dan J Gale</b></sub>
      </a>
      <br />
        <a title="Figure">🎨</a>
    </td>
    <td align="center">
      <a href="https://github.com/SamGuay">
        <img src="https://avatars.githubusercontent.com/u/30598330?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Samuel Guay</b></sub>
      </a>
      <br />
        <a title="Text revision">👀</a>
    </td>  
    <td align="center">
      <a href="https://github.com/Xanthylajoie">
        <img src="https://avatars.githubusercontent.com/u/90349544?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Xanthy Lajoie</b></sub>
      </a>
      <br />
        <a title="Content">🤔</a>
        <a title="Text revision">👀</a>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/elisabethloranger">
        <img src="https://avatars.githubusercontent.com/u/90270981?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Élisabeth Loranger</b></sub>
      </a>
      <br />
        <a title="Content">🤔</a>
    </td>
    <td align="center">
      <a href="https://github.com/sangfrois">
        <img src="https://avatars.githubusercontent.com/u/38385719?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>François Lespinasse</b></sub>
      </a>
      <br />
        <a title="Content">🤔</a>
        <a title="Text revision">👀</a>
    </td>
    <td align="center">
      <a href="https://github.com/me-pic">
        <img src="https://avatars.githubusercontent.com/u/77584086?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Marie-Eve Picard</b></sub>
      </a>
      <br />
        <a title="Content">🤔</a>
        <a title="Text revision">👀</a>
    </td>
    <td align="center">
      <a href="https://github.com/anproulx">
        <img src="https://avatars.githubusercontent.com/u/65092948?v=4?s=100" width="100px;" alt=""/>
        <br /><sub><b>Andréanne Proulx</b></sub>
      </a>
      <br />
        <a title="Content">🤔</a>
    </td>
  </tr>
</table>

## Acknowledgements

This book is to a large extent "reproducible": many of the figures are generated using open data, with code accessible right from the book. This technology is made possible by the following projects:
 * [jupyter book](https://jupyterbook.org) is the tool used to generate the book. This project itself is based on [sphinx](https://www.sphinx-doc.org) documentation tool.
 * The [nilearn](https://nilearn.github.io/) library in [python](https://www.python.org/), notably for the structural MRI, functional MRI and statistical models sections.
 * The [Dipy](https://dipy.org) library, notably for the section on diffusion MRI.
 * The [MNE python](https://mne.tools/stable/index.html) library is used in the chapter on optical imaging.
 * The brain image visualizations used in the course com in part from public datasets. The origin of the data is indicated in the description of each figure.
 * The logo comes from <a href="https://www.vecteezy.com/free-vector/brain">Brain Vectors by Vecteezy</a>
 * Some images in the book were obtained under unlimited rights for web distribution and limited rights for print (500k copies) via [shutterstock](https://www.shutterstock.com) by P. Bellec.

 The authors are very grateful for the hard work and generosity of the communities that create and maintain all these projects!

 ## Statistics

 Generating the figures for the various chapters of the book took the following time:
 ```{nb-exec-table}
```
