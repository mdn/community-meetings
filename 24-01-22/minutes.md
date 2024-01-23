# Minutes from MDN community meeting 22nd January '24

**Attendees:**
Mozilla: Ruth (@Rumyra), Brian (@bsmth), Vadim (@pepelsbey), Dipika (@dipikabh), Leo (@LeoMcA), Andi (@argl), Sonal (@s-sood)
OWD: Florian (@Elchi3), Jean-Yves (@teoli2003), Estelle (@estelle)
Google: Chris (@chrisdavidmills), Robert (@robnyman)
Community: Onkar (@OnkarRuikar), Natalia (@nataliaschlebinger), Jordan Harband (@ljharb)

**Host:** Brian (@bsmth)

**Taking notes:** Dipika (@dipikabh), Vadim (@pepelsbey)

## Welcome

(Brian) Welcome everyone to this year's first community call. Thanks for joining in. We have a packed agenda. We'll try to cover the updates in the first half and then move over to community updates. I'll keep a time check.

- I'll take this opportunity to welcome Vadim who joined MDN as a technical writer in November'23. He's based in Berlin.
- Also let's welcome Andi, who's joined the engineering team on the 15th of this month. He's also based in Berlin.

(Brian) A kind reminder for anyone working on contribution guidelines, macros, automations, give us a heads up for the changes coming. You know where to find us (Discord, Discussions on GitHub).

## Team updates

### Firefox [experimental features](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox/Experimental_features) page workflow (@pepelsbey)

- (Vadim) Firefox releases some features behind flags. They're interesting features that developers should play around with it. To enable surfacing these features, we decided to add a section to the Firefox release notes (as an example, we added [this section in Firefox 121](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox/Releases/121#experimental_web_features)). This will include a single para description to say which features are shipped in the release behind a flag. This would help making the developers aware. There are definitely features like :has(), declarative shadow dom, that developers would like to experiment. Highlighting this here in our community call so that we remember to update this section while preparing our release notes.
- (Chris) Is the plan to keep both pages, "Firefox release notes" and "Experimental features"? This is a good move to create awareness among developers.
- (Ruth) Yes, we'll keep both pages for now. The plan is also to somehow improve the table format on the "Experimental features" page moving forward

### Observatory (@LeoMcA)

- (Leo) [Mozilla observatory](https://observatory.mozilla.org/) is coming to MDN. We recently announced this in our [blog post](https://developer.mozilla.org/en-US/blog/mdn-observatory/). We might be able to release it this week on Thursday.
- As an introduction, its been around in Mozilla. Our infra team did not have capacity to maintain it. It is basically a tool where you give it a URL and it tells you the security recommendation, mostly around headers, recommends the best practices.
- We’ll be updating and maintaining it from now on.
- MDN is expanding on tools for web developers, like the Playground and now Observatory, and these tools link back to MDN
- It is technically an interesting project.
- We welcome your thoughts and ideas

### Yari architecture (the build part) v2.0

- (Brian) Florian D. has sent some notes. Since Florian D is not here, Leo, do you want to fill in?
- (Leo) Sure! Everyone please bear with me as I speak on behalf of Florian

#### What we want to achieve:

    - Much faster build time
    - Incremental builds
    - Decouple content from front-end
    - Intermediate representation to make content reusable (like VS-Code / devtools integration)
    - Simplify writers experience (fewer dependencies and a dev process closer to production)
    - Be prepared to leverage new things like page types
    - Streamline our various code examples

#### Where we are

    - We're scoping the work and are considering options moving forward. More once we narrowed things down.
    - Some options we'e considering:
      - Moving to Rust for most parts of the build system because it's:
        - Embedable via WASM so we can reuse code and gradually migrate
        - Easy to distribute as a single binary
        - Performant
      - Bigger changes to the macros. Some preliminary thoughts:
        - Move to a common templating language like mustache
        - Move to web-components that can either be rendered during build or in the client
        - Replace macros with custom md logic (think `[Array]` will link automagically to `/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array`)
        - Move more things like sidebar, BCD or syntax into front matter

- (Jean-Yves) What is the timeline? This quarter or year? For macros, examples, please come to the writer team, we know why they are different, what they are used for, the nuances. So please discuss at the beginning.
- (Leo) The aim is to try to do things gradually, we will definitely reach out. As for the timeline, probably the first half of this year, not sure of exact dates. The work is starting now.

### PR "size" labels in Content (@bsmth)

- (Brian) I've added an automation that adds labels to pull requests in content https://github.com/mdn/content/labels?q=size based on the size of the pull request. You can find the related discussion: https://github.com/orgs/mdn/discussions/629
- This is working as expected.
- Now we can improve the categories. The numbers are at the moment, for example, large is small. We can change the configurations.
- So let me know what you think
- (Chris) I am pleased you’ve added this automation. There's certainly value in people with limited time to quickly pick up PRs for review and contribute.
- (Brian) The bot was also adding comments to the PR, which we have disabled for now. But we can add going forward if they're helpful
- (Chris) They might be helpful because then Estelle would not have to manually ask me to split my big PRs into smaller ones!

### Chat with Chris M about some pain points (@Rumyra)

- (Ruth) Chris and I had a collaboration discussion to talk about the pain points in the last few months. Chris has put together a doc so we can share resolutions to the pain points very soon. Looking forward to discussions that come as a result.

## Contributor updates

### [Community help needed] Documenting interoperable APIs (@teoli2003)

- (Jean-Yves) Let's document all `HTML*Element.*` APIs!
- [Instructions](https://github.com/orgs/mdn/discussions/476) & [Task list](https://docs.google.com/spreadsheets/d/1lvITVZJM8dx8s_Kee5UNI1hDfPNF0gXQwjPop5xIF5E/edit#gid=369545647)
- (Jean-Yves) This is a community project to document all interoperable APIs. It's been 10-15 years that we’ve been wanting to do this. Now is a good time to add all missing docs - document all the APIs that are now available in the three engines
- There are more than 300 pages missing.
- When we started documenting, over the years we gave priority to new features
- With Baseline and Interop gaining importance, we now have a gap
- Html elements - 300
- Svg also
- I've created a list of pages in Google docs, and there are instructions: Go to the task list, put your name (GitHub handle), create the pull request, and we’ll review
- We managed to complete 3-4% in the last week itself. I am hoping we'll be done with all by the end of the year. I am hoping the process will become faster.
- Once you've completed the documentation for one element, you can go quickly, use the same template and create another one. If we go faster, I am hoping it can be done by end of summer.
- If you have any question, ping me on the pull request or on the discussion (linked above).
- Thanks for your help.

### [Community help needed] Document missing JavaScript errors (@nataliaschlebinger)

- (Natalia) Lot of them are missing, I looked into how many are missing. The details are captured in the issue https://github.com/mdn/mdn/issues/505.
- I checked JS engine code, Spidermonkey, v8
- (The connection was getting choppy and voice was breaking up, so Brian took over)
- (Brian) I can provide context. There are JavaScript errors that Natalia has spotted are missing documentation. Different browsers report them differently.
- We do have quite a few documented already.
- If anybody has any concerns, let us know
- Please leave questions in the issue
- Natalia, if I’ve missed anything, please let us know in the chat!
- (Natalia in chat): I was hesitating, thanks for the segway Brian!! The hardest part abt documenting the errors, is figuring out which ones we are missing, because if we look at the code of an engine, most user facing errors are next to internal ones. So maybe we need someone who is comfortable with that c++ code, to help out with that

### Update from Onkar (@OnkarRuikar)

- For context: https://github.com/mdn/content/pull/31694#issuecomment-1902848995
- Do not manually add/update the following:

  1. Front-matter `status`
  2. Page banners {{SeeCompatTable}}, {{Deprecated_Header}}, {{non-standard_header}}
  3. Inline badges {{Experimental_Inline}} etc.

- (Ruth) Can you let us know where this is documented, announced, or discussed.
- (Onkar) It has not been announced.
- (Jean-Yves) We've been doing this for a year.
- (Ruth) My team is still doing the updates manually and we're not aware of these automations. Could you open a PR to update the guidelines, and then we can announce.

## Questions/Discussions

### Standards position in docs (@Rumyra)

[Discussion open](https://github.com/orgs/mdn/discussions/463). I'll push this one out. I'd prefer to have a meeting specifically to discuss this because some folks involved are not here today. We'll hopefully meet within this week to discuss it.

### Consensus secure context usage (@teoli2003)

- [Where and how to use `{{securecontext_inline}}`](https://github.com/orgs/mdn/discussions/482#discussioncomment-7825014)
- (Jean-Yves) There is a discussion open on this. We'll move forward with the plan in the discussion.

### APIs that need an "enrollment" (@teoli2003)

- The first APIs that need an "enrollment" before their use landed in ([Shared Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Shared_Storage_API)). How to display this information on the relevant pages? A banner for secure contexts?
- (Jean-Yves) Not going to discuss this here. In order to use APIs, you need to enroll. These are controversial APIs, linked to the [standards position in docs discussion](https://github.com/orgs/mdn/discussions/463)
- (Florian Scholz in chat) Feature detection also doesn’t really work for APIs that use enrollment. If anyone has thoughts —> https://github.com/openwebdocs/mdn-bcd-collector/issues/986
- (Chris) At the moment, there's only enrollment requirement. This is an early way of doing it - Shared Storage docs https://developer.mozilla.org/en-US/docs/Web/API/Shared_Storage_API#enrollment_and_local_testing. Happy to get feedback
- (Brian) Where should we ask for feedback?
- (Ruth) We’ll have a meeting soon, hopefully we'll be able to discuss intricacies
- (Chris) So I wont create a discussion, we meet first

### Using GFM-standard syntax for notes & co (like `[!Notes]`) (@teoli2003)

- https://github.com/mdn/yari/pull/10168
- (Jean-Yves) GitHub has extended the markdown syntax, but we do our own syntax for Notes.
- Do we want to use new syntax in phases?
- Secondly, there are more types of notes in GitHub markdown. Do we want to use more cases?
- For localization, you don't have to translate notes. It would be nice going forward.
- Yari team can include this in their refactoring. It is better for maintenance.
- Folks will know it works here in GitHub and elsewhere. We need to coordinate this effort.

### Accepting more sources for polyfills (@ljharb / @teoli2003)

- https://github.com/orgs/mdn/discussions/475#discussion-6000833
- (Jean-Yves) The current problem: few years ago, polyfills on MDN were a mess, were unmaintained, and were plain wrong. There were links to many pages with polyfills without correctness assessment.
- 2 years ago, we decided not to host polyfills on MDN, instead we link to external websites
- For security reasons, we want to be strict about which place we trust for polyfills, only standard places like tc39
- It was never the intention that it would be the only one
- We have a shortcoming, we only have one source. What if the source is not trustable or there are more?
- We should have more than one website for accepting polyfills. What is the criteria, how to vet these websites? Jordan is maintaining a good website but no way to know if it is compliant
- (Jordan) Thanks for making the time for this topic and giving me a chance to speak
- I can talk about JS polyfills, cant speak for broader platform polyfills, core js and my package pass two tests, both are well maintained. Need to consider risk factors, high adoption
- Criteria could include conformance, web platform tests, sufficient adoption, which could be tough to quantify. Also it could be the case of you know it when you see it. JS has less than 5 of us with packages that are well known. Having two choices is a good start.
- (Ruth) Thanks Jordan for adding this topic to the agenda and for coming, thanks Jean-Yves. We need to be cautious of moving forward, thinking about who we include. We need to be mindful of what we need to maintain, and so I am inclined to start with two. Two that you mention is a good place to start.
- Let’s start with JS
- (Jean-Yves) Start with JS, yes. Decide which pages we include, criteria for which polyfill
- (Vadim) Worth considering how we recommend including them, link to CDN, hotlinking from cdn (performance, security),
- (Jordan) That is a complex question. npm package is/should be sufficient. MDN can avoid having to wade into that discussion, work you all do is hard enough
- (Jean-Yves) To move forward on this, I'll add a discussion, criteria where and how to link, and invite people to the discussion

### How to get reviews on Yari PRs? (@teoli2003)

- (Jean-Yves) Most small yari PRs sit idle. How can we streamline the process so that it is not too much work for the reviewers?
- (Leo) Some of this relates to the build process, research, and rewrite. What we can do now - we've started working in sprints on the dev side. This will help us to look at consistent number of PRs to see what we need to prioritise. We do have some of these marked as priority, we need to carve out time.
- What would help is to make clear in the PR body - whether it's just a content PR or you've fixed a macro, give the discussion link or provide sufficient context.
- (Onkar) Is it possible for OWD or content folks to merge kumascript PRs? They dont break build.
- (Leo) You can review and leave a comment
- (Onkar) Could we get merge permissions?
- (Leo) We do not want to do that, risk of breaking a build is high at night or on Fridays. Ping the core team. You can help with reviewing other PRs. If you have a list of small PRs that are easy to merge, send them our way.
- (Onkar) Where?
- (Leo) We are on Discord and GitHub
- (Onkar) I need permission to be able to ping the core team on GitHub
- (Jean-Yves) I’ll put together a list and will message on Discord, in the platform channel. Onkar can do the same.
- (Ruth) I too will do the same with some of the work content team is waiting on
- (Onkar) npm release of yari. Can we release it automatically at the end of the week? We used to do it after every PR earlier but that was too much. npm release is different from prod release. Last time we were waiting for a couple of days, there was a flaw. Can we automate npm release every weekend?
- (Leo) Yes, it is frustrating to have to do it manually

## End of the topics and call

- (Brian) Appreciate and thank you everyone who could make it. Until next time.
