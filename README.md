# Web Security
# Project 7 - WordPress Pentesting

For this project, I used XSS and creating alerts on mouseHover, on a pageLoad and in an image.


## Pentesting Report

1. (Required) WordPress 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename
  - [x] Summary: This vulnerability allows attackers to create an image with an infected filename.   
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6
  - [x] GIF Walkthrough: 
    ![image] (https://github.com/saroosh-z/webSecurity/blob/master/gifs/XSS1_image.gif)
  - [x] Steps to recreate: 
         Create a new post on WP. Upload an image with the following name
          ``` animal<img src=a onerror=alert(1)>.png //animal is the filename```
  - [X] Affected source code:
  - [Link 1](http://wpdistillery.dev/wp-admin/upload.php?item=29)
  
2. (Required) WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [X] Summary: 
    This vulnerablity allows remote attackers to inject arbitrary web script or HTML via video URL in YouTube emebeds. infected code runs when the page is rendered.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6
  - [X] GIF Walkthrough: 
  - https://github.com/saroosh-z/webSecurity/blob/master/gifs/XSS2_embeddedLink.gif
  
  - [X] Steps to recreate: 
        Create a new page in WP and add the code in page's body. Code will be execcuted when page is rendered.
    ```[embed src='https://youtube.com/embed/123\x3csvg onload=alert(1)\x3e'][/embed]```
  - [x] Affected source code:
    - [Link 1] (http://wpdistillery.dev/?page_id=43)
3. (Required) WordPress <= 4.3 - Authenticated Shortcode Tags Cross-Site Scripting (XSS)
  - [x] Summary: A vulnerability that allows attackers to add infected HTML elements/tags on the page. In this example, when user hovers over the infected HTML, an alert window appears.
    - Vulnerability types: XSS
    - Tested in version:4.2
    - Fixed in version: 4.3
  - [X] GIF Walkthrough: 
  - https://github.com/saroosh-z/webSecurity/blob/master/gifs/XSS3_onhover.gif
  - [X] Steps to recreate: 
      Create a new post and add the infected HTML code in the post. Following code will be evecuted when user will hover over the text
  ```[caption width="1.5" caption='<a href="' ">]</a><a href="http://onmouseover='alert('1')'">You have won!</a>```  
  - [ ] Affected source code:
  - [Link 1](http://wpdistillery.dev/?p=76)

## Assets

List any additional assets, such as scripts or files
 - 3 gifs are added in the gifs folder

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)
- [technet(https://technet.microsoft.com/en-us/library/cc512662.aspx)]

GIFs created with [Peek](http://www.omgubuntu.co.uk/2016/08/peek-desktop-gif-screen-recorder-linux).

## Notes
- this assignment was interesting!

## License

    Copyright [2017] [Saroosh Zaman]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
