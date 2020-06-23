# Instructions to build NRT-Library website locally

Here are thr instructions to build the NRT-Lirbary site locally.

It is recommended to work in your own branch of the project.

Serving the website locally will help you to see any changes you make in real time. Just change the markdown file and save. Some changes may requiere to close the browser and rebuild the site.

## Getting prerequisites

To build the site locally, you will need the following:

- [GitHub account](https://github.com/)
- [Git](https://git-scm.com/downloads)
- [Ruby](https://www.ruby-lang.org/en/)
- [RubyGems](https://rubygems.org/)
- [Jekyll](https://jekyllrb.com/)
- [Bundler](https://bundler.io/)

Below I provide instructions for each.

### GitHub

Fo to [github.com](https://github.com/) and follow the account creation instructions.

### Git

Check if you have git installed in the terminal as:

```git
git --version

# you should see something like
git version 2.17.1
```

If you do not have Git installed, go [here](https://git-scm.com/downloads) and follow the installation instruction for your system.

### Ruby

Check you have Ruby installed by:

```bash
# Mac/Linux
which ruby

# You should see something like
/usr/bin/ruby
------------------------
# Windows Command Prompt 
where ruby

# You should see something like
C:\Ruby26-x64\bin\ruby.exe
```

If you not have Ruby installed, follow installation instruction for your system [here](https://rubyinstaller.org/downloads/)

### RubyGems

RubyGems is a package manager for Ruby. It should be installed along with Ruby. 

To check you have RubyGems, run:

```bash
# Mac/Linux
which ruby

# You should see something like
/usr/bin/gem

------------------------
# Windows Command Prompt
where gem

# You should see something like
C:\Ruby26-x64\bin\gem
C:\Ruby26-x64\bin\gem.cmd
```

If you do not have RubyGem installed follow the installation instructions for your system [here](https://rubygems.org/pages/download).

### Jekyll

Jekyll is a Ruby package (Gem) to generate static websites.

Verify you have Jekyll installed by:

```bash
# Mac/Linux
which jekyll

# You should see something like
/usr/local/bin/jekyll

------------------------
# Windows Command Prompt 
where jekyll

# You should see something like
C:\Ruby26-x64\bin\jekyll
C:\Ruby26-x64\bin\jekyll.bat
```

If you do not have Jekyll installed, install it by:

```ruby
# Mac/Linux
gem install jekyll

------------------------
# Windows Command Prompt
gem install jekyll
```

Check installation was successful by:
```ruby
jekyll --version

# You should see the jekyll version printed out
jekyll 4.1.0
```

### Bundler

Bundler is a tool for dependency managment and resolution wich is paired with RubyGems.

Verify you have Bundler installed by:

```bash
# Mac/Linux
which bundler

# You should see something like
/usr/local/bin/bundler

------------------------
# Windows Command Prompt 
where bundler

# You should see something like
C:\Ruby26-x64\bin\bundler.cmd
```

If you do not have bundler installed, install it by:

```ruby
# Mac/Linux
gem install bundler

------------------------
# Windows Command Prompt
gem install bundler
```

Check installation was successful by:

```ruby
bundler --version

# You should see the jekyll version printed out
Bundler version 1.17.2
```

## Cloning the repo locally

Open the terminal in the directory where you want to save the files. Then, clone the repo as:

```git
git clone https://github.com/nrt-library/nrt-library.git
```

Then, nagivate into the directory as:

```bash
cd nrt-library/
```

## To create a GitHub branch

Once you you clone the repo, you will be default to the master branch. It is not recommended to work in the master branch. To create your own isolated branch of the project:

```git
git branch MY-BRANCH-NAME
```

After creation, you need to your new branch to work in it:

```git
git checkout MY-BRANCH-NAME
```

From now on, all the changes you do to the project will be saved in your branch without affecting the main project.

## Serving the site locally

To double check you are serving your own branch type:

```git
git branch
```

This will print all the existing branches in your computer. For instance:

```git
*master
 pablo-branch
 END
```

The `*` indicates in which branch you are working right now. In the previous example is indicating it is in the master branch. Hence, I need to swtich with:

```git
git checkout pablo-branch
```

Now:

```git
git branch
```

Prints:

```git
 master
*pablo-branch
 END
```

To serve the site locally, first update bundler as:

```ruby
bundler update
```

Note you may need Admin privileges to update Bundler.

Once Bundler is updated, make sure your terminal is in the `nrt-library/` directory and run:

```ruby
bundle exec jekyll serve
```

By default, the site should be served at http://127.0.0.1:4000 address. Copy and paste into your favorite browser.

If this address does not work, copy the address at `Server address:` printed in the terminal and past into your favorite browser.

It is recommended to end the process by typing `Ctrl + C` in the terminal. Otherwise, the process will be keep running in the background which may create problems updating the site contents. Closing and reopening the terminal should have the same effect.

## Serving your own branch of the website

In the terminal, make sure you are in your branch in Git as:

```git
git checkout MY-BRANCH-NAME
```

Then you can run

```ruby
bundle exec jekyll serve
```

The browser will render your branch version.

## 

Now your branch exist in your computer, but not on-line. To push your branch on-line for THE FIRST time, this is, assuming the branch does not exist on-line in GitHub already:

```git
git push -u origin MY-BRANCH-NAME
```

Alternatively, If your branch exist online, you can push changes as:

```git
git push origin MY-BRANCH-NAME
```

Once you are done with the section you want to put in the website, you need to merge your branch with the master branch as:

```git
# first switch to the master branch
git checkout master
# then merge
git merge MY-BRANCH-NAME
```