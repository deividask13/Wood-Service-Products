# BIO CWT | Wood Product Services - TESTING
---
Here you can find all of the testing that was performed on this website, also you will be able to find all of the bugs that were discovered during the development of this website.

Technical test reports are available upon following the link provided to each bug reported. Each bug will have its own technical test report with console log, network log and system info.

** **IMPORTANT** **<br>
Because this website was designed for mobile devices first please note when reweing the technical test reports in 'System Info' tab please refer to the 'Window:' column to have better understanding of the current dimensions in which the bug was found and reported.
---
## CONTENTS
---

* [Automated Testing - Validation Service](#User-Experience)

* [Manual Testing](#Design)

* [Bug](#Features)
---
## AUTOMATED TESTING - Validation Service
---
## Manual Testing
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

Issue Status - Currently present <br>
Technical test report - "https://app.birdeatsbug.com/sessions/CgyDXRv1VtKHDi0EP8IIDPODEnROi-Dz5WKT7jC9PvU2"

Bug resolution: N/A