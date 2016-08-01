# Firebase v3 Web Auth Complete Working Example
### Synopsis

A fully functional example of Firebase v3 Web authentication.  Sign in with Facebook, Github, Google, Twitter; password based and anonymous accounts.
Password based users have their email address validated with an email containing a validation link; they can change their email address and password - both events send emails as an additional security measure.
Users of any sign in type can delete their account.  Lastly, the difference between authentication, client side authorization, and server side authorization secured via Firebase Realtime Database Security Rules is demonstrated.
The code is easy to read and follow and is well documented.  The focus is on the fully functional authentication system.

### Live Fully Functional Demo

:point_right:  [CLICK FOR LIVE DEMO](http://rack.pub/firebase-auth)  :point_left:

<img src="https://github.com/rhroyston/rhroyston.github.io/blob/master/firebase-auth.jpg" alt="screenshot">

### Motivation

Setting up all 6 types of authentication took me quite a while so I decided to create a template that I could use as a starting point for my Firebase v3 Web applications.  It occurred to me that I could share this with other developers.

### Installation

The easiest way to install this code is to clone or download it.  The following tasks must be done to get it working on your system.

1. Prerequisites
    1. Create a [Firebase Web project](firebase.google.com).
    2. Install Firebase Tools in your IDE. I recommend Cloud9 if you do not have a preference.  It is free.
    3. You will need a Github, Google, Facebook, and Twitter account.
    4. You will need 2 email accounts

2. Configure Firebase
    1. Enable all 6 forms of authentication.  Follow the instructions on configuring social media site settings.
    2. Customize the Email Action Handler URL to point to your Firebase Web app URL + '/ack'
    3. From your IDE command line, use Firebase Tools to login to your Web project
    4. Using Firebase Tools, init your project

3. Install the firebase-auth project files
    1. Clone the repo to your IDE.
    2. Note script.js line 781 `privateLink.href = "../firebase-auth/private"` the `..` is required
    3. Update `href` and `src` as necessary to work with your Web hosting folder structure in all JS, CSS, and all HTML files.

4. Login to Web app
    1. Once pages render ok login using an oAuth provider
    2. From the browser command line, use the exposed `demo.update('mynode','myKey','myValue')` method exactly as follows:
    ```javascript
    demo.update("markup","secureData","<div class=\"mdl-card__title\"> <h1 class=\"mdl-card__title-text mdl-color-text--white\">Secured Data</h1> </div><div class=\"mdl-card__supporting-text mdl-typography--headline\"> <p>This is a secure card. The HTML markup that renders this card is secured in the Realtime Database.  Access is determined server side so no matter what you do with JavaScript on your browser you will not be able to view this card unless you are authorized to.</p><p>Secured data can be markup, JSON, strings, numbers, etc. Your imagination is the limit!</p></div><div class=\"mdl-card__actions mdl-card--border intro-card-actions\"> <a class=\"mdl-button mdl-button--colored mdl-js-button mdl-js-ripple-effect\" href=\"../firebase-auth/\">Home</a></div>");
    ```

### Firebase v3 Authentication and Authorization Demo Walkthrough

1. Login using each oAuth provider
    1. Notice that updating email address or password options are not present in your Account page.
    2. Notice any extra links in the side menu drawer?
    3. Try Deleting your account.  What Happens?

2. Register as a Password based user
    1. Did you get a verification email?
    2. Can you view private data until you clicked the verification link?
    3. Can you change your password?
    4. Can you change your email address?
    5. Can you undo the email change by clicking the email change notification email revokation link?

3. Logout
    1. What links are present in the side menu drawer?
    2. Can you access private data?
    3. Can you view private data?


### Contribute

If you found a bug, have any questions or want to contribute please let me know, [ron@rack.pub](mailto:ron@rack.pub).

### License

Ron Royston, [https://rack.pub](https://rack.pub), [MIT License](https://en.wikipedia.org/wiki/MIT_License)