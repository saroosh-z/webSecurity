# week8
#Saroosh Zaman
# Project 8 - Pentesting Live Targets

Time spent: **7** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* SQL Injection (SQLi)
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)



## Blue
Vulnerability #1: * Insecure Direct Object Reference (IDOR)
![IDOP](https://github.com/saroosh-z/webSecurity/blob/master/week8/gifs/insecure_OR.gif)

Vulnerability #2: * Session Hijacking/Fixation
![session_hijack](https://github.com/saroosh-z/webSecurity/blob/master/week8/gifs/sessionID.gif)



## Green
Vulnerability #1: SQL Injection
![sqli](https://github.com/saroosh-z/webSecurity/blob/master/week8/gifs/sqlInjection.gif)

Vulnerability #2: XSS
![xss](https://github.com/saroosh-z/webSecurity/blob/master/week8/gifs/xss.gif)



## Red
Vulnerability #1:  CSRF
![csrf](https://github.com/saroosh-z/webSecurity/blob/master/week8/gifs/csrf.gif)

Vulnerability #2: Enumeration
![enumeration](https://github.com/saroosh-z/webSecurity/blob/master/week8/gifs/userEnumeration.gif)


## Notes

Describe any challenges encountered while doing the work
session injection was the hardest one!
IDOR was way easier that I expected. 
CSRF was a good one to practice



## License
  Copyright 2017 Saroosh Zaman

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
