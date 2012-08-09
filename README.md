custom-downloads
================

Modification of default theme to display custom downloads on project pages

##Installation

First you need to modify index.html. Add following code to the ```<head>```:

```html 
<link rel="stylesheet" type="text/css" media="screen" href="http://cloud.github.com/downloads/simon-joseph/custom-downloads/custom_downloads.css">
```

Then you can add download links to ```<section id="downloads">``` with this code:

```html
  <a class="download_link" href="[URL_TO_FILE]">
    <div class="download_description">
      [STH]
    </div>
  </a>
```

Where ```[STH]``` is a short text, preferably file extension like .zip, .jar, tar.gz.

This also modifies default downloads so you need to change following lines:

```html
<a class="zip_download_link" href="https://github.com/[username]/[repo-name]/zipball/master">
  Download this project as a .zip file
</a>
<a class="tar_download_link" href="https://github.com/[username]/[repo-name]/tarball/master">
  Download this project as a tar.gz file  
</a>
```

into

```html
<a class="zip_download_link" href="https://github.com/[username]/[repo-name]/zipball/master">
  <div class="download_description">
    .zip
  </div>
</a>
<a class="tar_download_link" href="https://github.com/[username]/[repo-name]/tarball/master">
  <div class="download_description">
    tar.gz
  </div>
</a>
```
