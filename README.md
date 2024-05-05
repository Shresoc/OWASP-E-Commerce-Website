
# Building an Ecommerce web-application with security implementation:
<img width="419" alt="SDLC" src="https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/8f130438-da2d-4c83-b85c-96d626f31373">



## Introduction

In this project, I built a web-application, “Baggon” is a web application developed for the purpose and for serving 
functions of a regular shopping website. Many attackers try to penetrate and 
exploit these kinds of web applicationThe prime motive to build this web-application and implement various security 
features over it to make it more secure enough so that there is a minimum 
chance of any attacker exploiting it. As security being the prime factor, various 
tools were used for testing the vulnerabilities.

## Requirements
a. Software Requirements
1. PHP 7 or Above
2. WAMP64 Ver 3.2.3.0
3. Notepad ++ for HTML and CSS
4. MySQL V10.4.17


b. Hardware Requirements
1. Windows 7 or Above
2. Intel i5 or Higher
3. Minimum of 2 GB RAM
4. 50 GB of HDD or SSD


## Graphical User Interface (GUI):
![Screenshot 2024-05-05 201609](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/6fc08258-79d0-4df8-b957-58d418235d32)

![Login PAge](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/9a17e1dd-5826-4289-a2dd-8339087aecf4)

![Index Page](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/fab9934b-84d3-46e7-81d7-f2f02bd2caac)

## Use Case and Abuse Case
![Use Case](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/29b2ed24-d902-4009-aa91-180543d8679c)

![Abuse Case](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/8513878d-1048-4405-9e58-497cdae158ed)

## Security Requirements

## 1. 
SQL Injection: SQL Injection is one of the most widely performed
attack by a majority of attackers worldwide. It can a severe threat to
the web-application, and is on the list of one of the major
vulnerability risk of OSWAP. In this attack, the attacker could get
in and change the data of the databases with an query input.

Mitigation- Input validation is required to mitigate this
type of attack. Passwords and Usernames must be validated over the
number of strings matched.

## 2.
CSRF Attack: Any attacker could fake being an authorized user who
has been authenticated already for submitting the request of user to
a malicious site.

Mitigation- This can be avoided by a feature called same origin policy, which check the request made to
the website is genuine or not.

## 3.
Broken Access Control: This could occur when there is no restriction
for the normal or registered user in the web-application. Meaning,
any user could gain admin privileges just by manipulating the URL
or the path of the website.

Mitigation- Various sessions were introduced and the users
were given the minimum privileges.

## 4.
Broken Authentication: Authentication is one of the most
important virtue needed in every web-application. As now every
attacker has long list of pre-defined passwords, any hacker could
use brute-force and get into anyone’s account.

Mitigation- Session management was done knowingly, it
was also tested manually. A minimum number of length for the
password was setup.

## 5.
Cross Site Scripting: It is one of the most common vulnerability of
any web-application. It is mainly focused on the client-side
services, where an attacker inserts a script to get into any user’s
account and exploit further. The malicious code can be put in the
servers if there is very-less-to-no input validation and sanitization.

Mitigation- Proper input validation and sanitization is
required to lessen the chances of these kinds of attacks.

## Database Design
![Data Base Design](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/fb1f5edd-3861-4fb3-926c-5d51db179957)
![DB2](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/0d693b2d-0878-4d74-84b5-5ffcd9b24df8)
![DB 4](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/c7429ca7-5fc9-499c-a15a-9d2207075b37)
![DB 3](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/83a9f355-2140-4d1b-81bf-7884ad82fc8e)
![DB 5](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/1fa93d5b-07d4-4ebd-81cc-1de7dd2a0118)


## Security Implementations:

## 1. SQL Injection: 
Proper Input Validation was taken into account for
the password and the email structure, where a certain length was
set which is around 5 to 15 letters long (for the password) input. If
the required data did not match the requirement during registration
or the login period, the web application would notify to enter the
valid email ID or password of that particular length and structure.

![SQL Injection SI](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/399bb7c6-dfad-47d7-8fe2-20c49bb7deac)

## 2. Clickjacking or CSRF: 
The same origin policy was applied to
secure the web application from clickjacking and CSRF attacks.
Proper sessions were maintained, which were interlinked through
different layers of providing different services on the webapplication.

![CSRF SI](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/6d45d14d-cd17-46ce-9b36-1e485a200107)

## 3. Broken Access Control: 
Again, sessions were maintained using
various IDs so that a normal user could not add the product to the
cart, one must need to login first to become a registered user. If one
tries to add a product to the cart, a message would be sent stating
“Please Login to Add in Cart!!”. Therefore, a normal user would
not have a registered user or an admin access.

![Broken Access Control SI](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/c2b18608-802a-456c-bf70-6bebd91e3f5f)

## 4. Broken Authentication:
A session_destroy function was
implemented so that once the user has logged out, the user would
need to re-login to access the registered user privileges. Proper
session handling and session destroying functions were managed
and implemented.

![Broken Authentication SI](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/2df5c913-06ee-4c8f-87e8-dd7eb70a04af)

## 5. Security Misconfiguration: 
Every un-necessary file or logs were
deleted along with the passwords and usernames of the same input
which were common were also removed from the database. The
application was kept up-to-date.


## Design and Architecture:

![Architecture](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/159ff417-99fa-4179-b89f-427f8018b0b0)


## Testing and Risk-Assessment:
I. Manual Testing:
During the manual testing both negative and positive cases were taken into
consideration and further were noted down.
a. Users could only login with valid e-mail Id and Password.
20

b. A user is only able to login if the details have been fulfilled during
the registration process.

c. User is only to view the list of products.

d. Only the admin could access the privileged pages.

e. Only admin could monitor the registered users and subscriptions.

f. Only admin could manage the orders

g. Only the registered users could book the products and add it to the
cart.

## Testing Tool:
There are various testing tools available. However, “SonarLint” was considered
here. It is a tool that checks if the proper coding guidelines have been followed
or not and points out all the bugs and errors present on the code for Javascript
and PHP.
![Sonar Lint 1](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/900f5657-6ae2-4d63-9cd2-69c524bc4485)

![Sonar Lint 2](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/1cece5a5-668a-4975-8a12-1d001037b27d)

## Code Review:

![Code Review](https://github.com/Shresoc/OWASP-E-Commerce-Website/assets/168186856/fc5db563-85a6-4c2c-8dec-d38dc3f55cad)

## Conclusion

A website will always be prone to vulnerabilities, although after the over-all
evaluation the website tends to look safe and secure. However, like every other
application even this would require a constant maintenance once it has been
deployed. All the software should be kept up-to-date with regular patching of
various bugs if there are to be found in the future. If there is any kind of add-on
or removal of the content then the whole web-application should be tested
again.

As this being a locally hosted web-application, it would naturally be having
some or the other limitations to it, which could be examined with its usage in
the future. Findings out vulnerabilities would make the application even more
secure in the future and would help in gaining the knowledge to make even
better web-applications with respect to security.

