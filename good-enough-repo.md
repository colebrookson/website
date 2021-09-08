# How to Make a ~~Perfect~~ Good Enough Repository for Reproducible Science

This is my personal attempt to provide an example for how to structure the basic unit of a scientific
analysis pipeline -- the repository. I am far from an expert, but I am a huge #OpenScience advocate
and I'm passionate about learning how to make my own research as open and accessible as it can be. My
goal is to share some of the things I've cobbled together from software design, Open Science frameworks,
and other sources to try and provide an achievable example of how scientists (particularly ecologists)
can structure their version control repositories and code bases to ensure a baseline level of reproducibility
for other scientists, students, reviewers, and anyone who wants to run their code!

Some components of this will change depending on the specific softwares you're using. Since I am an
ecologist and I am writing this mainly for ecologists and other folks who may not want/have time to learn new
softwares and tools, this tutorial is centered around using the programming language R, and assumes that
you are comfortable working with Git through either the command line or a graphical user interface of some kind.

While there are amazing tools such as [Docker](https://www.docker.com/) and [Snakemake](https://snakemake.readthedocs.io/en/stable/),
built-in GitHub tools that allow for [CI/CD (Continuous Integration and Continuous Delivery)](https://github.com/features/actions), and amazing
cyberinfrastruture run by some amazing groups like [CyVerse](https://www.cyverse.org/), my goal is not to go that far.
I recommend you check out the great [Foundations of Open Science Skills](https://learning.cyverse.org/projects/cyverse-foss/en/latest/index.html) workshop or
some of the other great resources that are out there. A personal favourite for a general introduction is the book
[Computational Skills for Biologists](https://computingskillsforbiologists.com/) by Drs. Stefano Allesina and Madlen Wilmes,
from which I have learned some of the concepts that have informed this post.

## A quick guide to the components of this repo
### The structure of the repo
To keep all of our respective files in their rightful place within a repository, I have used a standard but simple file structure for
organization within this repo, broken up into four main subfolders, *docs*, *code*, *data*, *output*. These are the four common folders
usually used to store different kinds of files related to our analysis.

### `__main__` file
I use the method of employing a `__main__` code file that sources and runs all other code files. This allows all of the analysis to be
run at once in a single code file, but still allows for the different components of the code to be broken up appropriately into bite-sized
files.

### RProject & the `here()` package
This combination, of an RProject that interacts with the `here()` package allows this repository to be transferable to anyone else's
computer. This is essentially for collaboration and for anyone in the future who may want to run your analysis. Absolute paths are
your computer's worst nightmare! For example, on my computer, my code may be stored at this location:
`C:/Users/brookson/Documents/Github/good-enough-repository/` but that's not necessarily where you will store your repository. Having
to manually change these paths is a pain, and is sure to lead to typos and headaches. When cloning a new repository, ensuring you use
an RProject along with the `here()` package allows your computer to figure out the path business for you, and simply point you to where
the files are on *your* computer.
