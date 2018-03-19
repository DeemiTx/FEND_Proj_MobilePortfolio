# Udacity Front-End Web Developer Nanodegree
## Project: Website Optimization


### Overview
Student needs to optimize website resources to achieve a minimum pageSpeed score of 90, achieve 60 FPS during scrolling and sub-five second pizzas resize.

### Installation
Install/download website resources using one of following methods and open index.html:
* Clone from GitHub - https://github.com/DeemiTx/FEND_Proj_MobilePortfolio.git
* Download as Zip file - https://github.com/DeemiTx/FEND_Proj_MobilePortfolio/archive/master.zip

Access website resources (index.html) using following URL:
* https://deemitx.github.io/FEND_Proj_MobilePortfolio/index.html

### Optimization Details

#### Enhancements to index.html to optimize PageSpeed score of atleast 90
* Images resized/optimized
* Inlined and minified CSS
* Used async attribute to prevent parser blocking
* Used Web Font Loader to load the Google web fonts asynchronously
* Used media attribute/query to unblock rendering
* Moved analytics code to the end and used async attribute to prevent parser blocking

Please see index.html for more details.  Comments prefixed by "Nadeem" are added all through the file to provide details on modifications.

#### Enhancements to main.js to optimize to 60 FPS during scrolling and resize pizzas in 5 ms or less
* Removed determineDx function and optimized changePizzaSizes function per Cameron's demo in lesson #8
* Optimized updatePositions function by moving some functionality out of loops
* Used getElementsByClassName and getElementById

Please see main.js for more details.  Comments prefixed by "Nadeem" are added all through the code to provide details on modifications.

### Modifications/updates (per Review #2 feedback)
#### main.js
* Line 448: Replaced querySelectorAll by getElementsByClassName
* Line 512: Saved items.length in local variable len to avoid accessing length at each iteration
* Line 515: Replaced 500 by 100 to ensure full screen coverage by background pizzas
* Line 537 & 538: Used window height to calculate number of rows and pizzas and used numPizzas instead of 200 in loop
* Line 541: Moved movingPizzas DOM call outside the loop and replaced querySelector with getElementById
* Line 542: Moved variable elem declaration to loop initialization to prevent repeated declarations
* Line 550: Replaced elem.basicLeft with elem.style.left

#### index.html
* Line 67: Resized pizzeria.jpg to 100x75 and updated img tag

#### miscellaneous:
* Resized pizzeria.jpg to 100x75 and created pizzeria100x75.jpg
* Restored pizza.png to original size
