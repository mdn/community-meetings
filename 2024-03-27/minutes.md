# Minutes from MDN community meeting 27th March '24

**Attendees:**
Brian (@bsmth), Vadim (@pepelsbey), Dipika (@dipikabh), Florian D (@fiji-flo), Onkar (@OnkarRuikar), Holee (@hochan222), Eric Meyer (@meyerweb), Claas Augner (@caugner), Andi (@argl), Ruth John (@rumyra), Arkanit, Jean-Yves (@teoli2003), Estelle (@estelle), Florian S (@Elchi3), Mahi

**Host:** Brian (@bsmth)

## Intro & overview of agenda

(Brian)
Welcome, great to see everyone including new faces.
Agenda:

- new Footer that's on the website.
- community participation guidelines (CPG)
- What's changed on Discord and Matrix
- The new blog post out

## Team updates

- The Matrix room and the "# general" channel on Discord are now bridged.
  It's a bi-directional chat. So messages posted in the MDN matrix room are posted in the "# general" channel on Discord and vice versa.
  We're trying to make sure that people on Matrix are not left out because we tend to be on Discord quite a lot.
- There's a new blog post out about Interop: https://developer.mozilla.org/en-US/blog/interop2023-mdn-doc-updates/

### Footer

[Ruth John]
We've updated the MDN article footer based on user feedback, shifting more from decisions based on personal preferences to data-driven choices.
This involves a simple feedback form (on-page) asking users if they found the content helpful, so we're working more towards improving content quality through user insights.
Although there's no freeform text field feedback (for qualitative data), we're exploring other methods to gather this.

Since launching, we've seen an average 70% positive sentiment in March.
We will analyze this data by larger sections before tackling individual pages, combining it with other metrics like page views to inform updates or removals.
This is an ongoing project, and we're not taking specific requests yet for the data as we focus on actionable tasks. Any questions?

[Estelle] Q: Is there any way for people outside of Mozilla to see the feedback that is coming through?

[Ruth John]
No, the requests will come in, I know. That's why I would ask you not to ask me for that just yet, I want to be able to analyze the data first and be able to answer follow-up questions, which we'll surely have.

[Estelle]
Side note: I really miss the edit button in the Footer and I realized that I can just click on the "view on GitHub" and then edit.

[Ruth John]
Yeah, we went back and forth on this a lot of times. There were 3 links all to exactly the same thing in the old footer and it just it didn't make any sense.

### Community Participation Guidelines

[Brian Smith]
I'll talk about Mozilla's Community Participation Guidelines (CPG) — this is super important for us, especially because we're on GitHub all day and working closely with the community.
Here's a link to [Community Participation Guidelines (CPG)](https://www.mozilla.org/en-US/about/governance/policies/participation/) for anyone interested.
The CPG guides how we all behave on MDN's GitHub repositories, ensuring everyone follows a shared code of conduct.

There's a useful GitHub repo called [mozilla/inclusion](https://github.com/mozilla/inclusion) that has all the info on CPG, how to report issues, blog posts about it, and enforcement details.

For everyone: If you see something off on GitHub, like in comments or pull requests, you can report it using the 3-dot menu.
This alerts all the admins of the repo.
When a report comes in, we check it out right away to decide what to do. Often, it's clear what needs to happen, like hiding spam or blocking a bot.
But we always look at each case individually.
If it's not always straightforward, we follow a more detailed (and thorough) formal process, which involves the Community Participation team for an official investigation.

The goal is to keep the community safe and respectful.
If someone breaks the rules, we might have to take serious steps, but banning is an absolute last resort.
We prefer to resolve issues quickly with reminders of how to behave so everyone can keep participating.

If reporting through GitHub isn't your thing, you can also email CPG reports directly.
It's all private and confidential.
If you need to chat about something, just reach out. We're here to help.

[Estelle]
Any rules for false reports, a situation on Mastodon where a hijabi person was targeted with reports due to Islamophobia.
The reporter gets blocked in such cases.

[Brian Smith]
Yes abusing the reporting process is indeed a violation, consequences can vary, but it's abuse. Not sure of the specific language in CPG for that.

[Onkar]
Is this information linked from the main MDN website?

[Brian Smith]
The community pages on MDN have links, we might link directly to the Mozilla/inclusion repo.

[Estelle]
Opened a PR to add more links to the CPG for better visibility.

[Brian Smith]
Appreciated!

## Discussions & questions

### How to use inline status macros

**Discussion:** https://github.com/orgs/mdn/discussions/654

[Onkar]
We put these macros in two spots: up top in the header and inline right next to each property in the content.
Recently, we pulled the inline macros because of some issues, but now we're debating if we should add them back for properties marked as experimental.
It's handy because people don't have to scroll all over to find out if something's experimental (to BCD table or to top of page with banner)

We've got two ways to go about it: put them everywhere like a 'christmas tree' or just up top like a 'traffic light'.
Putting them inline makes it super obvious and cuts down on the need for scrolling or checking other sections.
If the property is experimental, the question is, do we tag each value with an inline badge?
It looks repetitive, but it's immediately noticeable to people without referring to other parts of the page.

[Estelle]
At first, I was skeptical, thinking, "This is going to be a massive headache," but then I realized it's not so bad because a bot can handle adding and removing these experimental inlines, making it less of a maintenance nightmare.
So, the burning question is, should we, or should we not add the experimental inline, considering it's automated?
This could make it significantly easier for readers to spot experimental features without extra effort.

[Brian Smith]
I can also leave an opinion on the GitHub discussion if that also helps, but just my initial thoughts were that this a bit too much to start inlining per CSS property value in the content.
I wonder if there's something in between where if we say in the banner that if it's not experimental (property) but there are parts of it which are (values).

[Onkar]
If the property is **not experimental** but the some of **the values are** then then we do tag them with the inline badges.
But the question is about if the property itself is experimental, should we tag each value with an inline badge?
It looks repetitive and verbose, but we have found that it is really visible to people and they do figure out if this is experimental or not.
So this way they notice it quickly. And they don't necessarily refer to BCD tables or scroll up to see the header macros.

'christmas tree' is the current implementation. So if we now change the strategy then we'll have to educate the readers as well.
That this is how it is. So there are a bunch of pros and cons stated in the discussion.
Please go through the discussion and please add your comments.

[Ruth John]
This would help for experimental values. So the property itself is not experimental, but sometimes we get new values on the property and their class is experimental.

[Estelle]
If we're putting experimental on a value when the property is not experimental, then someone can automatically see that this value is experimental.
But if the property itself is experimental, then they would have to actually go to the top or go to the bottom of the page.
To realize it's experimental and not realize that every single value is experimental.
So if every single value is experimental we probably should put it someplace in the values area that it is experimental.
Because they do get that information sometimes but not if the property itself is experimental.

[Brian Smith]
I wonder could that be a display fix instead where where we don't actually edit in the content, but Yari shows something for experimental values of an experimental property.

[Estelle]
So we the thing to realize, cause I thought this was the worst idea ever until Onkar explained that a bot does it.
So we don't have to maintain it.

-- off topic --

[Onkar]
There's an API example in chat, open that. The page header is experimental because the accelerometer is experimental API.
And if you scroll down each member of the API like constructor and instance property they are all marked with experimental inline badge (the flask icon).
Do we add a flask icon for each member of the API or the CSS property if the property itself is experimental?

This question arose because we have decided different strategy for secure context macros.
And Will objected saying that we should adopt this same strategy for inline status macros as well.

Right now we are using the 'christmas tree' strategy.
Will says that if we could use the same strategy that we decided for the Secure context macros.

[Ruth John]
It's difficult

[Dipika]
Yeah, I think, on initial thoughts, it seems that it might be a good idea to replicate whatever the BCD is showing.
So if the BCD is showing the status as experimental. Instead of having to scroll between values and BCD table.
If it's shown also next to the value. Then it would be helpful.

[Onkar]
Yes. It certainly is.

[Brian Smith]
Okay, then maybe the next step for us is to just record that on the GitHub discussion.
Do you need votes, right? Whether you go for the 'traffic light' or the 'christmas tree'?

[Onkar]
Yeah, please do go through Pros and Cons.

[Estelle]
Class asked a question or made a comment in chat, which I guess we should clarify, which is "the bot that would add the inline experimental macros, is that on Yari is that done in the Content"?

[Ruth John]
Content.

[Estelle]
Class does that change your comment?

[Claas Augner]
Hmm. So this implies that. The information about whether something's experimental is actually added to the content.
I wonder if there would also be a way to get what in the Markdown is enriched when rendering just like we run with BCD tables.

[Ruth John]
Yes, there is a whole document and project about automating things like this so we don't have to, but the way to Onkar's implemented is he's running an automation in the content repo.

[Claas Augner]
Okay.

[Ruth John]
And he's checking against BCD key, he's checking for the experimental flag and then he's automatically adding a markdown macro into the content, which isn't terrible.
We don't have to author it, which is kind of key here.
Maintenance is definitely a concern. We did decide with secure context though to only put the banner on the interface page.

[Estelle]
Secure context is a bit different because in secure context everything is served over HTTPS nowadays.

[Ruth John]
Oh, it's more that secure context is required to use the API.

[Onkar]
So if we are going to use 'christmas tree' for a status macros, then we should use the same strategy for secure context macros as well.
For sake of keeping the things the same.
If you use different strategy for each macro then there will be confusion.
And we so whatever we decided for secure context we haven't implemented in content repo.
So there is still chance that we could revert the decision on secure context macro.

[Ruth John]
I'm having a think about it. I don't know I'm gonna come to any conclusions in this call.

[Estelle]
There are guidelines now to discussions as to how to move them forward.
So Onkar; as the driver of this discussion, if you can summarize what was said in the meeting in the discussion and then if anyone has any opinions that they haven't shared, if you can put them directly in the discussions.
Cause the discussion is supposed to be the source of truth for any decisions that we come up with.

[Onkar]
My question is now I have conveyed this, are you going to put your comments in the discussion itself for are we going to conclude in the next community meeting?

[Ruth John]
We can conclude it in the discussion.

### Indicators and banners

[Brian Smith]
Next up, indicators and banners. This one is from Estelle, is it?

[Estelle]
I didn't know if there was a discussion, but if we could open up a discussion, point into the PRD, we can have the conversation in the Google doc and then once we have all the feedback in the Google Doc, port it over to the GitHub discussion.

[Ruth John]
This is a project that we want to go over sometime later in the year to sort out this banner mess basically.
What I will do (I'm not necessarily against capturing the timeline of this in discussion) I think everybody has commented on the Doc I created now.
Next up is to go through that Doc again and create a proposal.
Once I've done that, we can start a discussion and say "this is the proposal" and discuss the thoughts behind it.
Does that work?

I would also say regarding the timeline for this; there's no urgency.
We also have to wait for Baseline to be on more pages before we can actually make a good educated decision, if we try to do that before then I think we'll be doing the work twice.

[Estelle]
There's about 6 different conversations about indicators and banners. So there's already all these discussions going on.

[Ruth John]
They're all captured in the Doc.
I'd rather wait until we had a proposal and how we're going to move forward and then open the discussion and in all the related discussions, say 'Let's go and look at this discussion because this is our proposal'.

[Estelle]
I would love to at some point close all those other discussions and move on

[Ruth John]
Yeah, it's next on the list.

### Writing Guidelines and Glossary

**Discussion:** https://github.com/orgs/mdn/discussions/661

[Brian Smith]
The sections Glossary and Writing Guidelines living on islands. A bit more of a visibility to be recognized.

[Ruth John]
I think where we link to the Writing Guidelines, where we link to the Glossary, are 2 separate discussions to be had because they're very separate things.
In the discussion, Will very rightly points out that if we put Writing Guidelines at the top anywhere, our users are just going to think it's "how to write code" guidelines.
So that's not something that we are going to do.

Glossary; there are design and product considerations to find out how everyone feels about putting Glossary in that dropdown.
It seems to be the consensus that people want it there.

As far as the Writing Guidelines go.
There's a lot of talk about where to put links and all the rest of it and the changes to be made.
The key one for me was: when you click on contributing, you get taken to contributing.md on GitHub and then all the links in there move you back onto MDN.
And then this kind of opens a can of worms about where we put the contribution guidelines but I think they're too linked to the Writing Guidelines to really separate them.

And we can't have the Writing Guidelines elsewhere because they contain so much styling from MDN itself that we'd lose all of that.

[Onkar]
So I think it is better to move whatever there is in the GitHub `.md` files about contributing to the rendered pages and we host everything like other MDN docs.
So, basically all the README files on GitHub (CONTRIBUTING.md), we move it into the content and host it.

[Ruth John]
Yeah, I think that we could stop the user flow from going to GitHub and back again.
We need to keep repository specific stuff with the repository though.

That was a conscious decision that we made when we were doing all the contribution docs because otherwise we're gonna have 2 places to list our 50 repositories and put all the guidelines for all of them on MDN.
I don't think that's MDN content. I think that's repository-specific.

So some stuff is still going to have to stay on repositories, READMEs, CONTRIBUTING.md, things like that.

[Onkar]
We can have minimal stuff on the repository and most of the checking out, the git stuff, all the small small things about using it.

[Ruth John]
I think there is some "how to use GitHub" stuff in both places, we should review it again.
We can review the contributing.md on content that we link to, revise that and make sure that when people do click on Contributing they're taken still to MDN rather than back and forth.

[Estelle]
The other thing we can do is since it's all markdown; point to the blob on GitHub which is actually then automatically rendered so it's just written in one place.
And where you link to it if you're in GitHub you can link to it from GitHub like from the README file.

[Ruth John]
We don't want to duplicate content and have to keep it up to date in 2 places.
So that does help solve that problem, definitely.
Unless you have macros. I think we can avoid them in our contributing docs.

[Estelle]
I mean, there'll be the sidebar macro, but that would be about it.

[Ruth John]
Yeah, I think that's a blocker. As far as some of the suggestions on where this link should go, I think we carry that on in the discussion.
Some of the suggestions already in there crossing over with some work that Anuja, our UX designer is currently doing on site-wide navigation.
But things like adding Writing Guidelines specifically unobtrusively is okay.
I think if we have a markdown page that links to all the different things on MDN, then we can harness that and we can link to that.

[Brian Smith]
Anything else? Anyone?

[Onkar]
No, just contribute to the discussions. If you put your comments over there, then we know that it is making progress.

[Estelle]
I guess what you're also saying is we should pull out Glossary from the Writing Guidelines discussion and create a separate discussion for Glossary.

[Ruth John]
I think maybe that's a good idea. Cause I think that user flow for the guidelines and where it comes from where it goes to and everything is probably gonna take over from Glossary discussion.
There'll be 2 conversations happening at the same time.

[Onkar]
Okay, I'll create a separate discussion.

[Ruth John]
Thanks.

[Estelle]
Thank you for all your contributions Onkar

[Brian Smith]
Yeah, absolutely.

[Onkar]
My pleasure.

## Closing discussions

[Brian Smith]
If there's anything else that you want to discuss, talk about, bring up. Now's a good time.

[Estelle]
I went through a bunch of discussions. So I might have hit you up asking you a question to move your discussion forward. There's a lot of discussions that have been opened since like 2022.

[Ruth John]
That's great Estelle, thank you. I did start trying to do this a couple of months back but got caught up in discussions.

### Playground feedback

[Onkar]
Yeah, I have one issue that has been bugging me. In the playground, there is a Reset button.
And when we click on the Reset button, it wipes out everything. I think it should bring back the original code.

[Brian sharing screen]

[Florian Dieminger]
Background color is my favorite.
No, that's a good point. It should be a "clear" button. That's what it does.
And I do see the need for a "reset".

[Onkar]
If I've modified the code and hit Reset but now I can't get the original code

[Florian Dieminger]
Yeah, the original code is not stored anywhere. We should at least change it to "clear".
So it's clear to everyone what this button does. It doesn't reset.

I think it was done prior to the integration, so the thing was to reset the current state.
If you click on refresh, like if you come to the playground from the top, you have a fresh thing.

And reset like get it back to be clean. But it should should be clear. And I do see the need for that.

To get back to the example.
We have enhancing the playground in our goals.
And we'll actually extend it quite a bit and move to having a proper Service worker implementation.

I think we can do the "clear" rather soon because that's like UI renaming.
But to actually store the context you came with like the original example and reset to that original state.
Probably have to wait until we do the second iteration of the playground, which will be midsummer, something like that.

[Onkar]
In the share URL, you are already capturing the code, right. Could you just pick up the code and repopulate the editor?

[Florian Dieminger]
No, the permalink is quite different.
That actually creates Gist on GitHub where the code is stored and we don't have this for a live sample.
So the live samples are stored in local local storage.
I can look if I can see an easy way to restore that state but right now we don't keep history.
I mean that's the issue; if you modify the code, we override the current state and we don't have a history in the state.

[Onkar]
So quick solution is to rename the button to clear, right?

[Florian Dieminger]
Yes, and I think Control C in the editors works and maybe there is a way for me to actually make this to go in the editors to the initial state. I need to look into that.
Thanks for bringing it up. I'm sorry for the confusion with that naming.

[Onkar]
Thank you.

[Brian Smith]
It was great seeing everybody. Really appreciate all of you joining. You know where to catch us.
I'm looking forward to the next one. And have a lovely evening and we'll see you next time.
