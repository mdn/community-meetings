# Minutes from MDN community meeting - 24th June 2024
**Attendees:** Ruth John (@Rumyra), Chris Mills (@chrisdavidmills), Vadim Makeev (@pepelsbey), Pranshu Khanna (@pransh15), Dipika Bhattacharya (@dipikabh), Christine Belzie (@CBID2), Florian Dieminger (@fiji-flo), Claas Augner (@caugner), Florian Scholz (@elchi3), Brian Smith(@bmsith), Andi Piper(@argl), Onkar Ruikar(@OnkarRuikar)

**Host:** Pranshu Khanna (@pransh15)

## Intro and overview

[Pranshu] Welcome to the June community call. If you're not a part of our discord community, please join the MDN community. While you're in MDN spaces, make sure that you follow the Mozilla community participation guidelines.

## Team updates

### Project updates from the MDN team (@rumyra/@pransh15)

[Ruth] Moving forward, we are planning to make community calls more focused.

We'll have one set focused on content, community, and contributing and another set focused on product and engineering, eg, what's happening with platform rewrites. Community members can join ones they are interested in.

We've also been talking about frequency of these calls and having some open office hours as well. Once we've made some decisions around that, we will communicate that. Am I right, Pranshu?

[Pranshu] Yes, that's correct. Please share if you any suggestions around office hours and content and community/product/engineering calls. We're very open to feedback and make this experience work for you.

[Chris] One of the things I was just gonna query like I assume like whatever the frequency ends up being you're just gonna sort of alternate between Product/Engineering and content. That's cool. Yeah, that totally makes sense. I also like the idea of having the odd office hours bit as well.

[Ruth] Yeah, something maybe a little bit less official and people can just come and talk about things that they need to talk about.

### Content Workshop Update (@rumyra)

[Ruth] We ran a couple of content workshops at the end of Q1 and I have been slowly putting together a plan for the content architecture is in the document side of it, not the UI side of it. And when we want to write things and where we want to put them. I'm putting together a presentation this week. I will be doing it finally hopefully on Thursday for which I'll receive feedback. I can then share the presentation with the community members and get feedback then as to what a good plan would be for content, but I just wanted it to give you an update. It hasn't fallen by the wayside.

[Pranshu] Sounds good.

### GitHub Week - 8th July (@rumyra)
[Ruth] The content and community team at Mozilla will be having a GitHub week. We try to do these once every 6 months. We'll be doing a bit of spring cleaning of our GitHub repositories, reviewing some of our processes, and looking at the pain points again.

We won't accomplish everything in a week, but it's a space for us to be able to focus specifically on GitHub organization and management and other tasks that we don't tend to do in our day-to-day. 

We'll make an announcement in GH Discussions, probably this week, with a few goals and what to expect. We will keep everybody informed with the things that we are actually doing.

[Chris] Is this just related to closing issues or is it a wider variety of things?

[Ruth] We will do some triaging and we will look at stale things. I think with Pranshu starting last month, it's a really good opportunity to look at the processes, the way that we track things, what our projects look like, and teams and access rights. All those aspects need to be sorted and reviewed periodically to make sure they're working for everybody.

[Onkar] Is it like inviting students to work on small tasks?

[Ruth] Not this one. This one will include the core team, the writers and Pranshu. We repeat this exercise every six months for iterating over and improving our processes and guidelines.

[Chris] That's great. It sounds super positive because I've noticed that OWD folks have been doing quite a bit of issue triage and stuff recently. So that's great and then Some of our volunteers have as well like Josh Chen has done absolutely loads of stuff recently closing a load of stale issues. I'm also wondering whether it would be worth spending a bit of your time kind of figuring out a way to highlight issues which would be good kind of You know. Like good 1st issue type things but not necessarily that but you know just sort of this is something that can be worked on without a massive mind field hassle, go crazy and run away screaming.

[Ruth] Yeah.

[Chris] I say this not purely just for kind of you know, regular. Flow of. Volunteer contributions but also it's worth having a bunch of those in hand for when you start to get efforts like Hacktoberfest and stuff piling onto your site.

[Ruth] Our previous community manager set up a project specifically for contributors. It would be a good idea to revisit that and see whether we can improve it. We also want to improve the workflow between contribution docs on MDN and what we have on GitHub because the flow is a little bit disjointed at the moment.

[Pranshu] Okay. Also reviewing PRs I mean if a new wave of contributors come in and just annoying everyone but with a lot of reviews right and if you're not supposed to be there It might just be easier to review the processes right now before have to professed before, you know, these students come in and yeah.

[Chris] Yeah, yeah. Absolutely.

### German Locale Project (@caugner)

[Claas] I believe it was 2 or 3 community calls ago in April. That we are experimenting with a German Locale on MDN and we've made some progress. We're waiting for one partner to come back to us to really announce it on GitHub. But what I can say is that we ran a survey in the context of the documentation. Of 5 days in the beginning of June. And we targeted those users and where the browser indicated German as their preferred language. And the survey asked, a couple of different questions.

First of all, with if German locale was available which locale would they use? Would they rather use the English locale? Or which, which most of them were on? Or would they, then what is it, proficiency in German and English? And, what would be important for them. Or a junk locale on NDM.

And overall we got, quite a lot of responses. In fact, 3% of all users who saw the survey responded and that indicates to us that the German speaking community is quite active and engaged. And that's, that's, useful, for, an experiment like this. Of those who responded to the survey, 90%, indicate that their native speakers are German. And 25%. I indicated that they would mostly use the German locale. And that's interesting considering that those people were on a non-German Page. And one of the explanations is that 33% of the survey respondents indicated that they're not fluid in English.

We know that. So those are the people who already visit MDN and so let's say MDN was available in Germany. Other people who are not comfortable visiting a page in English might, additionally come to come to to MDN. And this is one of the reasons why we want to experiment with that. To see can we attract a new audience mainly German speaking people that are not comfortable in reading documentation. And at the same time, I don't think we, said it, but what we will, what we plan on doing is machine translation.

Appearing in mind the general problems that that machine, that, will have. So we will use, LLM based translation because it turns out that LLM-based translations are much more consistent and coherent compared to traditional machine translation.

And we will iterate We saw the respondent that were interested in testing. To ensure that the quality of the translations are good enough. If the, the quality of the conjecture is good enough, then we will go live.

Yeah, and this is the reason why we asked for the kind of priorities. So we gave a couple of aspects that could that that and let's and the respondents rate them. What was rated the most important was technical correctness. Then the consistency of technical chance. But also, on rank 3 and 4 and there were 9, different aspects in total was completeness and comprehensibility. No, 3 and 4 was up-to-dateness and complete. And this and kind of confirms our plan to really, all of MDN. So that means, all of the MDN web docs. To be specific. So all of our 12,000 pages, into German and the sources of those it will be markdown files. They would be open, for edits. But the idea is that, changes as they happen in the English locale would be synchronized to that.

But Yeah, the community will review those changes will hopefully allow us to increase the the quality of those and translations. So we know that machine translations. Or, specifically, but also more generally, German translations of technical documentation doesn't often read great. But, what is the most important is that the people that feel more comfortable reading this, and find this helpful and useful. And obviously avoiding that there's like any, let's say any important issues introduced in the translation.

So all next steps is to have an internal test environment, and we will then share the first version of the German locale. With 300 Volunteers that are interested in this, and then we will iterate with those. And once we come to the conclusion that the quality is good enough we launched this in production. Yeah and so that might be around September - the launch in production. Any questions?

[Onkar]  Is Google Translating Pages helpful?

[Claas] I think it's a good question like, we do see in our server locks that some requests from Google can be stale and so we know that some folks are using Google Translate to exit. Although we don't have data on that, I assume it's not the best experience. Does it also, maybe, because it's probably delayed, you know, and, Yeah. We don't have, we don't have data on that. We could, we could have asked from you, service respondents. Although probably those using Google translates to browse MDN. What not have seen a survey on The second question is about converting images to a loud train station.

One of the aspects that we gave them gave the in the survey to rate was is it necessary to translate graphics? And it rated second but last just before translated cod examples actually. So we don't think it's it's that important. But yeah, it has to be taken to consideration. Now we have some charts. That are that really had English terms but we are already seeing those in some of the locates that we have.

Does that answer your question? Maybe you're referring to the shared-assets repository where the idea is to Also store the original versions like SVGs or Mermaid files. And it would be possible to use that to, to generate translated images. But based on the feedback. Based on the results of the survey. That is not as important and so that would rather come later down the line. As a nice to have.

[Pranshu] That's awesome.

[Chris] And one thing I just thought I'd bring up, then I'm not sure how helpful it will still be because it was quite a few years ago, but when I worked at Mozilla on MD and I did a survey specifically where You know, I asked a load of. Folks that used MDN for which English is not their 1st language in particular locales kind of you know I asked them to sort of compare an existing manually translated page that I thought looked fairly reasonable, IE. It was all translated and not just like the 1st sentence or whatever. With one that was done on the fly using Google Translate and I think another service too just to sort of see. If they thought the Google Translate. On the fly version was actually usable in any way or if it if it was like more usable than the manually translated versions sort of on average. And I seem to remember that kind of on average people kind of said, well, obviously it would be nice to have really beautiful, perfectly translated manual pages, but actually the Google Translated ones weren't too bad and they would be serviceable if that was kind of what was available. Of course, that was mainly in Latin-based languages such as those in Europe or languages like Chinese and Japanese the answer was at Big Fat No, it was very, very different. And so yeah, I'm not sure if that's still helpful stuff or if you'd be able to find that still hanging around somewhere. I know that Ruth has like a, you know, a giant document that like repository somewhere of all of my old crap from when I worked there.

[Claas] I think it's interesting that you mentioned also other languages, which is maybe, I mean, I, I can, mention that. So we go with, we went with, German because German, well, Germany is actually the country where we get most visits, most users, not now, use the page group, but it should be similar where we don't have a native language, available. So for us, it makes sense to kind of test with that. And then the second aspect is that. And the inherited German locale actually for 15 years between 2011 and 2022 if I'm not the and so it's it's a little more natural to to bring that okay back but it was retired in 2022 because it was incomplete and outdated. And this is what was what we would solve with an automated machine translation approach. And then if that is successful, then we can, think about extending that. Other languages. For example, I think the next language on the list. Would be depending on what you look at. Could be Italian, but also be Indonesian.

Yeah, and then a question from Florian about localizing strings in the UI. That was also one of the aspects and it's the 3rd last so the 7th of 9 aspects in terms of priority. That was having a user interface, that user interface. So again, we believe it. Well, it's on both results. It is not the most among the most important, things to tackle, but it's definitely on our agenda. We have some plan with after the rewrite that Florian is working on to also Work on the front end. Later this year or early next year and we definitely will look at making it possible to localize UI with that. But yeah, in

[Vadim] Have a feeling that The list of priorities will change from, locale to locale because for, German speakers, who are into web development, it's probably, they just have to know some basic English and it's it's enough for UI but for other other locales we might have to translate UI as well.

[Claas] Absolutely. That's a good point. And I think what we might, do, let's say if we take it another language, but again, like, 3, 2, I used to talk about that. We might use a similar approach, having a survey 1st to see the priorities and to understand like, if it makes sense because the the more down for the down we go with the list. Users we can potentially get and so it comes at some point it May not make sense or we won't be able to maintain this translation.

In a good enough quality. So at some point, that's like a point where. We have to say below that we may not be able. Yeah, to all the machine translations also. Will you not? Actually provide good enough quality translation for certain languages that are where there's less content available.

[Florian] I just wanted to add on like the translating UI is on our agenda. And macros is coming sooner. Actually like, planning to move that into content. So move the translations out of macros and like just have macros chasing for now in their content. Hopefully that will help with getting them translated because like a lot of them are like just translated in a handful of languages. And yeah, single for side bars. So all of that will be up and coming in the next couple of weeks.

[Pranshu] Awesome.

## Contributor Updates

[Pranshu] Next up, we don't have any contributor updates, but I would still like to remind you that we have a space for contributors updates. We're looking to feature you in the community call for the amazing work that you do.

## Questions and Discussions

### External Examples (@rumyra)

[Ruth] External examples. This was something that had started again discussed again on the GitHub organization in that we have a lot of repositories, a lot of examples in, we have a lot of opens and jazz fiddles and things on the website. We do want to start conforming these examples in the long term. We would like to integrate the playground a little bit better into the site. So initially It'll be really good if any contributors want to pull out any small examples from external example countries, ones that can be live samples and only in one maybe 2 pages.

If they cross like 5 pages, we'll keep them separate for now. And you're more than welcome to take them out of the repositories and put them into content. Cause that would be helpful. With live samples again that would also be helpful. Just FYI and when delete them if they're moved Pretty much for it.

Yeah, like see if we can't move some of the low hanging fruit into content pages, right? And then we will come up with a plan on how to actually structure bigger examples being a part of the repository.

As soon as we know more about the plan, which I'm working on in July, I will share it.

So yeah, maybe the problem is if if we don't remove them from the repository, we will not know which ones need to be moved further down the line. Which might make things difficult.

[Onkar] Maybe we need to create a spreadsheet.

[Ruth] Need to create a spreadsheet for each. Yeah, let's do that. Let's have an adventure.

[Claas] One thing we've done the past also is that when we maybe let's say delete one from content, we create an issue in the which is, content and then have a checklist for each locale.

[Florian] Yeah, I just also I hope that in the like early July I can just also move to working towards tooling. I think a lot of that is like, much, much easier in, the, in your world. I can some of that like if it's substantial work like refrain from it. I'm happy to help leveraging, making some of those things. And make it easier with the new build system like scraping out external links or any links is much much easier than currently, and faster. Don't don't get go dig into it but like I Publish the 1st pre-releases earlier today.

If you wanna get a get a rough feeling for what's up and coming, but yeah, but the polishing is missing. But especially when I learned like Chunking through macros and like broken links and some of that is so much easier if your iteration cycle is like a second or not Few minutes and I hope that will help like getting a lot of these. Yeah, 5 samples moved and like other issues resolved.

[Ruth] Thanks, Florian. That sounds really good. We're excited.Okay, so for example, then I think you're right, I think we need to create a spreadsheet. So we will think about that ASAP and what we will think about that ASAP and what we can do is we wanted to review that ASAP and what we can do is we wanted to review what external examples we wanted anyway because they're not all going to be able to review what external examples we wanted anyway because they're not all going to review what external examples we wanted anyway because they're not all going to be able to be live examples. So we need to figure out what's what and maybe once we've done that we will then have a list of the ones that can be moved and we can tell translated content.

[Pranshu] Should we create an issue or discussion for this so that it's easier to for everybody else to see?

[Ruth] Let us do the audit 1st and then we'll create a discussion which can link to the spreadsheet with the things that we want people to help us with. Yeah, cause you're right, yes we do, but I think we probably need a list first, don't we? And that we contributors can come in and take things off our list.

[Pranshu] Awesome! Looking forward to some progress in the next call.

[Ruth] Yeah.

### Is there an objective around closing issues? (@rumyra)

[Ruth] I had a question around closing issues because we have contributors closing lots of issues. I found out the answer earlier, which is there is no objective. People just wanted to come in and close loads of issues. So I guess the things. Mention here is you're gonna see a lot of activity over the next few weeks because some of our contributors are trying to reduce that issue count, which is fine. This is totally fine. Just because they want to. There was no other reason. They just wanted to do it. Which is cool.

### Inline icons [discussion](https://github.com/orgs/mdn/discussions/654#discussioncomment-9746229) (@rumyra)
[Ruth] The inline icons discussion on code. This is probably something most relevant to you, Onkar. This is the idea of putting experimental and deprecated icons throughout the site so not just in the side bars but making sure they're clear on pages and in our reference pages and things like that.

I want to see the vote on the discussion to see how maintainers feel we this should be done. But I don't think at this time it's a good idea for us to implement any way to do it because of the platform changes that are coming. So we have go through and have like, including macros and doing all of that kind of stuff and in like 3 months that'll all be mute and null because we'll be doing it in a completely different way.
 
[Florian] Yeah, I can also add on that's 1 of the things I realized that required inconsistent. So when I read it the side bars. Actually, I'm adding more of the where we previously did not. At them and I need to figure out if you wanna don't wanna have them.

[Ruth] Yeah, exactly.

[Florian] And, and at the same time it's it's quite easy like there's a global post processing of all links where we have this context so just injecting them is like really nothing to do.

[Ruth] That's what I'm trying to say on. Like I, I want people to vote. But no implementation to happen at this time, that's what I'm saying.

[Florian] I was wondering about one case I ran into and that I was not aware of like there's guide pages that have like a feature status is that

[Ruth] Yes, because they've got a BCD key. And we're using the BCD key for the baseline status.

[Florian] But the feature is it called feature status, don't get me wrong.

[Ruth] Okay. So yeah, I'm interested to see how maintainer feel about it. I think we also need to ask our users, but we can roll that into some decisions that we're gonna be making about the platform anyway. That's it for me.

#### Other Topics

[Onkar] Onkar needs a review on pull request. I think we can take that offline.

[Christine] How does someone become a maintainer for MD and Web Talks?

[Pranshu] Good question.

[Ruth] It's usually, someone who has around for a long time which is helping with poor request reviews and issue triaging and those kind of activities and then we take it on a case-by-case basis.

[Pranshu] We don't have a fixed guidelines yet. But I will be building those. So I will have a clear response for you in a few weeks, but, right now, just get involved, just get, get your hands dirty with issues, PRs, just help us out. Just, just like Onkar does here. Chris has here and a lot of good folks who are on the yeah, and After some time, I'll just add you to becoming a maintainer, honestly. It's as simple as that right now. But, I will get back to you with concrete guidelines. I'll reach out to you. And, yeah, we'll take it offline. No worries.

[Onkar] I'm being asked to convert an image to a SVG here, but I'm not well-versed with SVG, how to proceed? Can we have a tool hosted somewhere to convert P and G to SVG for other contributors?

[Brian] I can help you with that one Onkar. If you want, I've been doing a lot of the HTTP diagrams in the last couple of weeks. Mostly this has been redoing them from scratch, which has been okay if they're mermaids, then we have the Source for this afterwards. And otherwise, they're just boxes and lines. And this is pretty easy to recreate so I can give you a hand with that if you want.

[Ruth] Thanks, Brian.

[Pranshu] Awesome. So we don't have anything else on the agenda. One last important update that I wanted to share was that our next community call will be on the 23rd of July. 2024, which you, if you haven't guessed it yet, it's, MDN will turn 19. I hope to see all of you there.

Okay. Cool, awesome. Alright, so we still have 15 min. Which I happily give you back because it's Chris' birthday. So, alright, thank you so much to everyone for joining. And see you in the next one.
