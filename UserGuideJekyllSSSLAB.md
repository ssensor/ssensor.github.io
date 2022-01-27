If Installation process is already done, go to **Running Local Server**



# Installation

## 1. Installation-Window (default)

Jekyll is a Ruby gem. First, install Ruby on your machine. 

### Ruby Installation

The easiest way to install Ruby and Jekyll is by using the [RubyInstaller](https://rubyinstaller.org/) for Windows.

RubyInstaller is a self-contained Windows-based installer that includes the Ruby language, an execution environment, important documentation, and more.

1. Download and install a **Ruby+Devkit** version from [RubyInstaller Downloads](https://rubyinstaller.org/downloads/). Use default options for installation.

   e.g. rubyinstaller-devkit 2.7.x(x64)

2. Run the `ridk install` step on the last stage of the installation wizard. This is needed for installing gems with native extensions. You can find additional information regarding this in the [RubyInstaller Documentation](https://github.com/oneclick/rubyinstaller2#using-the-installer-on-a-target-system)

3. Open a new command prompt window from the start menu, so that changes to the `PATH` environment variable becomes effective.

### NodeJS (8 or greater) / Gulp

Download and open the [NodeJS installer](https://nodejs.org/en/)



In cmd(administration), update npm

```
npm install -g npm

npm install -g --production windows-build-tools
```



(optional) Install Gulp CLI

```
npm install --global gulp-cli
```



### Jekyll Installation

   With Ruby installed, install Jekyll from the terminal:

   ```
   gem install jekyll bundler

   ```

   Check if Jekyll has been installed properly: `jekyll -v`

   # 

### Install bundle/npm in Git Directory

1. [Fork the repo](https://github.com/janczizikow/sleek/fork)(github blog)

2. Clone or download the repo into directory of your choice: `git clone https://github.com/your-github-username/sleek.git`

3. Go to the website git directory and Inside the directory run `bundle install`

   ```
   bundle install
   ```

4. In the same directory, Install npm

   ``` 
   npm install
   ```

   ​

5. If you want to use [gulp.js](https://gulpjs.com/) run `gulp` or `npm start`~~

   - ~~if you don't want to use gulp you can run `bundle exec jekyll serve` instead~~




#### Installing to existing jekyll project

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "jekyll-sleek"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: jekyll-sleek
```

"Gemfile"  should look as

```
# frozen_string_literal: true

source "https://rubygems.org"
#gemspec
gem "kramdown-parser-gfm"
gem "jekyll-sleek"
```

And then execute:

```
$ bundle
```



Run the server

 `bundle exec jekyll serve` 



## Installation-Linux on Window

 Windows Subsystem for Linux.

Open a new Command Prompt or PowerShell window and type `bash`.

 Next, update your repository lists and packages:

```
sudo apt-get update -y && sudo apt-get upgrade -y

```

Next, install Ruby. To do this, let’s use a repository from [BrightBox](https://www.brightbox.com/docs/ruby/ubuntu/), which hosts optimized versions of Ruby for Ubuntu.

```
sudo apt-add-repository ppa:brightbox/ruby-ng
sudo apt-get update
sudo apt-get install ruby2.5 ruby2.5-dev build-essential dh-autoreconf

```

Next, update your Ruby gems:

```
gem update

```

> It no permission is given (e.g. You don't have write permissions for the /var/lib/gems/2.5.0 directory.), then, edit /.bashrc
>
> `# Ruby exports`
>
> `export GEM_HOME=$HOME/gems`
> `export PATH=$HOME/gems/bin:$PATH`

Install Jekyll:

```
gem install jekyll bundler

```

# 



# Running Local Server

1. Modify contents

2. Execute:

```
$ bundle
```

3. Run the server

   ```
   bundle exec jekyll serve
   ```


4. Check the site in the local host

   http://localhost:4000/

   ​

---

## File Structure Overview

```bash
sleek
├── _includes	               # theme includes
├── _js	                       # javascript files (by default jquery will be included with the scripts inside)
├── _layouts                   # theme layouts (see below for details)
├── _pages                     # pages folder (empty by default)
├── _posts                     # blog posts
├── _sass                      # Sass partials
├── assets
|  ├── css	               # minified css files
|  ├── img                     # images and icons used for the template
|  └── js		               # bundled and minified files from _js folder
├── _config.yml                # sample configuration
├── gulpfile.js                # gulp tasks (tasks autorunner)
├── index.md                   # sample home page (blog page)
└── package.json               # gulp tasks
```

---







## Style Modification

You can modify the theme by changing the settings in `_config.yml`.



# Post Blogs

### Posts

Create a new Markdown file such as `2017-01-13-my-post.md` in `_post` folder. Configure YAML Front Matter (stuff between `---`):

```
---
layout: post # needs to be post
title: Getting Started with Sleek # title of your post
featured-img: sleek #optional - if you want you can include hero image
---


```

#### Images

Hero Image:  Title Image

*  To do so, just upload an image in `.jpg` format to `_img` folder. The name must before the `.jpg` file extension has to match with `featured-img` in YAML

Thumbnail Image:  On main 



In case you want to add a hero image to the post, apart from changing `featured-img` in YAML, you also need to add the image file to the project. To do so, just upload an image in `.jpg` format to `_img` folder. The name must before the `.jpg` file extension has to match with `featured-img` in YAML. Next, run `gulp img` from command line to generate optimized version of the image and all the thumbnails. You have to restart the jekyll server to see the changes. Sleek uses [Lazy Sizes](https://github.com/aFarkas/lazysizes) Lazy Loader for loading images. Check the link for more info. Lazy Sizes doesnt’t require any configuration and it’s going to be included in your bundled js file.

# Add Pages

