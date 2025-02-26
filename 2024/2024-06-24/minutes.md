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

[Chris] So, whatever the frequency ends up being, you're just gonna alternate between Product/Engineering and content? That's cool and makes sense. I also like the idea of having office hours.

[Ruth] Yes, the idea is to have something less official so people can join and talk about things they're working on or want to talk about.

### Content workshop update (@rumyra)

[Ruth] We ran a couple of content workshops at the end of Q1. I have been slowly putting together a plan for the content architecture (excluding the UI side of it). I'm putting together a presentation this week. I will hopefully present on Thursday and get some feedback. I can then share the presentation with the community members and get more feedback as to what a good plan would be for content. I just wanted to give you an update that there is progress happening and that it hasn't fallen by the wayside.

### GitHub Week - 8th July (@rumyra)

[Ruth] The content and community team at Mozilla will be having a GitHub week. We try to do these once every 6 months. We'll be doing a bit of spring cleaning of our GitHub repositories, reviewing some of our processes, and looking at the pain points again.

We won't accomplish everything in a week, but it's a space for us to be able to focus specifically on GitHub organization and management and other tasks that we don't tend to do in our day-to-day. 

We'll make an announcement in GH Discussions, probably this week, with a few goals and what to expect. We will keep everybody informed with the things that we are actually doing.

[Chris] Is this just related to closing issues or is it a wider variety of things?

[Ruth] We will do some triaging and we will look at stale things. I think with Pranshu starting last month, it's a really good opportunity to look at the processes, the way that we track things, what our projects look like, and teams and access rights. All those aspects need to be sorted and reviewed periodically to make sure they're working for everybody.

[Onkar] Is it like inviting students to work on small tasks?

[Ruth] Not this one. This one will include the core team, the writers and Pranshu. We repeat this exercise every six months for iterating over and improving our processes and guidelines.

[Chris] That's great. It sounds super positive because I've noticed that OWD folks have been doing quite a bit of issue triaging recently. Some of our volunteers like Josh Chen have also done loads recently and closed a lot of stale issues.

I'm wondering whether it would be worth spending some time figuring out a way to highlight good first issues. This would help with regular flow of volunteer contributions but will also be useful for events like Hacktoberfest.

[Ruth] Yeah. Our previous community manager set up a project specifically for contributors. It would be a good idea to revisit that and see whether we can improve it. We also want to improve the workflow between contribution docs on MDN and what we have on GitHub because the flow is a little bit disjointed at the moment.

[Pranshu] Also reviewing PRs is important. If a new wave of contributors comes in, it will be overwhelming for everyone with the number of reviews. It might just be easier to review the processes right now before these students and contributors come in.

### German locale project (@caugner)

[Claas] In April, we shared that we are experimenting with the German locale on MDN. We've made some progress. We're waiting for a partner to come back to us before announcing it on GitHub.

What I can share now is that we ran a survey in the beginning of June, targeting users whose browsers indicated German as their preferred language. In the survey, we asked their preferred locale if German locale was available, their proficiency in German and English, and what they think is important in the German locale on MDN.

We got a lot of responses. In fact, 3% of all users who saw the survey responded, which indicates to us that the German-speaking community is quite active and engaged. This is useful for such an experiment. Of those who responded to the survey, 90% were native German speakers, and 25% indicated that they would mostly use the German locale. This is interesting considering that those people were on a non-German Page. One of the explanations is that 33% of the survey respondents indicated that they're not fluent in English.

So these are the people who already visit MDN and if MDN is available in German, other people who are not comfortable visiting a page in English might additionally come to MDN. This is one of the reasons why we wanted to run this experiment - to see if we can attract a new audience, mainly German-speaking people, that is not comfortable in reading documentation in English.

Keeping in mind the general problems that machine translations have, we will use LLM-based translations because they are much more consistent and coherent compared to traditional machine translations.

We saw respondents who were interested in testing to ensure that the quality of the translations is good enough. If the quality of translation is good, we will go live.

This is the reason we asked for priorities and let the respondents rate them. What was rated the most important was technical correctness. Then the consistency of technical terms, followed by up-to-dateness, completeness, and comprehensibility. This confirms our plan to translate all of MDN to German, so all of our 12,000 pages. The source for these will be markdown files. They would be open for edits. The idea is that as changes happen in the English locale, they would be synchronized to that.

The community will review those changes to help us increase the quality of translations. We know that machine translations, and more generally, German translations of technical documentation, don't often read great. But what's most important is that the people who feel more comfortable reading in German find this helpful and useful. And obviously avoiding any important issues introduced in the translation.

So our next steps are to have an internal test environment, and we will then share the first version of the German locale with 300 volunteers who are interested in testing, and then we will iterate with those. Once we come to the conclusion that the quality is good enough, we'll launch this in production. This might be around September - the launch in production. Any questions?

[Onkar]  Is Google Translate helpful for translating pages?

[Claas] That's a good question. We see in our server logs that some requests from Google can be stale, so we know that some folks are using Google Translate. Although we don't have data on this, I assume it's not the best experience. It's probably also delayed. We could have asked survey respondents, for those using Google Translate to browse MDN. But they would not have seen the survey.

About the second question about converting images to translated versions: one of the aspects we asked in the survey was to rate the necessity to translate graphics. It rated second to last, just before translating code examples, so we don't think it's that important. But yeah, it has to be taken into consideration. Now we have some charts that have English terms but we are already seeing those in some of the locates that we have.

Does that answer your question? Maybe you're referring to the shared-assets repository where the idea is to also store the original versions like SVGs or Mermaid files. It would be possible to use that to generate translated images. But based on the results of the survey, this is not as important and would rather come later down the line as a nice-to-have.

[Chris] One thing I just thought I'd bring up, though I'm not sure how helpful it will still be because it was quite a few years ago, is that when I worked at Mozilla on MDN and I did a survey specifically asking folks that used MDN and for whom English is not their 1st language, to compare an existing manually translated page that I thought looked fairly reasonable, with one that was done on the fly using Google Translate and probably another service.

The idea was to see if they thought the Google Translate version was usable in any way or more usable than the manually translated versions on average. I seem to remember that on average, people said that while it will obviously nice to have perfectly translated pages, but that the Google Translated ones weren't too bad and they would be serviceable if that was what was available. Of course, that was mainly in Latin-based languages such as those in Europe. For languages like Chinese and Japanese, the answer was a big fat no; it was very, very different.

I'm not sure if that's still helpful or if you'd be able to find that data still hanging around somewhere. I know that Ruth has a giant document like repository somewhere of all my old stuff from when I worked there.

[Claas] It's interesting that you mentioned other languages. We went with German because Germany is the country from where we get the most visits and most users, where we don't have a native language available. So it makes sense to test with that. The second aspect is that we had the German locale for 15 years, between 2011 and 2022, so it's a little more natural to to bring that back; it was retired in 2022 because it was incomplete and outdated. We would solve this with an automated machine translation approach. And if successful, we can think about extending it to other languages. For example, I think the next language on the list could be Italian or Indonesian.

Regarding the question from Florian about localizing strings in the UI, this was also one of the aspects we considered. It ranked 7th out of 9 in terms of priority. It is not the most important thing to tackle, but it's definitely on our agenda. We have some plan to work on the front end later this year or early next year after the rewrite that Florian is working on. We definitely will look at making it possible to localize the UI.

[Vadim] I have a feeling that the list of priorities will change from locale to locale. For German speakers who are into web development, they just have to know some basic English to understand the UI, but for other other locales, we might have to translate the UI as well.

[Claas] Absolutely. That's a good point. I think for other languages, we might use a similar approach, that is conducting a survey first to see the priorities and to understand if it makes sense, and at some point, it may not make sense or we won't be able to maintain high-quality translation. At some point, machine translations might not be good enough quality for certain languages.

[Florian] I just wanted to add that translating the UI is on our agenda. Macros are coming sooner. We're planning to move that into content. Hopefully that will help with getting them translated because a lot of them are translated in only a handful of languages. And yeah, same for side bars. All of this will be up and coming in the next couple of weeks.

[Pranshu] Awesome.

## Contributor updates

[Pranshu] Next up, we don't have any contributor updates, but I would still like to remind you that we have a space for contributors updates. We're looking to feature you in the community call for the amazing work that you do.

## Questions and discussions

### External examples (@rumyra)

[Ruth] External examples. We have a lot of repositories, a lot of examples, and a lot of JSFiddles. We do want to start conforming these examples in the long term. We would like to integrate the playground a little bit better into the site. So initially it'll be really good if any contributor wants to pull out any small example from external example repositories, ones that can be live samples and only in one or two pages. If they cross five pages, we'll keep them separate for now.

You're more than welcome to take them out of the repositories and put them into content because that would be helpful. It will also be helpful with live samples. Just FYI, when they're moved, they can be deleted from the repositories.

And then we will come up with a plan on how to actually structure bigger examples being a part of the repository. As soon as we know more about the plan, which I'm working on in July, I will share it.

So maybe the problem is if we don't remove them from the repository, we will not know which ones need to be moved later, which might make things difficult.

[Onkar] Maybe we need to create a spreadsheet.

[Ruth] Yes, let's create a spreadsheet for each

[Claas] One thing we've done in the past is that when we delete one from content, we create an issue, and have a checklist for each locale.

[Florian] In early July, I plan to start working towards tooling. A lot of that will be much easier in the new system. I'm happy to help leveraging and making it easier with the new build system like scraping out external links, which will be much easier and faster. No need to dig into it, but I published the first pre-release earlier today.

You can check it out if you want to get a rough idea of what's up and coming, but the polishing is missing. Chunking through macros and broken links is so much easier if your iteration cycle is like a second instead of a few minutes. I hope that will help fixing a lot of these and resolving other issues.

[Ruth] Thanks, Florian. That sounds really good. We're excited

Onkar, so for examples, I think you're right, we need to create a spreadsheet. We will think about that ASAP and  review what external examples we want to keep because they're not all going to be live examples. Once we've done that, we will have a list of the ones that can be moved and we can tell translated content team.

[Pranshu] Should we create an issue or discussion for this so that it's easier for everybody to see?

[Ruth] Let us do the audit first and then we'll create a discussion which can link to the spreadsheet with the items we want people to help us with. We need to have a list first that contributors can refer to and take tasks from.

[Pranshu] Awesome! Looking forward to some progress in the next call.

### Is there an objective around closing issues? (@rumyra)

[Ruth] I had a question around closing issues because we have contributors closing lots of issues. I found out the answer earlier, which is, there is no objective. People just wanted to come in and close loads of issues. So I guess the thing to mention here is that you're gonna see a lot of activity over the next few weeks because some of our contributors are trying to reduce that issue count, which is fine and cool.

### Inline icons [discussion](https://github.com/orgs/mdn/discussions/654#discussioncomment-9746229) (@rumyra)

[Ruth] The inline icons discussion on code. This is probably something most relevant to you, Onkar. This is the idea of putting experimental and deprecated icons throughout the site, not just in the sidebars, but making sure they're clear in our reference pages and things like that.

I want to see the vote on the discussion to see how maintainers feel this should be done. But I don't think at this time it's a good idea for us to implement it because of the platform changes that are coming. So we will be updating macros, but in about three months, that'll all be moot because we'll be doing it in a completely different way.
 
[Florian] Yeah, I can also add that when I redid the sidebars, I'm adding more icons where we previously did not have them. I need to figure out if we want to keep them.

At the same time, it's quite easy because there's a global post-processing of all links where we have this context so just injecting them is straightforward.

[Ruth] Yeah, that's what I'm trying to say. I want people to vote. But no implementation will happen at this time.

[Florian] I was wondering about one case I ran into and that I was not aware of — some guide pages have a feature status

[Ruth] Yes, because they've got a BCD key. We're using the BCD key for the baseline status.

#### Other topics

[Onkar] I need a review on a pull request. I think we can take that offline.

[Christine] How does someone become a maintainer on MDN?

[Ruth] It's usually someone who has been around for a long time and has been helping with pull request reviews, issue triaging, and those kind of activities. We consider it on a case-by-case basis.

[Pranshu] We don't have fixed guidelines yet. I will be building those, so I will have a clear response for you in a few weeks. For now, just get involved, get your hands dirty with issues, PRs, and help us out, just like Onkar, Chris, and other folks here. After some time, I'll add you as a maintainer, it's as simple as that. I'll reach out to you, and we'll take it offline. No worries.

[Onkar] I'm being asked to convert an image to an SVG, but I'm not well-versed with SVG. How should I proceed? Can we have a tool hosted somewhere to convert PNG to SVG for other contributors?

[Brian] I can help you with that, Onkar. I've been doing a lot of the HTTP diagrams in the last couple of weeks, mostly redoing them from scratch, which has been okay if they're mermaid diagrams, because then we have the source for them afterwards. Otherwise, if they're just boxes and lines, they're pretty easy to recreate, so I can give you a hand with that if you want.

[Pranshu] Awesome. We don't have anything else on the agenda. One last important update that I wanted to share was that our next community call will be on the 23rd of July, 2024. If you haven't guessed it yet, MDN will turn 19. I hope to see all of you there.
