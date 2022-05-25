---
layout: single
title: MD Link in Jekyll
---

# How to use MD Link

## Works for both github and local
#### For big category page, ues permanent link
#### For small category page, use built html.  If they are under root\docs\ , then use /docs/filename,  without extension
* [Using built html](/docs/researchImage)
* [Using built html](/docs/researchAI)
* [Using Permanent link](/researchImg)
* [Using permanent link2](/research/DIP)

## Only on github
* [Using md file link](/researchImage.md)
* [Using md file link 2](researchImage.md)
* [Using md file link](/researchImage2.md)


# Link within the page
[Emphasis](#emphasis)

<a name="emphasis"/>
#Emphasis
Link goes here

-----

# how to link images in MD under sub folders


### Light-Weight Object Detection with SORT for Object Tracking
1. (git only)

<img src=".\research\images\demo.gif" alt="demo" style="zoom:50%;" />
[YOffleNet Deep Sort in PyTorch](https://github.com/hkim1207/2021MIP)

2. (git only)

<img src="./research/images/demo.gif" alt="demo" style="zoom:50%;" />

3. (none)

<img src="docs/research/images/demo.gif" alt="demo" style="zoom:50%;" />


4 (both)

<img src="../docs/research/images/demo.gif" alt="demo" style="zoom:50%;" />


5 (web only)

<img src="https://ssensor.github.io/docs/research/images/demo.gif" alt="demo" style="zoom:50%;" />
