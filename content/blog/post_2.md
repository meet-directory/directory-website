---
title: "v0.1.1-beta Release Notes!"
date: 2026-04-05
tags: ["release notes", "Q&A"]
---

A few updates since our first release one week ago!

#### Bug tracking and open source migration
For those curious, we've released the [client code on
Github](https://github.com/meet-directory/directory-app)!  We'll
need to spend some more time working on a public contribution process, but for
now we are using Github to track bugs and issues. So for the more
developer-oriented users, feel free to [submit issues directly in
Github](https://github.com/meet-directory/directory-app/issues)!

#### Photo location data privacy
One user asked if we strip location data from photos-- and the answer is yes!

When you upload a photo, the client creates a new photo that is cropped and has
a lower resolution than the the original. It is this new file that is then sent to
the server. So the original exif data doesn't get transferred at all because it
is a new file.


#### New features/bug fixes
- photo upload works! (Something always has to go wrong on release day ^^')
- Previously, kinks were under the sex category, but someone reminded us that
  many people who practice kink aren't sexual at all! So we have renamed the
  "sex" category to "intimacy" and moved the "sex" tag under this category.
  We think this designation makes more sense and fits a broader array of tags.
- The search filter now allows you to only show unseen profiles.
- in-app user feedback form
- change your password in the app!
- Users now stay logged in for 21 days and no more server errors.
		There were some browser issues that would sign out the account or show a message that an error occurred when reaching the server. No longer!

#### Clipboard and Password manager compatability
We're aware that our login form is not yet compatable with password
managers and the clipboard behavior is a little janky (in Firefox, copy and
paste doesn't work at all!). It turns out this issue is a bit more complicated
than we thought and we likely won't have time to resolve it soon as we focus on upcoming mobile releases, but the issues [are being tracked](https://github.com/meet-directory/directory-app/issues/1)!

~ Cecilia
