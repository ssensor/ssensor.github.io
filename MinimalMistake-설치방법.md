# Gem-based method Setup

Minimal Mistakes has been developed as a [Gem-based theme](http://jekyllrb.com/docs/themes/) for easier use, and 100% compatible with GitHub Pages when used as a remote theme.

## 참고 블로그

1. [Github Blog 만들기](https://velog.io/@eona1301/Github-Blog-Jekyll-minimal-mistakes)

## Installation-Window (default)

Jekyll is a Ruby gem. First, install Ruby on your machine. 

### Ruby Installation

The easiest way to install Ruby and Jekyll is by using the [RubyInstaller](https://rubyinstaller.org/) for Windows.

RubyInstaller is a self-contained Windows-based installer that includes the Ruby language, an execution environment, important documentation, and more.

1. Download and install a **Ruby+Devkit** version from [RubyInstaller Downloads](https://rubyinstaller.org/downloads/). 

   e.g. rubyinstaller-devkit 2.7.x(x86)

   > 여기서 가장 중요한 것은 **Jekyll은 32bit**이기에, 설치시 (x64)가 아닌 **(x86)**으로 진행해야합니다.
   > 이는 초기 설정시 제일 빈번하게 발생하는 세팅 오류이기 때문에, 꼭 신경써서 설치해주셔야 합니다.

2. Use default options for installation. Keep clicking `Next`

3. Select (1) MSYS2 Base and (3) MSYS2 and MINGW installation:  Type  1,3  as instructed. This is needed for installing gems with native extensions. You can find additional information regarding this in the [RubyInstaller Documentation](https://github.com/oneclick/rubyinstaller2#using-the-installer-on-a-target-system)

![image](https://user-images.githubusercontent.com/38373000/167570682-f7648fbd-0b19-4f82-a9d9-2fda064df8c2.png)



4. Open a new commandprompt(adminstration mode) from the start menu. The `PATH` environment variable becomes effective.



### NodeJS (8 or greater) / Gulp

Download and open the [NodeJS installer](https://nodejs.org/en/)

Install with default setting. 

It will also install 'Chocolatey' on the local machine. It is similar to package manager of `apt-get` for window programs.



Open a new  command prompt(administration) window, and update npm by

```
npm install -g npm

npm install -g --production windows-build-tools
```

![image](https://user-images.githubusercontent.com/38373000/167575585-519fe84d-a86b-4218-aab5-ae6e34cbc0a1.png)



(optional) Install Gulp CLI

```
npm install --global gulp-cli
```



### Jekyll Installation

Go to the directory where repository for github blog is installed.

Open a CMD window.

With Ruby installed, install Jekyll from the terminal:

```
gem install jekyll bundler

```

![image](https://user-images.githubusercontent.com/38373000/167576506-8bce70f2-c02d-4cc3-98c7-820ce1743b41.png)

   Check if Jekyll has been installed properly: `jekyll -v`

>  rake를 찾을 수 없다고 뜨는 경우  `gem install rake`를 이용해 받아주도록 합니다.

>  Jekyll이 잘 안되는 경우는 호환성 문제인 것 같은데, 이 때는 gem을 다운그레이드 하는 것도 해결책이 될 수도 있다고 합니다. 명령어 `gem update --system 2.5.0`을 실행 

#  

If Installation process is already done, go to **Running Local Server**



## Installing the theme

If you're running Jekyll v3.7+ and self-hosting you can quickly install the theme as a Ruby gem.

[^structure]: See [**Structure** page]({{ "/docs/structure/" | relative_url }}) for a list of theme files and what they do.

**ProTip:** Be sure to remove `/docs` and `/test` if you forked Minimal Mistakes. These folders contain documentation and test pages for the theme and you probably don't want them littering up your repo.

**Note:** The theme uses the [jekyll-include-cache](https://github.com/benbalter/jekyll-include-cache) plugin which will need to be installed in your `Gemfile` and added to the `plugins` array of `_config.yml`. Otherwise you'll throw `Unknown tag 'include_cached'` errors at build.
{: .notice--warning}



### Gem-based method

With Gem-based themes, directories such as the `assets`, `_layouts`, `_includes`, and `_sass` are stored in the theme’s gem, hidden from your immediate view. This allows for easier installation and updating as you don't have to manage any of the theme files. 

To install as a Gem-based theme:

1. Modify the following to your `Gemfile`:

   ```ruby
   source "https://rubygems.org"
   #gemspec
   gem "jekyll", "~> 3.7"
   gem "kramdown-parser-gfm"
   gem "minimal-mistakes-jekyll"
   ```

   

2. Fetch and update bundled gems by running the following [Bundler](https://bundler.io/) command:

   ```bash
   bundle      // bundle install
   ```
   

   
3. In the same directory, Install npm

   ```
   npm install
   ```

   

4. **For GITHUB Page,**  comment theme in your project's Jekyll `_config.yml` file:

   ```yaml
   # theme: minimal-mistakes-jekyll
   ```

   ![image](https://user-images.githubusercontent.com/38373000/167577152-4a51f913-421d-47fd-8676-f7625d6dde47.png)

5. Add `jekyll-include-cache` to the `plugins` array of your `_config.yml`.

   <img src="https://user-images.githubusercontent.com/38373000/167577433-523876a0-e78c-4fe1-b635-142a4583ccd4.png" alt="image" style="zoom:50%;" />

6. To update the theme run in CMD

   ```
   bundle update
   ```

7. Run the server

   ```
   bundle exec jekyll serve
   ```

8. Check the site in the local host: http://localhost:4000/





# Running Local Server

1. Modify contents
2. Execute:

    ```
     bundle
    ```

1. Run the server

   ```
   bundle exec jekyll serve
   ```

4. Check the site in the local host:  http://localhost:4000/ 






## 불필요한 폴더 제거

If you forked or downloaded the `minimal-mistakes-jekyll` repo you can safely remove the following folders and files:

- `.editorconfig`
- `.gitattributes`
- `.github`
- `/docs`
- `/test`
- `CHANGELOG.md`
- `minimal-mistakes-jekyll.gemspec`
- `README.md`
- `screenshot-layouts.png`
- `screenshot.png`



![img](https://user-images.githubusercontent.com/45550607/102005471-5a86c780-3d5c-11eb-8ad4-bc5fd466ed57.png)

docs 내부의 _pages 폴더는 추후 상단의 카테고리를 선택할 수 있는 양식이라,  참고용으로 사용하면  됩니다. 

> docs 내부의  _post, _docs 등도 메인 디렉토리에 복사해서 유용하게 사용할 수 있음

![img](https://user-images.githubusercontent.com/45550607/102005746-c407d580-3d5e-11eb-913a-bb2e36c54f4b.png)



## Style Modification

Also read:

* https://inhyeokyoo.github.io/github%20pages/tips-for-minimal-mistakes/

* https://www.fabriziomusacchio.com/blog/2021-08-11-Minimal_Mistakes_Cheat_Sheet/



You can modify the theme by changing the settings in `_config.yml` of Root Directory



**Note:** for technical reasons, `_config.yml` is NOT reloaded 	automatically when used with `jekyll serve`. If you make any changes to this file, please restart the server process for them to be applied.
	
For a full explanation of every setting be sure to read the [**Configuration**]({{ "/docs/configuration/" | relative_url }}) section.



**v4 Breaking Change:** Paths for image headers, overlays, teasers, [galleries]({{ "/docs/helpers/#gallery" | relative_url }}), and [feature rows]({{ "/docs/helpers/#feature-row" | relative_url }}) have changed and now require a full path. Instead of just `image: filename.jpg` you'll need to use the full path eg: `image: /assets/images/filename.jpg`. 



## Font size 변경하기

### Method 1: _resec.scss

- 수정 파일 : github.io 폴더 > _sass 폴더 > _minimal-mistakes 폴더 > _reset.scss

```scss
html {
  /* apply a natural box layout model to all elements */
  box-sizing: border-box;
  background-color: $background-color;
  font-size: 16px;                    // Default 16px;

  @include breakpoint($medium) {
    font-size: 16px;                  // Default 18px;
  }

  @include breakpoint($large) {
    font-size: 16px;                  // Default 20px;
  }

  @include breakpoint($x-large) {
    font-size: 16px;                  // Default 22px;
  }

  -webkit-text-size-adjust: 100%;
  -ms-text-size-adjust: 100%;
}
```

### Method 2: _resec.scss

 /[assets]/[css]/**main.scss**

폰트 사이즈만 오버라이딩하는 방법임.

```
---
# Only the main Sass file needs front matter (the dashes are enough)
---

@charset "utf-8";

@import "minimal-mistakes/skins/{{ site.minimal_mistakes_skin | default: 'default' }}"; // skin
@import "minimal-mistakes"; // main partials

html {
    font-size: 16px; // change to whatever
    @include breakpoint($medium) {
      font-size: 18px; // change to whatever
    }
  
    @include breakpoint($large) {
      font-size: 18px; // change to whatever
    }
  
    @include breakpoint($x-large) {
      font-size: 18px; // change to whatever
    }
}
```



# TOC 폰트 사이즈 수정

TOC 폰트 사이즈는 자동적으로 page width에 따라 가변되도록 설정되어 있다.  `_sass\minimal-mistakes\_navigation.scss` 파일에서 확인



H1~H4의 사이즈는  `_sass\minimal-mistakes\_variables.scss`에서 설정 가능.

```css
/* headline scale */
$h-size-1: 2.7em !default; // ~25.008px
$h-size-2: 2.0em !default; // ~20px
$h-size-3: 1.75em !default; // ~18px
$h-size-4: 1.5em !default; // ~17px
//$h-size-1: 1.563em !default; // ~25.008px
//$h-size-2: 1.25em !default; // ~20px
//$h-size-3: 1.125em !default; // ~18px
//$h-size-4: 1.0625em !default; // ~17px
$h-size-5: 1.03125em !default; // ~16.5px
$h-size-6: 1em !default; // ~16px

```





## Main index 변경하기

메인 디렉토리에  index.md 생성

예시:

```
---
layout: single  #splash
author_profile: true
title: Welcome to SSS LAB
---

```

레이아웃 테마를 splash 혹은 single로 선택



좋은 예시로 docs/home.md 를 참고하면 됨.

------



That's it! If all goes well running `bundle exec jekyll serve` should spin-up your site.



## Troubleshooting

### 1. Successful in Local Server but Build Error in Github Page
" theme" cannot be found error in Github build
### Solution

**For GITHUB Page,**  comment `theme` in your project's Jekyll `_config.yml` file:

