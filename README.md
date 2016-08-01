# Firebase v3 Web Authentication 
# Complete Working Example
### Synopsis

A fully functional example of Firebase v3 Web authentication.  Sign in with Facebook, Github, Google, Twitter; password based and anonymous accounts.
Password based users have their email address validated with an email containing a validation link; they can change their email address and password - both events send emails as an additional security measure.
Users of any sign in type can delete their account.  Lastly, the difference between authentication, client side authorization, and server side authorization secured via Firebase Realtime Database Security Rules is demonstrated.
The code is easy to read and follow and is well documented.  The focus is on the fully functional authentication system.
### Code Example

### [LIVE DEMO](http://rack.pub/firebase-auth)

<img src="https://github.com/rhroyston/rhroyston.github.io/blob/master/firebase-auth.jpg" alt="screenshot">

### Motivation

Setting up all 6 types of authentication took me quite a while so I decided to create a template that I could use as a starting point for my Firebase v3 Web applications.  It occurred to me that I could share this with other developers.

### Installation

:checkered_flag: Load via rack.pub's global CDN

The easiest way to install this example is to clone or download it.

:rocket:  Embed clock.min.js in your javascript when putting in production for best page loading performance.

### API Reference

```
demo.update('mynode','myKey','myValue')
```
> :point_right: although negligible in most cases, months and years are approximated for the `clock.since(timestamp)` and `clock.until(timestamp)` methods and the `clock.unit.months` and `clock.unit.years` properties.

### Contribute

If you found a bug, have any questions or want to contribute please let me know, [ron@rack.pub](mailto:ron@rack.pub).

### License

Ron Royston, [https://rack.pub](https://rack.pub), [MIT License](https://en.wikipedia.org/wiki/MIT_License)