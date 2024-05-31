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
Claas Augner (@caugner).

**Host:** Vadim (@pepelsbey)

## Intro and overview

[Vadim] Okay. Let's start with the first topic on our agenda.

## A new community manager introduction (@pepelsbey)

[Pranshu Khanna on GitHub](https://github.com/pransh15)

[Vadim] We have a new community manager joined MDN content team. Pranshu, introduce yourself.

[Pranshu] Awesome. Thank you so much for doing. Hi everyone. I'm Pranshu.

[Pranshu] I am the new community manager for NDN. I've been a Mozilla contributor for a while now.

[Pranshu] And yeah just excited to show in the team. I've been in and around open source almost all my career and life.

[Pranshu] At least young life and yeah, looking forward to. Working with all of you and seeing you every month.

[Vadim] I guess you're gonna be running the June community call.

[Vadim] Next time you'll see this. Pranshu is gonna be running the call instead of me.

[Vadim] Yeah, so I guess you already know Pranshu from our Discord and Discussions.

[Vadim] I think, MDN community is the is the most important part of this.

[Vadim] It's not just a bunch of teams. It's like everyone. So yeah, if you have any kind of questions or anything, Pranshu is your man.

[Chris] It's awesome. I'm really excited about you joining Pranshu and feel free to reach out to me if you have any questions about like old-school context of all of this crazy MDN thing because I've been around for a very long time.

[Chris] But yeah, seriously, happy to help with some of the stuff that you're doing because I think it's going to be really valuable for us.

[Pranshu] Thank you so much. I'll reach out and yeah, we'll jump on a call. So yeah.

[Vadim] Okay, so we have an official historian on the team as well.

[Chris] I prefer to think of myself as an archaeologist.

[Vadim] Alright.

[Eric Meyer] I mean it's nicer than how I refer to myself which is professional old person.

[Chris] Yep. Love it.

[Vadim] Moving on in the agenda, we have Curriculum updates from Chris.

## Curriculum updates (@chrisdavidmills)

[MDN Curriculum](https://developer.mozilla.org/en-US/curriculum/)

[Chris] Alrighty, hello folks. So as some of you already know, I wear two hats these days I have a Mozilla hat and a Google hat that I wear some of the time in the work I do on MDN with my Mozilla hat on today.

[Chris] And I'd like to draw your attention to some of the work that we've been doing for the MDN Curriculum.

[Chris] So we released the MDN Curriculum and it seems to have gone down fairly well. We've had quite a bit of interest from various folks in education and academia and industry and using it to support the kind of, you know, the knowledge that they need to, and make available via some of their educational projects. That's really cool.

[Chris] And but we've also been hard at work considering. Bringing on board kind of official education partners because one of the things about the curriculum is that it doesn't actually contain any learning material.

[Chris] It is a curriculum in the academic sense. It's basically a syllabus. This was deliberate, you know, there's so much awesome content already available on MDN that we thought it would be ridiculous to just repeat a load of it again.

[Chris] And but we also want to start linking out to some learning partners of various types. Some of these might be paid.

[Chris] We will definitely also include some free ones because we believe, you know, that everybody should be able to have access to this awesome educational experience that we're trying to project for free.

[Chris] As well as having the option to. Pay for a, a service to learn if they want to. So.

[Chris] Around June time. Can't really say much more about who yet but some of your probably have some guesses as to who is we're gonna announce our 1st educational partner so So watch this space and look out for it at some point in June.

[Chris] And it's, very interesting. As part of the process of selecting learning partners, we've been doing a whole ton of work reviewing their courses and

[Chris] Giving them a whole bunch of feedback on how to improve their their material. To make sure that it covers what we feel is the required amount of Samantics, accessibility, another kind of, you know.

[Chris] Evergreen information that we feel. Web developers need to. Create an awesome and accessible web. So that's been really valuable and a lot of them have been very receptive to that.

[Chris] So yeah, I see good things in this space. So, Yeah, watch out for more announcements about learning partners soon.

[Vadim] Thank you, Chris.

## Yari rewrite project (@fiji-flo)

[Yari: The platform code behind MDN Web Docs](https://github.com/mdn/yari/)

[Florian] I think we'll blog about it in the next few weeks. So I've been logging along to address quite some pain points.

[Florian] We have, and I. Can, happily say that for the past 6 week I've started the, Don't be scared.

[Florian] Them didn't rewrite project. So, will replace Yari with a successor that It's there to solve a lot of pain points.

[Florian] Over the past few years I tried to address a lot of this issue in and became clear that like some of them are like fundamental architectural issues and there's Yeah, the only way to solve them bottom up is to actually start from scratch.

[Florian] Which might sound scary, but it's not. I am quite close, as I said, like 6 weeks in.

[Florian] And it already ran was quite nice. And that's some of that was used already because I started to poke into different areas and fix some things in the.

[Florian] So I think the most important thing this will be like a parity rewrite. So, they should.

[Florian] Not be any visible change. And so everything renders exactly the same just that the engine is. You and then we do this to then like incrementally start improving things.

[Florian] Because it's written in a way that we can do this. there will be a few benefits.

[Florian] One of our pain points is, performance and that most likely we build that will be the yeah, most immediate impact is just like how long it takes to deploy a dot.

[Florian] And, and then like one of the benefits down the road is that we can hopefully have a That's some point this year do.

[Florian] For pure employment. So basically, changes will be reflected like like in the olden days when we had a week.

[Florian] So. Being parity with 4 years ago. And I think one thing to bring up, so as I said, I try to.

[Florian] Yeah, future parity. I do wanna do some improvements in, how things work. And One of the biggest changes is most likely the site bars.

[Florian] And don't get too excited. I don't want to change how the 5 bars look and feel because like that's been a conversation that Yeah, that will take a long time.

[Florian] When I do wanna change, I can. Put a link for branch of mine in the contact into the Chand and we probably can also just have this in the notes.

[Florian] Where's the chant?

[Florian] Yeah, if you do want to open that. So this would be like one of our, very comprehensive.

[Florian] So 1st that is a collection of a lot of links. Brinkled with some automation because we also like, automatically, scan up for this is as properties functions and whatnot in the middle of it.

[Florian] If that looks intimidating, I probably should have prepped to just show you like how it's currently generated because then you do see the I would say huge.

[Florian] Of it.

[Florian] Yes, so that's what it's replacing.

[Florian] Most important change is it moves into the content repository. So no more PRs to the build system if you want to change.

[Florian] Something that actually is content in a way. And it yeah it has another a lot of other like benefits it takes the titles out of the front better.

[Florian] Like currently all of this is translated in the macro which is Just doesn't have to be.

[Florian] I think. In that state right now it renders like the exact same HTML than the outside part us.

[Florian] And that is basically just this neat peak of. Changes that will come but I do wanna have this change from the go and These days, We have a slightly more pumping migration.

[Florian] When we switch systems or if I just back port this to, which I think is also not too much work.

[Florian] Yeah, I think.

[Florian] That it's, will open, I'll open up the ripple. Right now it's private because it's really quite messy for me because code moves a lot.

[Florian] But I get into to shape that. It still will be messy, but open that. The work can be forwarded transparently.

[Florian] I want to be sure to wait until it's inevitable and not get people excited and then disappoint

[Florian] Cool.

[Vadim] Yeah, thank you. And that's quite an improvement. We're going down from 1,500 to 300 lines of code.

[Vadim] That's That speaks for itself.

[Chris] Super exciting. It's going to be superb to be able to just edit things like side bars in the content repo and not have to try and do it in your very old time.

[Chris] That's amazing.

[Florian] And I think it also just. That's to the other topic that wanted to be discussed.

[Florian] So also clear intentions to move much, much more into the front better and 2. Also start start start using templates, more like, some of our work already, start to leverage this so when Jari was, we didn't have page types, we now have them and there's no reason why not Also a big shout out to everyone who worked on that and pushed for that.

[Florian] And something like proper page templates to to automatically add things like web compat, like browser compat and specification data.

[Florian] Is within, within reach. So. I hope and of the year. All of your life gets.

## Stalled PR discussion (@CBID2)

[Docs: making information about read-only clearer](https://github.com/mdn/content/pull/33193)

[Vadim] Thank you. Okay, we can give a chance to discuss this pull request. Christine if you're still up for it go ahead and unute yourself and we can we can talk about it or we can we can go to Discord.

[Christine] Hold on, let me just, let me just try and find it.

[Vadim] If anyone missed any parts of this this call, we're, we're, life-captioning this and, we're not gonna publish the full transcript, but we're gonna. Post some minutes. In the of this call later and the same repository.

[Christine] Alright, I just posted it. It's mostly that I need the update.

[Christine] One of the maintainer suggested, but I never really. Got notified. We'll follow up feedback.

[Christine] Even though I am tagged her. So.

[Christine] That's what it mostly is.

[Vadim] Hey, yeah, yeah, we will have a look at it and I see that Estelle is your viewing us and that you were talking on sometime like in April.

[Vadim] Yeah, I guess you can you can also, tag her again or, We can, some other people from commutes can have a look at this PR.

[Christine] Yeah. Alright.

[Vadim] Okay, thank you for bringing this up. You can, like I mentioned before, you can always, go to to our Discord and then ask for help there or just talk some from content team.

[Christine] Okay.

[Vadim] Someone from contributors will be there to help you.

[Ruth] Yeah, thank you, Christine. We, we can take a look at this one. If you have any in the future that get stools, just ping us in Discord.

[Vadim] Yep.

[Ruth] And we can pick them up. Alright, sorry this one has got stalled.

[Christine] Oh, sure, sure.

[Vadim] Good. And, that's it for today.

[Vadim] Yep, I guess we are. And, we're gonna be, we'll think about the next date for the community call, but it most likely gonna be end of June.

[Vadim] Look for announcement in a Discord or in the discussions we'll let you know once we have the final date.

[Vadim] And, we'll see each other. In June or in pull requests, you know.

[Vadim] See you around.

[Chris] Awesome, nice to see you all.

[Ruth] Thank you everyone.
