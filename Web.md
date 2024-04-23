# Web Challenge Report: Finding the Flag in Source Code

## Overview

In this web challenge, the goal was to locate the flag on the website `https://redsystem.io/` without using brute force or fuzzing techniques. 

The challenge included inspecting various elements of the website to uncover hidden or less obvious areas where the flag might be stored.

## Methodology

### Initial Steps

1. **View Page Source:**
   - Accessed by pressing `Ctrl+U`.
   - This action reveals the raw HTML content of the website.

2. **Developer Tools:**
   - Accessed by pressing `Ctrl+Shift+I`.
   - Used to inspect elements, linked CSS, and script files.
   - Networking tab explored to check for fetch requests that load dynamic data.
   - Resources and storage explored for any hidden data.

### Additional Checks

3. **Robots.txt:**
   - Located at `https://redsystem.io/robots.txt`.
   - Used to determine which areas of the website web crawlers are restricted from accessing. This file sometimes contains paths that are not directly linked from the website, which might hold sensitive information.

4. **Sitemap:**
   - Accessed through `https://redsystem.io/sitemap.xml`.
   - Sitemaps provide a quick way to find all the pages on a website and are crucial for locating resources that might not be obvious from the homepage or other linked pages.

### Outcome

- After navigating through multiple layers, the flag was finally located deep in a script file.
- The process required not only a keen eye on the surface-level elements but also a deeper investigation into the structure and requests made by the web application.


## Conclusion

This challenge highlighted the importance of thorough inspection of all accessible web resources, not just those that are immediately visible. Tools like the page source viewer and developer tools were invaluable in dissecting the website's structure and ultimately led to the successful retrieval of the flag.

## Flags Found

- Two flags were discovered during this challenge, detailed exploration and strategic thinking were key to uncovering them in hidden parts of the website's structure.
