# BIO CWT | Wood Product Services - TESTING
---
Here you can find all of the testing that was performed on this website, also you will be able to find all of the bugs that were discovered during the development of this website.

Technical test reports are available upon following the link provided to each bug reported. Each bug will have its own technical test report with console log, network log and system info.

** **IMPORTANT** **<br>
Because this website was designed for mobile devices first please note when reweing the technical test reports in 'System Info' tab please refer to the 'Window:' column to have better understanding of the current dimensions in which the bug was found and reported.
---
## CONTENTS
---

* [Automated Testing - Validation Service](#Automated-Testing)
  * [W3C Validation HTML/CSS](#W3C-Validation)
  * [Lighthouse](#Lighthouse)

* [Manual Testing](#Design)

* [Bugs](#Features)
---
## AUTOMATED TESTING - Validation Service
 ### W3C Validator HTML
 All of the website's pages had their HTML checked by the W3C. The CSS was also validated using it.
* index.html - Returned 1 warning for self-closing tag syntax for linking a font-awesome library in html document, since this library was included in the begging of the project as a part of my custom boilerplate I've removed this library as I haven't used it anywhere.
* style.scss - Returned 4 errors and 22 warnings. <br>
```diff
- Error Nº 1 - Unrecognized at-rule ```@forward```, this rule is part of scss syntax which imports css from my globals folder.
---
- Error Nº 2 ```right``` is not a ```place-items``` value, this line since has been removed.
---
- Error Nº 3/4 - only ```0``` can be a ```unit```. You must put a unit after your number : x, since I was defining a grid I didn't realise I required a unit after my number which I thought would be inherited when using media queries, currently I've decided to use fr units which I thought would be appropariate and inline with responsive design.
---
! 22 Warning - I've used CSS variables thourgh out my project and CSS variables are presently not statically verified because of their dynamic nature.
```

 ### Lighthouse 
 To evaluate the website's performance, accessibility, best practises, and SEO, I utilised Lighthouse in the Chrome Developer Tools.
 ### Desktop Viewport
 ![Desktop Lighthouse](/README_Container/lighthouse.png)
 ![Desktop Lighthouse](/README_Container/lighthouse-errors.png)
#### Currently my page is underperforming on Perfomance and Accessibility categories mainly because of image format and not properly sized images. Most of my images that were used are in ```.png``` or ```.jpeg``` format. To rectify this issue and get higher scores I would require to convert and serve all of the images in next-get formats i.e ```.WebP``` and ```.AVIF``` because these often provide better compression which in return lead to less data consumption and helps to avoid enormouse network payloads. <br>
#### In addition to this I would also provide appropriately-sized images to save cellular data and improve load time. I will do this by having same image but in different size variants depending on the viewport image is being viewed on.
#### Lighthouse has flagged form elements do not have associated labels to ensure that form controls are announced properly by asistive technologies, like screen readers. The element that was failing is a chechbox which was used to create a hamburger menu. to rectify this issue I would require to create a label for this specific checkbox and specify this is a toggler for menu.
#### Cache static resources - to improve load time on repeated visits It would be best practice to configure the server to cache static resources using HTTP caching. This can be achieved by configuring the server to return ```Cache-Control``` HTTP response header. (Long cache lifetimes have the potential to prevent users from seeing static file changes. By configuring your build process to contain a hash in the filenames of your static assets, you may prevent this problem and force the browser to download the most recent version from the server.)
### WAVE
 ![WAVE](/README_Container/wave.png)
 ![WAVE](/README_Container/wave-form.png)
#### If a form control does not have a correctly matched text label, screen reader users may not be made aware of its function or purpose. I'll utilise the ```<label>``` element to link it to the appropriate form control in order to fix this problem.
---
## Manual Testing
### Testing User Stories -
### BIO CWT
|Gaol|How was this achieved?|
|---	|---	|
|Responsive Design|Grid Layout was used throught the development of the website|
|Design and accessibility that sets the client's service apart from the competition in a succinct way.|Pages were designed using figma there were no extra or unnecessary information, first load of the page displayed a clear message about the business and starting prices. In addition, color pallete didn't interfere with accessibility standards|
|Social Proofs|Landing page contains a distinc section 'Our Work' which contains a carousel with images of previously completed work|
|CTA aka call-to-action|CTA can be found at the top, bottom and middle of the page|
### First time visitors
|Goal|How was this achieved?|
|---	|---	|
|Type of wood supplied by the company|This information is accessible in the hero section of the landing page and 'the wood we work with' section|
|Estimated Cost|This information is accessible in the hero section of the landing page|
|For information to be easily accessible|For informationg to be easily accessible we decided to go with landing page style for the website, all of the information a first time visitor might require is available on one page, if the visior has any unanswered questions they can use the form at the bottom of the page to contact the business|
### Customers
|Goal|How was this achieved?|
|---	|---	|
|Up-to-date pricing|Currently not achieved|
|Contact Information|Contact information and contact form can be found at the bottom of the website and footer|
|Advantages of working with BIO CWT|Landing page contains a distinct section for the advantages of choosing BIO CWT as wood supplier|
### Profile visitors
|Goal|How was this achieved?|
|---	|---	|
|BIO CWT completed work for other customers|Landing page contains a distinct section which showcases completed work for other customers|

---
## BUGS

Navbar - hamburger Menu

Hamburger checkbox does not work properly, when user scrolls down the website checkbox doesn't stay fixed to the top of the website thus not allowing the user to open navigation menu.

Issue Status - Fixed <br>
Technical test report - "https://app.birdeatsbug.com/sessions/DilDCKCa4FsOZwo_g3cBphzNd1ssFPf6OwZvDYHLZXb_"

Bug resolution: Used z-index to position div.toggler on top of all of the elements while ::checked.

---

UX - Elements

User cannot fully interact with the website because a div.menu is taking up space while hidden. I was able to partially resolve the issue using z-index. This bug was discovered while creating a horizontally scrollable media.

Issue Status - Fixed <br>
Technical test report - "https://app.birdeatsbug.com/sessions/CgyDXRv1VtKHDi0EP8IIDPODEnROi-Dz5WKT7jC9PvU2"

Bug resolution: While targeting .nav-wrapper give it a height of 0.

---

UX - Elements

While viewing the website on smaller devices starting from 320px there is hidden overflow which is caused by the menu.

Issue Status - Present <br>
Technical test report - Not required.

---

UX - Responsiveness

While developing the website I didn't follow any responsive layouts which caused major problems and elements weren't scalling when viewed on different devices.

Issue Status - Fixed <br>
Technical test report - Not required.

Bug resolution - restructuring of the website from the beginning. Using grid layout so that elements scale for 4 most used viewport dimensions. (Desktop 1600x992px, Laptop 1280x802px, Tablet 768x1024px, Mobile 320x480px).