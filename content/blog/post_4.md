---
title: "v0.2-beta Release Notes"
date: 2026-04-30
tags: ["release-notes"]
---
## News

### Call for Photos!
As the mobile release of Directory approaches, I'm searching for photos to be used in marketing! I'm looking for photos that look like authentic profile pictures with personality. Photos of couples or multiple partners are welcome!

If you or anyone you know would like to participate, you can send submissions to me directly at cecilia@meet.directory. I can offer $50 venmo or check for each photo I decide to use!

No AI slop here!

### Mobile App Registration has begun!
We got our DUNS number two weeks ago, which means the process of putting Directory on mobile app stores has officially begun! If all goes well, I'm hoping to get the beta version as-is onto Android and iOS within the next two weeks and then continue updating!

---
## Changes to the App
### New compatibility filtering
The biggest change to the app is a new addition to the filtering system. Previously the only filtering mechanism for compatibility was with tags. Tags can be anything- gender, identity, sports, foods, lifestyles -- and anyone can add more. If enough people join, I expect there to be lots and lots of tags. 

When all tags are treated equally and there are potentially many synonymous tags, its not entirely clear how to filter for basic compatibility on gender and orientation. So, in addition to custom tags, there are now a few built-in options to choose from in the profile editor:

<figure>
<div class="image-group">

![image broken](/blog/post_4/pic-friends.png)
![image broken](/blog/post_4/pic-friends-dating.png)
![image broken](/blog/post_4/pic-identify.png)
</div>
<figcaption>New options in profile settings to specify your relationship types and basic gender preference</figcaption>
</figure>


This was a hard choice, because to me the custom tagging system is the bread and butter of directory. Part of what initially felt special was that no labels were "baked in" or more important than any other. 

But I think the reality is most people are going to identify strongly with female, male, or nonbinary and have a strong preference for who they want to meet if they are using the app for dating. Hard-coding these into the app makes it much easier to onboard and navigate as a user.

If anyone has thoughts on how to do this better, I would love to hear them!

### Other new features in 0.2
- A smoother onboarding process
- touch to scroll now works on dropdown menus for mobile
- Location data!
	- Rough location data is captured on app start up. I'm using IP location which is not as accurate as data from location services, so use a generous search margin. We'll get there eventually.
	- Distance filter is now enabled
	- User's city is now displayed on profile
- Photos are now using a square 1:1 aspect ratio

### Invisible changes:
- Upgraded to Godot 4.6
- work on applications for mobile developer accounts
- continued work on mobile apps
	- support for native ios photo selection

### Changes for existing users
- Existing users will have all genders and relationship type preferences selected, as this was the default behavior before the update.  You can update these in the profile settings. 

- I plan to remove the basic relationship/identity tags I initially added such as "man", "woman", "poly" because they are now redundant. However if you feel strongly about one of these tags and want to keep it you can always recreate it!

- Your existing profile photos will appear smaller because they are in the original 4:5 aspect ratio. Re-uploading them will put them in the new aspect ratio.

- The first time you login, location will be updated. Existing users may not appear right away until they also have locations updated. If you're still not seeing any search results after a few weeks, please reach out to me.

### Terms and Privacy Policy Change
The privacy policy used to say that we do not collect location data, but plan to in the near future. Now it says that we collect
"coarse location data, with latitude and longitude rounded to three decimal places."

Previously the terms of service said this app was for NC residents only. However, I can't actually restrict mobile app store access by state, so I took this restriction out of the terms. But for now, I'll only be advertising in NC.

See the diffs [here](https://github.com/meet-directory/directory-website/commit/ea75cdd56d2de27642cea4d732f60c0614c001b3) and [here](https://github.com/meet-directory/directory-website/commit/5d1e045a1f8e9383ef375b0e19e897f2f52f6379).

---

In this early phase of development, feedback on the features and look and feel of the app is always welcome! You can send it to contact@meet.directory or directly in the app settings.

~ Cecilia
