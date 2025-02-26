# Minutes from MDN community meeting 11th December 2023

**Attendees:** Ruth (@rumyra), Claas (@caugner), Zach (@zfox23), Vadim (@pepelsbey), Onkar (@OnkarRuikar), Dave (@dletorey), Vinyl (@queengooborg), Florian (@Elchi3), Jean-Yves (@teoli2003), Estelle (@estelle), Chris (@chrisdavidmills), Will (@wbamberg).

**Host:** Ruth (@rumyra)

**Taking notes:** Brian (@bsmth)

## Welcome

- (Ruth) Happy holidays, this is the last community call of the year, incoming calls will be announced soon.

  - MDN team not here for week of 25th, will announce on GitHub. Bear in mind we may be slow to respond.
  - Reminder of Open source etiquette, everyone should revisit our CPG, familiarize yourself with it. Please be nice online.

## MDN Front End Developer Curriculum

- Chris Mills

  - (GitHub repo URL for curriculum) - <https://github.com/mdn/curriculum/blob/main/README.md>
  - Been working on FED (Front-End-Developer) curriculum. We'd like to improve education on MDN.
  - Started with Learn area, Chris worked a lot on about 100 articles on web dev.

    - starting point was feedback on other forums to make MDN more approachable for beginners as it can seem intimidating.
    - as an extension, should we revisit the Learn area as a curriculum?
    - Curriculum is based on research from people in a lot of different companies, what are people missing with new hires? what skills do people need? Are certifications actually useful?
    - Results were that hiring managers universally said we wish people knew more about a11y, core JavaScript, not just React.
    - Answer was very much "certs are not super useful", we want to see portfolios, certs cannot be trusted fully. Surely Mozilla has a reputation that could be trustworthy.
    - This is not a course, not a certification. This is the organization of the essentials that a FED should know, arranged into a pathway. Things are arranged as:
      - prerequisites (file system, tooling)
      - soft skills
      - research
      - team work, collaboration
      - core skills, JS, version control, testing.
      - optional extensions -> does privacy / frameworks etc belong in core skills? This is arguable, good to know, but being a security expert might not be a required.

  - Feedback is always welcome. In the new year, the curriculum will be published. It will be free. With some momentum, this could be the basis for courses that others will develop. Guide for complete beginners. Could be used for certifications, but no definite plans there at the moment.
  - (Q from Estelle): New v advanced, what is the boundary?
    - (CM) We've tried to include just fundamentals, but try to steer clear of advanced stuff. Core shouldn't be overwhelming for beginners. We want to keep it short and manageable. If someone wants to create a course from it, or create a certification, it shouldn't be impossible to test "everything". There may be room for this in the advanced or extension modules. Floor is open for this, please file issues on the repo.
    - (Estelle) - I have thoughts
    - (CM) Contact me on Slack or file an issue in the repo.

## MDN Observatory

- (RJ) Work is ongoing on MDN Observatory, deep dive about this is postponed for now, but we'll share details soon, it will be on the agenda for the next call.

## Baseline

- (RJ) New definition rolled out recently. More features are coming soon, there is an MDN blog, go read it :)
  There is a feedback mechanism on pages with this feature. The WebDX community is a place to give feedback there about that.

## Flaw fixing

- (JYP) What happened this year fighting flaws on MDN.
  - At the top of each article (in development mode), there are flaws, and also on localhost, there is a list of flaws and a dashboard.
  - Over time, we want to fix all of them. At one point, there were 15,000 flaws.
  - At this year, there were 5,000, so far we're down to 2,500 over the year.
  - This has been organic, plus directed goal by others. Thanks to Onkar, Brian.
  - We're very close to only "missing pages" flaws.
  - There are a lot of BCD flaws, a lot of these are temporary, from current work in progress.
  - There are flaws for sidebar macros, for static methods. We want to take the macro and fix it there.
  - For missing pages, maybe we can get help from the community.
  - If there are community members who would like to help, reach out to JYP. These pages are easy enough to get started as a contributor. This will be a great project for 2024. At the moment, this is something for community efforts.
  - One thing that's annoying, there is a PR for redirection open from Onkar. This PR is open a long time, should be done soon.
  - (Ruth) Let us know when you want to get contributors involved, we can announce it. Claas - do you have eyes on the Yari PR?
  - (Claas) No capacity in December, but should be on the cards for first 2 weeks of January 2024.
  - [Notes in chat from Onkar] - Also implemented ReviewDog automatic reviews / suggestions from CI workflows doing linting.
  - (JYP) This is a really cool addition in 2023, this really lowers the amount of effort to fixing flaws.

## BCD

- (Vinyl) OWD and Mozilla contractor, maintainer in BCD. Working extensively on BCD collector project. See link for web-features. [https://github.com/web-platform-dx/web-features]
- Good chunk of data from web features now integrated into BCD.
- WebDX group will be using this to implement feature categories.
- Also working hard on a system to automatically update BCD following different browser releases. Whenever there's a new release, the collector runs.
  - (Ruth) Do we run it on stable or beta?
  - (Vinyl) We run it on stable now, because this is the least likely to change. Occasionally run on Beta, but we can do this more often. Main plan is to let machines do repetitive work.
- Great news, just this week I've gone over BCD issues and closed old, duplicates, resolved etc. About 70% of the 168 issues resolved by the BCD collector!
  - (Ruth) that's amazing, well done.

## Content architecture

- (Ruth) I am foreseeing changes with Learn and curriculum. What would be some next steps with organizing documentation. Should we be very strict about content architecture, would this help with guides and docs that sit in multiple places?
- It would be nice to do a joint workshop on "what would you do to organize content" if we started from scratch. Having it very clear what you write and where it goes.
  - (JYP) I agree we need to discuss content architecture. Especially about Divio system, we've looked at this over many years. The recent changes are based on cleaning up guides that have been without a home for a long time. Some of them seem to be from 2007. These changes are more a cleaning rather than re architecture. This will in turn help with sidebars.
  - (Ruth) Thanks for clarifying. We're aware of the Divio system and we can use it for inspiration, but on MDN we are covering a lot of different technologies and this system might not be a silver bullet for us.
- (Ruth) Would start planning a workshop, would be great to do two 1 hour (remote) sessions, would be nice to have a forum for everyone to have their input. Comments, questions, feedback welcome.

## Formal syntax

- (Ruth) Handing it over to Onkar for this one.
- (Onkar) [audio issues]
- (Will Bamberg) I can share some info. This is a big issue, it's about more than Formal Syntax. We have pages about CSS, they have links to specs, links to BCD. How can we make sure these things agree? One of the main problems is formal syntax. What makes sense that MDN does is documenting the realities in browsers. But Formal Syntax documents whats in specs. We can choose to show formal syntax from a certain module, but not specific ones, such as those that are delivered or working in browsers. What's the best thing to do here?
  - We have people opening issues like "Formal syntax doesn't match what's on the page"
  - For the formal syntax, you could have a note saying "not all these things are not implemented" - but we don't have a way to show something as not implemented. At least the formal syntax as it currently is, is better than nothing, but it could be more helpful.
  - Another branch of this is that one of the problems that this exposes is basic support is not defined in BCD.
  - In BCD we have feature -> sub-feature. What does basic support mean? If you say Fx supports align items, but which values? How to find that out?
  - (Vinyl) in regards to a lot of that, the plan is to test for sub-features, and have it be as extensive and comprehensive as possible. So the collector can help with a lot fo that. We can have the collector scan the spec and build tests for this.
  - (WB) Often this is not clear-cut, as there are things such as different syntax in different module levels.
  - (JYP) Non-standard values don't appear in formal syntax. This is very quickly a can of worms, and very involved.
- (Ruth) Thank you for the explanation. I re-read this, I've seen the issues coming in about this. We might want to try to do something sooner than later, with a notice in the meantime. I would suggest we do a temporary workaround.
- (Will) It's not a fix, but it's helpful, so I'm +1 on that. There's a separate issue about bugs, this can be fixed, but the Formal syntax issues here are more content architecture issues, not bugs.
- (Onkar) [audio issues]
- (Will) As soon as you say you want to be precise about it, you'll hit issues. This doesn't go away if you go back to hand-curated data (mdn/data)
- (Vinyl) WiFi issues, sorry.
- (Ruth) This is something for us to handle in 2024
- (Chris) Does this mean we don't have to update CSS data?
- (Ruth) Not quite yet! We did put out a call to people using this package to say how much we depend on it, but nobody got back, so we couldn't deprecate it entirely. It's in limbo, but the end goal would be to deprecate it.
- (Chris) I would love to remove and archive that completely.
- (WB) There are translated strings, making it harder. The main one is CSSTree, which depends on mdn/data. It would be great to split mdn/data into two parts to separate concerns. I get the feeling CSSTree might not be maintained much at the moment, I'm not sure. Although there are some patches on top of MDN/Data, maybe they do their own thing to bridge gaps.
- (Ruth) The decision is whether there's an interim solution while we wait for BCD to do sub-features. Should we add a banner / note?
- (JYP) We can try a sentence, like "This is the spec syntax" and see if there are fewer issues opened. we want issues to be reported, of course, but to mention "there may be differences because browsers may have separate implementations". We could do a search/replace for this afterwards, which helps solve it.
- (Ruth) This is also CSS-only at the moment, right?
- (Will) If we think a real great fix in BCD would take a long time, there may not be very many places where the formal syntax shows stuff that's not on the pages. We could do overrides, some manual fixes.
- (Ruth) Would you like to make a proposal so we can evaluate options?

## Removal of duplicate markdown headings for examples

- (Ruth) Added by Dipika, this is about repeating titles in the prose and the code.
  We had a discussion about this one internally. Originally, I thought headings were a great idea, however I don't think that's a great solution, as the content is machine-readable with language of code blocks visible in source.
- We're not going to be moving them to the right, that's not a fix.
- (Will) This is not about the code, it's about the prose. The prose that's associated with the code. "Here's a block of HTML, here's a description about it". Just to be clear, it's about "how do you link the prose with the code?""
- (Ruth) How often does this happen? I would assume it's mostly implicit based on the position of the prose.
- (Will) This has been talked to death, if you want convention that if you have prose before the code. Or if you say we want to support this use case, we have this convention. This makes it harder to review.
- (Estelle) This came to a head with Chris Mills PR, there are many examples where there's 3 lines of CSS, 3 lines of JS, now it looks very much like a duplicate. When there is content, and a lot of it, it helps tell the user what they expect. Not always, when there's a complex example, this really helps readers when you describe complex actions. When you put the H3s in there, you can link to it from outside. To say we can't have it for newbies, this makes things much harder. We have to frame it based on what learners get, but it has to be geared towards learners.
- (JYP) For the position, before or after, it would be great to get stats. If there's 23 pages, it's not much work. If it's 200+, it's a different story.
- (Ruth) anything else? [no other topics]
- Thanks all!
