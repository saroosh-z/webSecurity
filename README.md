# Web Security
# Project 7 - WordPress Pentesting

For this project, I used XSS and creating alerts on mouseHover, on a pageLoad and in an image.


## Pentesting Report

1. (Required) WordPress 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename
  - [x] Summary: This vulnerability allows attackers to create an image filename that injects arbitary web web script. 
  
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6
  - [ ] GIF Walkthrough: 
  
  - [x] Steps to recreate: 
  Create a new post on WP.Upload an image with the following name
  '''animal<img src=a onerror=alert(1)>.png //animal is the filename'''    
  - [ ] Affected source code:
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
2. (Required) WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [X] Summary: 
    This vulnerablity allows remote attackers to inject arbitrary web script or HTML via video URL in YouTube emebeds.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6
  - [ ] GIF Walkthrough: 
  
  - [X] Steps to recreate: 
  Create a new page in WP and add the code in page's body. Code will be execcuted when page is rendered.
    ```
    [embed src='https://youtube.com/embed/123\x3csvg onload=alert(1)\x3e'][/embed]
    ```
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
3. (Required) WordPress <= 4.3 - Authenticated Shortcode Tags Cross-Site Scripting (XSS)
  - [x] Summary: A vulnerability that allows attackers to add HTML elements/tags
    - Vulnerability types: XSS
    - Tested in version:4.2
    - Fixed in version: 4.3
  - [ ] GIF Walkthrough: 
  - [X] Steps to recreate: 
  Create a new post and add the infected HTML code in the post. Following code will be evecuted when user will hover over the text
  '''[caption width="1.5" caption='<a href="' ">]</a><a href="http://onmouseover='alert('1')'">Over here!</a>'''
  
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
