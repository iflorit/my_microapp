# MicroApp

Hackathon template to create a microapp

# Development

## Single Page Application (SPA)
A single-page application (SPA) is a web application or website that interacts 
with the web browser by dynamically rewriting the current web page with new data
from the web server, instead of the default method of the browser loading entire
new pages. The goal is faster transitions that make the website feel more like a
native app.

Ayoba Microapps are based on this concept and helps to external developers to
increase the functionalities of Ayoba.

## Ayoba integration

Ayoba provides a list of operations that can be used by external developers to retrieve some user allowed information.

Examples:
```
// send plain text
Ayoba.sendMessage("Hello Ayoba!")

// send multimedia files
Ayoba.sendMedia(`https://gph.is/28WrGiV`, `image/gif`)

// read user info
var userCountry = Ayoba.getCountry()

// ... check other samples in this repository 
```

Read the[official docs] to see all the available operations 

## Extra info
Please read these documents to develop a good SPA

*  https://en.wikipedia.org/wiki/Single-page_application
*  https://developer.android.com/guide/webapps/best-practices

## Contribute Microapp library
Pull requests are encouraged and always welcome. Pick an issue and help us out!

To work on this project: 

```
git clone https://xxx.git
````

# End-to-End test
You can test your microapp only after beeing published. Please visit the request form to prepare you microapp publication:

1. Request for a Microapp slot into Ayoba xxx@xxx.com
2. Provide the detailed info of your app
3. All the user info your app needs can be requested by a permission system while the user installs the app. Please make sure the permissions list is well requested
4. Deploy you microapp code in a public site



## How-to use the GitLab Pages CI to publish the microapp files
Using GitLab Pages, your microapp can be deployed and public visible to internet. E.g.

```
https://xpertai.gitlab.io/microapp/
````

This will allow you as a developer to publish your microapp without running a complete webserver. 

Follow the next steps to publish a microapp through this repo template:

1. Develop you microapp
2. Config your .gitlab-ci.yml
```
# This file is a template, and might need editing before it works on your project.
# Full project: https://gitlab.com/pages/plain-html
pages:
  stage: deploy
  script:
    - mkdir .public
    - cp -r * .public
    - mv .public public
  artifacts:
    paths:
      - public
  only:
    # choose your preferred source branch
    - master 
```
3. Commit your changes into your choosed source branch (e.g. master)
4. Confirm after the code integration to your choosed source branch, the pipeline runs and deploys your microapp

Check https://docs.gitlab.com/ee/user/project/pages/ for more info. 

# Bug Reporting
Bugs should be reported to ...
