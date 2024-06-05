# Minutes from MDN community meeting 29th May 2024

**Attendees:**
Ruth John (@Rumyra),
Chris Mills (@chrisdavidmills),
Vadim Makeev (@pepelsbey),
Pranshu Khanna (@pransh15),
Dipika Bhattacharya (@dipikabh),
Christine Belzie (@CBID2),
Eric Meyer (@meyerweb),
Florian Dieminger (@fiji-flo),
Claas Augner (@caugner),
Anuja (@AnujaRajput727),
Florian Scholz (@elchi3),
Natalia (@nataliaschlebinger)

**Host:** Vadim (@pepelsbey)

## Intro and overview

[Vadim] Okay. Let's start with the first topic on our agenda.

## A new community manager introduction (@pepelsbey)

[Pranshu Khanna on GitHub](https://github.com/pransh15)

[Vadim] We have a new community manager joined MDN content team. Pranshu, introduce yourself.

[Pranshu] Thank you. Hi everyone. I'm Pranshu. I am the new community manager for MDN. I've been a Mozilla contributor for a while now. I'm excited to join in the team. I've been in and around open source almost all my career and life. At least young life and yeah, looking forward to working with all of you and seeing you every month.

[Vadim] Pranshu will be running the next community call. Perhaps you all already know Pranshu from our Discord and GitHub Discussions.
MDN community is the is the most important part of our work. It's not just a bunch of teams, it includes everyone. So yeah, if you have any questions, Pranshu is your man.

[Chris] It's awesome. I'm really excited about you joining Pranshu and feel free to reach out to me if you have any questions about the old-school context of MDN because I've been around for a very long time. Happy to help with some of the stuff that you're doing because I think it's going to be really valuable for us.

[Pranshu] Thank you so much. I'll reach out and yeah, we'll jump on a call.


[Vadim] Moving on in the agenda, we have Curriculum updates from Chris.

## Curriculum updates (@chrisdavidmills)

[MDN Curriculum](https://developer.mozilla.org/en-US/curriculum/)

[Chris] Hello folks. As some of you already know, I wear two hats these days. I have a Mozilla hat and a Google hat. I have my Mozilla hat on today.

I'd like to draw your attention to some of the work that we've been doing for the MDN Curriculum. We released the MDN Curriculum and it seems to have gone down fairly well. We've had quite a bit of interest from various folks in education and academia and industry and using it to support the knowledge that they need to make available via some of their educational projects. That's really cool.

We've also been considering bringing on board official education partners. Because one of the things about the curriculum is that it doesn't actually contain any learning material. It is a curriculum in the academic sense. It's basically a syllabus. This was deliberate, there's so much awesome content already available on MDN that we thought it would be ridiculous to just repeat a load of it again.

But we also want to start linking out to some learning partners. Some of these might be paid. We will definitely also include some free ones because we believe that everybody should be able to have access to this awesome educational experience.

I can't really say much more about who yet but some of you probably have some guesses as to who is we're gonna announce as our 1st educational partner. So watch this space and look out for it at some point in June.

As part of the process of selecting learning partners, we've been doing a whole ton of work reviewing their courses and giving them feedback on how to improve their material to make sure that it covers what we feel is the required amount of semantics, accessibility, any information that we feel web developers need to create an awesome and accessible web. So that's been really valuable and a lot of them have been very receptive to that.

So yeah, I see good things in this space. Watch out for more announcements about learning partners soon.

[Vadim] Thank you, Chris.

## Yari rewrite project (@fiji-flo)

[Yari: The platform code behind MDN Web Docs](https://github.com/mdn/yari/)

[Florian] I think we'll blog about it in the next few weeks. So I've been trying to address quite some pain points. For the past 6 weeks, I've been working on the rewrite project to replace Yari with a successor to solve a lot of pain points.

[Florian] Over the past few years, I tried to address a lot of these issues and became clear that some of them are fundamental architectural issues and the only way to solve them bottom up is to actually start from scratch. This might sound scary, but it's not. I am quite close, as I said, like 6 weeks in.

The most important thing will be the parity rewrite. So, there should not be any visible change. And everything will render exactly the same. We do this to then incrementally start improving things.

[Florian] One of our pain points is performance and the most immediate impact will be how long it takes to deploy.

[Florian] For pure deployment, changes will be reflected like in the olden days when we had a wiki. So bringing parity with 4 years ago. And also build future parity. I do wanna do some improvements in how things work.

One of the biggest changes is most likely the sidebars.

[Florian] I don't want to change how the sidebars look and feel. Let me share a link for branch of mine: https://github.com/fiji-flo/content/blob/move-sidebars/files/sidebars/en-us/cssref.yaml. This is a collection of a lot of links, sprinkled with some automation.

Most important change is that it moved moves sidebars into the content repository. So no more PRs to the build system if you want to change something that actually is content in a way. The other benefit it has is that it takes the titles out of the front matter. Currently, all of this is translated in the macro which it doesn't have to be.

This is a sneak peak of changes that are coming. When we switch systems or if I just back port this to, which I think is also not too much work.

[Florian] I'll open up the repo. Right now it's private because it's really quite messy for me because the code moves quite a lot. The work can be forwarded transparently. I want to be sure to wait until it's inevitable and not get people excited and then disappoint them.

[Vadim] Yeah, thank you. And that's quite an improvement. We're going down from 1,500 to 300 lines of code.


[Chris] Super exciting. It's going to be superb to be able to edit things like side bars in the content repo and not have to try and do it in yari every time.

[Florian] That's to the other topic I wanted to be discussed. There's clear intentions to move much more content into the front matter and also start using templates, start to leverage page types. When we moved to Yari, we didn't have page types, we now have them and there's no reason why not leverage them. Also a big shout out to everyone who worked on page types and pushed for them.

We can have proper page templates to automatically add things like web compat, browser compat and specification data. This is now within reach. I hope by the end of the year, things will get better for all you.

## Stalled PR discussion (@CBID2)

[Docs: making information about read-only clearer](https://github.com/mdn/content/pull/33193)

[Vadim] We can give a chance to discuss this pull request. Christine if you're still up for it, go ahead and we can talk about it or we can we can discuss on Discord.


[Christine] It's mostly that I need an update. I've added what the maintainer suggested, I'm waiting for feedback.

[Vadim] I see that Estelle is reviewing this. You can tag her again or some other people from the community can have a look at this PR.

[Christine] Alright.

[Vadim] Thank you for bringing this up. Like I mentioned before, you can always go to to our Discord and ask for help there

[Christine] Okay.

[Ruth] Yeah, thank you, Christine. We can take a look at this one. If you have any in the future that get stalled, just ping us in Discord. Sorry this one has got stalled.

[Vadim] Good. And, that's it for today. We'll announce the next date for the community call, but it most likely will be around end of June. Look for announcement in Discord or in the GitHub Discussions. 

We'll see each other in June or in pull requests. See you around.

[Chris] Awesome, nice to see you all.

[Ruth] Thank you everyone.
