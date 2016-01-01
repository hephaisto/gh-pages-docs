# gh-pages-docs
Git hook to automatically push current documentation to branch gh-pages

## Installation
* Copy post-commit to your .git/hooks/ directory
* Edit the section "actual doc generation" so that documentation for your code is saved in doc/
* Create a gh-pages branch and create an index.html file which links to the doc/ (or doc/html) directory.

## Usage
Every time you do a commit on the local master branch, doxygen is run and the output to the doc/ directory is saved in the gh-pages branch.
The commit on gh-pages will be relative to the previous gh-pages commit and will reference the code commit upon which it was created only in the commit message.
This is to get a clean history for gh-pages and allow to have manually updated files in gh-pages.

## Limitations
* gh-pages will not be automatically pushed
* No auto-merging of gh-pages in collaborations
