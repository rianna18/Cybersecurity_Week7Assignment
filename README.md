# Cybersecurity Week 7 Assignment - rianna18

Time spent: 2 hour spent in total

## User Stories

The following **required** functionality is completed:

1. [x]  Required: Challenge 0 - User Authentication
2. [x]  Required: Challenge 1 - User Authentication Challenge 1
3. [x]  Required: Challenge 2 - User Authentication Challenge 2
4. [x]  Required: Challenge 3 - User Authentication Challenge 3
5. [x]  Required: Challenge 4 - Password Hashing 1
6. [x]  Required: Challenge 5 - Password Hashing 2
7. [x]  Required: Challenge 6 - Password Hashing 3

The following advanced user stories are optional:

* [ ]  Bonus 1: User Authentication Challenge 4
* [ ]  Bonus 2: Password Hashing 4

## Wordpress Exploits

1. WordPress 4.7 - User Information Disclosure via REST API
   * Description: The WordPress REST API provides a list of the users on a WordPress website without someone registering or having an account. Once a username is given, an attacker can use techniques such as Brute Force and Dictionary Attacks to guess the password.
   * Vulnerabilities: User Enumeration
   * Affected Version: WordPress 4.7
   * Fixed Version: WordPress 4.7.1
   * Source Code: https://github.com/WordPress/WordPress/commit/daf358983cc1ce0c77bf6d2de2ebbb43df2add60
   * Steps to recreate exploit: Change to WordPress Version 4.7. Go to example.com/wp-json/wp/v2/users, replacing example with desired WordPress site. Observe the userid, username, gravatar hash, and website URL.
   <img src='Week7Exploit1.gif' width='' alt='Video Walkthrough' />
   GIF created with [LiceCap](http://www.cockos.com/licecap/).

2. WordPress 3.3-4.7.4 - Large File Upload Error XSS
   * Description: There is an XSS vulnerability when attempting to upload very large files, because the error message does not properly restrict the presentation of the filename. This allows an attacker to inject a malicious script into the filename.
   * Vulnerabilities: Cross-Site Scripting (XSS)
   * Affected Versions: WordPress 3.3 - 4.7.4
   * Fixed Version: WordPress 4.7.5
   * Source Code: https://github.com/WordPress/WordPress/commit/8c7ea71edbbffca5d9766b7bea7c7f3722ffafa6
   * Steps to recreate exploit: Go to your WordPress site, click on Media > Add New. Drag or upload a picture that has a size greater than 2 MB. Observe the alert box saying the image is too large.
   <img src='Week7Exploit2.gif' width='' alt='Video Walkthrough' />
   GIF created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

This assignment was a bit challenging but allowed us to explore all the vulnerabilities we learned through a real world example.

## License

    Copyright [2017] [Rianna Jawa]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
