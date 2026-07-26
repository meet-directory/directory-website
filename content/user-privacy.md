---
title: "user-privacy"
type: page
---

<h2><span class="text-accent">Security and Privacy Considerations</span></h2>
<br>

This is not a legal document, but information for privacy-concerned users who want to know more about how Directory works.

### Threat Model
We consider cases where an attacker:
- has full access to source code and design documents
- may have their own user account on their own device
- does **not** have access to other users' devices

Like any mainstream dating app, this is an app where your data is accessible to
anyone with an account who fits most of your filter criteria, so anyone dedicated enough could find the data that you
display publicly.

### Geolocation
We never give exact location coordinates to the client. Distances are precomputed on the server and sent to the client.

#### Trilateration
Dating apps that show location distance (x miles away) are all subject to [trilateration attacks](https://digitalmarketreports.com/news/22960/six-dating-apps-expose-user-locations-to-stalkers-study-reveals/) that can allow anyone with an account to pinpoint an exact location of any user by getting the distance from three different points and then triangulating them to find exact coordinates.

We mitigate trilateration attacks by:
1. Only asking for rough location data on mobile apps (reports your
   neighborhood, not exact coordinates)
2. Using IP location on the browser app (usually granular to the nearest city)
3. Rounding any latitude and longitude data sent to our server to two decimal
   places before storing it in our database. This makes all location
   coordinates have about 1km of uncertainty.

- For reference, Grindr collects location data with [accuracy of up to 100 meters](https://help.grindr.com/hc/en-us/articles/1500009290262-Safety-tips).
- **Other mainstream apps have no statements on how accurate their location data is or how they mitigate this attack.**


### User Photos
- Photo metadata, including location data, is completely stripped from uploaded photos (in
  fact a whole new file is created and only the raw image is copied to the
  new file.)

### Data Mining
Directory profiles may include a user's age, aproximate location and any number
of self-reported interests. Naturally this could be valuable data to
third-parties. Directory does not give any data to third parties, but our
servers do use rate-limiting to prevent scraping from bots.

We can't prevent a user from logging in and simply writing down the data they
see on your profile, but we can somewhat prevent them from automating it on a large scale.

### Messaging
All webtraffic from Directory uses HTTPS, so your messages are encrypted in
transit. However they are stored in plaintext on our servers. Note that this is
the case for most online services. 

### Server/Database Security
We use Render to deploy our services with servers located in Virginia, US. So
their security is our security.


### Future Work
This is a volunteer project, given the time and resources we'd love to add more
security/privacy features, here are just a few:


- Use end-to-end encryption for messages so they are not readable on our servers.
- Provide face-blur/alteration for photos in the app
- Verified photos
- Give user profiles a "hidden tag" section where users can report interests
  that are used in the search algorithm but not publicly displayed.
- Make Directory resilient against widespread Denial-of-Service attacks. 
- Make app messages that auto-delete after 3 months so they are not on our servers.
- Add more protection against bots/spam


---

### Did we miss anything?
<section id="about-cta" class="text-center">
<p>If you have any privacy related questions or concerns, let us know!</p>
<a href="mailto:contact@meet.directory" class="btn mt-2">Contact Us</a>
</section>
