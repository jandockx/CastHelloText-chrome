# Getting up and running with no change



## Register you Chromecast

Register the device for development with Google at
[Google Cast SDK Developer Console]. You are charged $5!

Do this first, as it takes 15 minutes to settle.
I followed [Registration / Devices]. Note that
the page that shows you the serial number ("as if you were casting *this* page") is the registration page,
not the documentation page.



## Fork the Google repo and clone

The original repo is at <https://github.com/googlecast/CastHelloText-chrome>. Fork it under your own account,
and clone a local copy.

My fork is <https://github.com/jandockx/CastHelloText-chrome>.



## Deploy the application to a webserver

Deploying is easy with github. I used
[project pages](https://help.github.com/articles/user-organization-and-project-pages/).
Just create a `gh-pages` branch, and push it. This also works with `https`, which is noted as required for Cast apps.

The sender app is now hosted at <https://jandockx.github.io/CastHelloText-chrome/chromehellotext.html>.



## Done

If you go to that URL with Chrome, you can cast, and it works.

Note that I didn't need to restart the Chromecast, as was described in
[Registration / Devices].

Note that you are using the receiver app hosted by Google, not yet the one in your own repo.





# Using my own receiver



## Register a new application

In [Google Cast SDK Developer Console / Applications], register a new application with the URL of the receiver app.

As name, I used `jandockx-CastHelloText`.

The receiver app is in the same repo at github, and served next to the sender app, at
<https://jandockx.github.io/CastHelloText-chrome/receiver.html>.



## Tell the sender app to use my receiver app

Copy / paste the `Application ID` into the sender app (`chromehellotext.html`, `applicationID` variable).



## Done

Commit, push, test.










[Google Cast SDK Developer Console]: https://cast.google.com/publish/#/overview
[Google Cast SDK Developer Console / Applications]: https://cast.google.com/publish/#/applications
[Registration / Devices]: https://developers.google.com/cast/docs/registration#RegisterDevice



