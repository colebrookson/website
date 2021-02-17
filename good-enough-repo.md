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
some of the other great resources that are out there.  
