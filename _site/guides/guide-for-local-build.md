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

## Serving the site locally

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

```
git checkout MY-BRANCH-NAME
```

Then you can run 

```ruby
bundle exec jekyll serve
```

The browser will render your branch version.