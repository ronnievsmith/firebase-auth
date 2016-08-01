# Firebase v3 Web Auth Complete Working Example

:star: Please star me if you like this! :star:

### Synopsis

A fully functional example of Firebase v3 Web authentication.  Sign in with Facebook, Github, Google, Twitter, password based, and anonymous accounts.  The code is easy to read and follow and is well documented.  The focus is on the fully functional authentication system.

Password based users are sent a validation link.  They can also change their email address and password - both of these events send a verification email as an additional security measure.

Lastly, the difference between authentication, client side authorization, and server side authorization secured via Firebase Realtime Database Security Rules is demonstrated.


### Live Fully Functional Demo

:point_right:  [CLICK FOR LIVE DEMO](http://rack.pub/firebase-auth)  :point_left:

<img src="https://github.com/rhroyston/rhroyston.github.io/blob/master/firebase-auth.jpg" alt="screenshot">

### Motivation

Setting up all 6 types of authentication took me quite a while so I decided to create a template that I could use as a starting point for my Firebase v3 Web applications.  It occurred to me that I could share this with other developers.

### Installation

The easiest way to install this code is to clone or download it.  The following tasks must be done to get it working on your system.

1. **Prerequisites**
    1. A [Firebase Web project](firebase.google.com). :free:
    2. An IDE. What's an IDE?  Try [Cloud9](https://c9.io/). :free:
    3. A Github, Google, Facebook, and Twitter account. :free:
    4. Two email accounts. :free:

2. **Configure Your IDE**
    2. Create an HTML5 project.
    3. Install Firebase Tools.  `npm install -g firebase-tools`
    4. Using Firebase Tools command line, login to your Firebase project.  `firebase login --no-localhost `
    5. Using Firebase Tools command line, setup a Firebase project in the current directory. `firebase init`
    6. Clone this set of files and folders to your IDE. `git clone https://github.com/rhroyston/firebase-auth.git`
    7. Using Firebase Tools command line, push your IDE project to your Firebase project. `firebase deploy`
    8. View Firebase project in your browser.  Any broken images or errors?  Easy fix below.
    8. You may need to update `href`, `src`, and `background: url` in all JS, CSS, and all HTML files depending on your Web hosting folder structure .
        1. Use Find feature to search for both `href` and `src` and update as necessary.
        2. Browser Console will display any remaining incorrect paths errors. 
        3. Note script.js line 781 `privateLink.href = "../firebase-auth/private"` the `..` seems to be required.
        4. Once all pages render properly from Firebase Hosting (no broken images or console errors), continue.
    
3. **Configure Firebase**
    1. Enable all 6 forms of authentication.  Follow the instructions on configuring social media site settings.
    2. Customize the Email Action Handler URL to point to your Firebase Web app URL + '/ack', e.g. `https://my-app-1234/ack`.

4. **Login to Web app**
    1. Login using an oAuth provider.
    2. From the browser command line, use the exposed `demo.update('mynode','myKey','myValue')` method to add secure markup to your Realtime Database.
        1. A success message will show up in your browser console.
        2. You may need to update the `href` path to match your folder structure.
    ```javascript
    demo.update("markup","secureData","<div class=\"mdl-card__title\"> <h1 class=\"mdl-card__title-text mdl-color-text--white\">Secured Data</h1> </div><div class=\"mdl-card__supporting-text mdl-typography--headline\"> <p>This is a secure card. The HTML markup that renders this card is secured in the Realtime Database.  Access is determined server side so no matter what you do with JavaScript on your browser you will not be able to view this card unless you are authorized to.</p><p>Secured data can be markup, JSON, strings, numbers, etc. Your imagination is the limit!</p></div><div class=\"mdl-card__actions mdl-card--border intro-card-actions\"> <a class=\"mdl-button mdl-button--colored mdl-js-button mdl-js-ripple-effect\" href=\"../firebase-auth/\">Home</a></div>");
    ```

### Firebase v3 Authentication and Authorization Demo Walkthrough

1. **Login using each oAuth provider**
    1. Notice that updating email address or password options are not present in your Account page.
    2. Notice any extra links in the side menu drawer?
    3. Try Deleting your account.  What Happens?

2. **Register as a Password based user**
    1. Did you get a verification email?
    2. Can you view private data until you clicked the verification link?
    3. Can you change your password?
    4. Can you change your email address?
    5. Can you undo the email change by clicking the email change notification email revokation link?

3. **Logout**
    1. What links are present in the side menu drawer?
    2. Can you access private data?
    3. Can you view private data?


### Contribute

If you found a bug, have any questions or want to contribute please let me know, [ron@rack.pub](mailto:ron@rack.pub).

### License

Ron Royston, [https://rack.pub](https://rack.pub), [MIT License](https://en.wikipedia.org/wiki/MIT_License)