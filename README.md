# ANN3: Méthodes numériques matricicelles avancées: analyse et experimentation (2025)

## Organization

This repository contains the material for the
[ANN203](https://synapses.ensta-paris.fr/catalogue/2024-2025/ue/7679/ann203-methodes-numeriques-matricielles-avancees-analyse-et-experimentation)
course taught at ENSTA. The course is an introduction to numerical linear algebra, and
contains a mix of theory and programming/algorithmic assignments.

The homeworks will be done using [Pluto](https://plutojl.org) notebooks and the
[Julia](https://julialang.org) programming language. For each homework assignment, I will
provide a Pluto notebook with exercises of both theoretical and practical nature, and you
will fill it in with your solutions and submit the notebook for grading. Code can run
directly in the notebooks.

The main reference for the course are the lecture notes by Marc Bonnet, available
[here](https://hal.science/hal-03321502v2/file/aln.pdf). I will post slight modifications of these notes
as we go along, but the main content will be the same.

## Grading

The course will be graded as follows:

- 60% of the grade will be based on the homework assignments (2 graded assignments with 30%
  each). For each graded homework, you will have 1 week to complete it.
- 40% of the grade will be based on the final exam (1.5 hours)

## Schedule

Below is **tentative** schedule for the course:

| Date      | Time        | Room      | Lecture                                      | Project (TP)                              |
| --------- | ----------- | --------- | -------------------------------------------- | ----------------------------------------- |
| Thu 27/03 | 9:00-12:15  | Room 1226 | Motivation, review, and generalities         | Intro. to Julia, round-off, stability     |
| Thu 03/04 | 9:00-12:15  | Room 1226 | Square linear systems and direct solvers     | Polynomial interpolation, conditioning    |
| Thu 17/04 | 9:00-12:15  | Room 1226 | Rectangular systems and least-squares        | **Orthogonal polynomials and QR**         |
| Tue 29/04 | 14:00-17:15 | Room 1226 | Matrix eigenvalues                           | Image compression                         |
| Tue 06/05 | 14:00-17:15 | Room 1226 | Iterative solvers                            | GMRES                                     |
| Tue 13/05 | 14:00-17:15 | Room 1226 | Preconditioning and ill-conditioned problems | **PDE discretization + pre-conditioners** |
| Tue 20/05 | 9:00-12:15  | Room 1315 | Applications and advanced topics             | **EXAM**                                  |

## Getting started

- Install [Julia](https://julialang.org/downloads/). I suggest using
   [Juliaup](https://github.com/JuliaLang/juliaup) for an easier version
   control.
- Install [Pluto](https://github.com/fonsp/Pluto.jl)
- Open a terminal and enter the *Julia REPL* by typing `julia`
- Enter the following lines to open a browser with *Pluto.jl*

```julia
using Pluto
Pluto.run()
```

Your browser should open with a new tab showing the *Pluto* interface (if not, let me know).

The last step is to load the homework assignment. Either download the homework and enter the
path to the downloaded file in *Pluto*, or copy and paste the following URL on the **Open a
notebook** window and press `Open`:

<https://github.com/maltezfaria/ANN3/blob/main/homeworks/ANN3_tp1.jl>

That should load the notebook for the `TP0` in a *safe preview* mode. To execute the content of the notebook, you will need to give *Pluto* permission to run some code.

## From `Matlab` to `Julia`

If you are familiar with `Matlab`, it should not be too difficult to get started
with `Julia`. A lot of the syntax looks familiar, and `Julia`'s standard library
comes with a `LinearAlgebra` package implementing many of the things that you
love about `Matlab` (e.g. the *magical* backslash `\` operator). Here is a [list
of noteworthy
differences](https://docs.julialang.org/en/v1/manual/noteworthy-differences/)
that may help you get started translating code.

## Workflows and `Pluto.jl`

As you will notice in your first assignment, the homework for this class is available in the
form of a `Pluto` notebook. `Pluto`(https://github.com/fonsp/Pluto.jl) provides a
notebook-like environment for combining `Julia` with pretty text that can easily be rendered
on a website, and you can think of it as a web-based *workflow* for developing code (similar
to e.g. *Jupyter* notebooks if you have heard of those). While in general I don't recommend
using `Pluto` for coding anything long or complex, most of the code you will write in this
class is simple enough that using `Pluto` as a *web-based*
[IDE](https://en.wikipedia.org/wiki/Integrated_development_environment) may be a viable
option. My suggestion is to give it a try to see if it fits you.

Should you find yourself hating `Pluto.jl` (and missing `matlab`), I suggest you try [Visual
Studio Code](https://code.visualstudio.com) with its [julia
extension](https://code.visualstudio.com/docs/languages/julia) to have an *out-of-the-box*
experience as similar to `matlab` as possible. Keep in mind that I still expect you to
submit your code as a `Pluto` notebook, but you can always just copy and paste the code to
`Pluto` after you get it to work.
