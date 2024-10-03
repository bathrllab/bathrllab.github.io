# Bath RL website

Table of Contents:
- *I want to add myself to the website*
- *I want to change my photo*
- *I want to change my personal links*
- *I want to add a paper*
- *How do I run this locally*

## I want to add myself to the website
Add a photo in `/assets/img/` with a simple title e.g. `pani.jpeg`.
Create a folder with your name in `/_profiles/` and inside add a markdown file (extension .md). Below is an example markdown file with all the supported fields:

```
---
name: Panayiotis Panayiotou (Pani)
linkedIn: https://www.linkedin.com/in/panispani
twitter: https://twitter.com/panispani
profileImg: pani.png
personalSite: https://panispani.com
scholar: https://scholar.google.com/citations?user=AfaKtVwAAAAJ
---
```

There is also a boolean "staff" field, to be only set for stuff e.g. Ozgur.

## I want to change my photo
Photos are in `/assets/img/`. Specify the right image path in your personal profile (these are located in `/_profiles/` in a folder with your name, saved as a markdown .md file).

## I want to change my personal links
Personal profiles are in `/_profiles/`. You need to add a folder with your name and inside a markdown file (.md at the end). For now all the supported fields are the following:

```
---
name: Panayiotis Panayiotou (Pani)
linkedIn: https://www.linkedin.com/in/panispani
twitter: https://twitter.com/panispani
profileImg: pani.png
personalSite: https://panispani.com
scholar: https://scholar.google.com/citations?user=AfaKtVwAAAAJ
---
```

There is also a boolean "staff" field, to be only set for stuff e.g. Ozgur.

## I want to add a paper
Papers are in /assets/papers.txt.
The format of the file is just a collection of BibTeX entries. Just paste your BibTeX entry at the right chronological order. **IMPORTANT:** if you want to add a link to your paper add an extra field in BibTeX called "link". For example,

```
@article{evans2023creating,
  title={Creating multi-level skill hierarchies in reinforcement learning},
  author={Evans, Joshua B and {\c{S}}im{\c{s}}ek, {\"O}zg{\"u}r},
  journal={Advances in Neural Information Processing Systems},
  volume={36},
  pages={48472--48484},
  year={2023},
  link={https://proceedings.neurips.cc/paper_files/paper/2023/file/97b73904e88cc1dc0a3485595eda3753-Paper-Conference.pdf}
}
```

## How do I run this locally
```bash
# Install ruby. If you are not on Mac check the ruby website on how to install and add to your path.
brew install ruby
# Add to PATH.
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
# Verify install.
ruby -v
# Install packages
gem install bundler jekyll
# Make sure EXECUTABLE DIRECTORY is in your PATH
gem env
# Add EXECUTABLE DIRECTORY to PATH if it's not by adding this to .zshrc
export PATH="/opt/homebrew/lib/ruby/gems/3.3.0/bin:$PATH"
source ~/.zshrc
# Create empty template
jekyll new .
# Install dependencies
bundle install
# Build and serve
bundle exec jekyll serve
```

