# Minutes from MDN community meeting 29th April 2024

**Attendees:**
Andi Pieper (@argl), Chris Mills (@chrisdavidmills), Claas Augner (@caugner), Dipika Bhattacharya (@dipikabh), Florian Dieminger (@fijiflo), Florian Scholz (@Elchi3), hochan Lee (@hochan222), Natalia (@nataliaschlebinger), Ruth John (@Rumyra), Vadim Makeev (@pepelsbey)

**Host:** Vadim (@pepelsbey)

**Taking notes:** Dipika (@dipikabh)

## Intro and overview

[Vadim] Welcome everyone! We have a bunch of team updates first and then a couple of topics from the community. If you have any questions, feel free to unmute yourself, raise your hand, or just post them in the chat.

## Team updates

### Community manager update and reviewing community calls (@Rumyra)

We are currently in the process of extending an offer to somebody. Fingers crossed that they’ll accept and hopefully the next call will be run by the new community manager.

Getting a community manager onboard will give us the opportunity to review how our community calls are going, how people feel about the frequency and the time zone. We’re asking if people would like this call in a different time zone.

[Vadim] Yes, please let us know on Discord or on the GitHub poll what time works best for you. Feel free to leave a comment: https://github.com/orgs/mdn/discussions/678.

### Update on content team projects (@Rumyra)

- About the **content workshop** I ran a month ago, I am still writing up the notes. Sorry for the delay but my time has been dedicated in trying to hire a community manager over the past couple of weeks.
  In the content workshop, we talked about content architecture, types of content, and how we are looking at the new curriculum now along with the Learn area and what we want to do with guides and how-to's.

  I'm hoping that I will be able to produce the outline and the summary and propose the next steps forward from that work, very soon. So watch this space.

- Some of you may have noticed that we added a new **article footer** back in February. The footer now has a little form asking if the page is useful. We intend to use this to give us the sentiment data on pages.

  We have one month of data from March and I will be looking at April's data as well and comparing them. In the content team, we’re looking at that data to guide us on the areas to improve or update. Any area with a low score implies people are saying this wasn't useful because of whatever reason; we can then look into those areas and hopefully update them. There'll be probably more to say on that once we actually start this work.

  I'm excited about getting the data in because then I can compare and see whether it's the same sections that are coming up month on month.

- For the reference indicators and banners, I put together a document back in January. This kind of ties into some platform work, which is ongoing and will run into Q3/Q4. We are obviously in danger with Baseline being rolled out across the site - that's the indicator to say whether a feature is in baseline.

  We're going to get lots of banners at the top of pages, including those for secure context and deprecated features. We need to review how to present that information so we don't end up with just a box after box at the top of the page instead of the information that people actually need.

  I will be revisiting that document this quarter, along with some work that we're doing for the platform.

  Thanks to everybody who reviewed it. And again, sorry for the delay, but it's ongoing.

  Any questions?

[Chris] I didn't necessarily have any questions, but I just wanted to say - very exciting news on the community manager. Really looking forward to seeing more progress on the content workshop. Let me know if I can help in any way because I do appreciate your time is very stretched. I can't remember if we were intending to have that as what data should we have, what data we need, and then have a "how to present it" as a separate follow-on thing from that session.

[Ruth] Yes, that will be the next step. For reference indicators and banners, for example, if there's a lot of data that we want to show, maybe we should consider that together. I want to integrate people's comments from the workshop and then think about the next steps. We can talk about the kind of data that we have for pages and make sure that it's confirmed in the way that we're actually getting it, and then we can move forward with how that data is displayed. Thanks very much for the offer. I just want to at least get the transcript bit finished. And then do some rough drafting of some proposals for next steps.

[Chris] I'm quite interested in the sentiment data. From my experience, people tend to comment primarily when they've had a bad experience and rarely if they have a good experience, which could be useful in identifying pages needing action. I'd love to see semi-regular data updates to monitor patterns and get a clearer idea of the trends.

[Ruth] Right now, we're looking at high-level areas with low scores, not breaking it down by page yet. We have an average of about 70% good sentiment, so people are actually telling us that they like the content, which is super nice. But this isn't perfect and won't tell us exactly what is wrong, though it gives us a good place to start to know what needs our attention.

We'll get more data over the next month, and I'll let you know when it comes in.

### Spam from zombie GitHub actions (@pepelsbey)

I want to address the issue of notifications from zombie GitHub actions. You might have received notifications titled something like '[jessejay-ch/content] PR review companion workflow run' (https://github.com/jessejay-ch/content/pull/2). Someone forked the `mdn/content` repository a year ago, and it started failing some GitHub action. We later fixed this action, but the fork and pull request are stuck, causing it to fail every time someone pushes commits to `mdn/content`. I get an email every time my pull requests get merged, and 90 other people in the pull request also get notified. This has been going on for a year.

I've contacted GitHub support, but there's not much they can do for now. They are, however, considering options to let users disable these notifications or unlink forks.

In the meantime, we can only filter these out. I'm sorry for the inconvenience, but let us know if you experience something similar. We'll let you know if it gets solved in any way.

### SEO and translation experiments updates (@caugner)

I wanted to briefly share two things.

- First, we're working on SEO improvements, including [a notable experiment](https://github.com/orgs/mdn/discussions/673), though it's too early to share results.
- Second, we're creating a German locale using machine translation. We'll share more details later, but this gives a sneak peek at what's coming.

## Contributor updates

### Documenting missing JavaScript errors (@nataliaschlebinger)

Josh (@Josh-Cena) and I have been working on documenting errors. We've identified a list of errors to address, focusing particularly on JavaScript errors listed in V8. We noticed many errors that should be documented, especially those related to classes were missing. For example, there were only two class-related errors listed, while nameless functions were documented in more detail.

It seems classes were introduced later, leading to this imbalance. Our initial plan was to go through the V8 list in order, but after discussing with Josh, who is reviewing the PRs, we've decided to allow contributors to choose the most interesting errors first. This way, we prioritize complex and valuable errors, particularly those users might actively search for, rather than just glancing at the error text and moving on.

Related pull request: https://github.com/mdn/content/pull/32857
Planning issue: https://github.com/mdn/mdn/issues/505

[Chris] I really approve of this effort because when we first documented JavaScript errors, those pages became some of the most visited on the site. People search for errors in Google when they face issues, so updating these is definitely worthwhile. Have you talked to Florian Scholz (@Elchi3) about this? He originally documented the errors and might have useful insights. It's also great to have a checkbox for the errors completed, making it easier for contributors to pick up where others left off. One issue to consider is that error messages vary across browsers. V8 error messages are fine, but it might be helpful to link these to the equivalent messages in Gecko. This discrepancy isn't a blocker, but it's something to think about.

[Ruth] I agree. I've seen the discussion on Discord and think going out of order is fine. Florian Scholz could give us feedback, and others can join the discussion. The checkbox idea is helpful for tracking progress and guiding contributors. You can message Florian on the GitHub issue for input.

[Natalia] I'll contacted Florian. When testing errors, I've been running code that triggers the error on V8 and Gecko. There might be discrepancies, but it hasn't been an issue. We could consider how to handle these differences.

Are there any automated tests for the documentation, particularly to ensure examples still work. If not, we could consider checking examples for errors across different browsers.

[Florian D] No, we don't run automated tests on the content examples. This can be tricky because not everything works everywhere. Some examples are specifically wrong to teach the right approach. Additionally, errors can vary between JavaScript engines, and some are API-specific.

[Ruth] I agree. Automated testing might not work well due to the variety of content and intentional errors. Let's focus on content errors for now.

[Vadim] It sounds like something for browser compatibility data. Maybe we could add this data to BCD and run some tests. We could also flag features that are experimental in different JavaScript engines.

[Chris] I think the priority is getting pages written. We can review them afterward. Thank you for the work on this.

### Documentation updates on MDN (@chrisdavidmills)

I've been documenting various features for Google and responding to comments on my pull requests. This has led to a lot of published content, including:

- [Long Animation Frames API](https://developer.mozilla.org/en-US/docs/Web/API/Performance_API/Long_animation_frame_timing)
- [CSS `field-sizing` property](https://developer.mozilla.org/en-US/docs/Web/CSS/field-sizing)
- [Vertical form controls](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_writing_modes/Vertical_controls) using writing modes, now coming to both Chrome and Firefox
- The `notRestoredReasons` API, helping identify [why a page is incompatible with the back-forward cache](https://developer.mozilla.org/en-US/docs/Web/API/Performance_API/Monitoring_bfcache_blocking_reasons), aiding in performance improvements
- [CSS relative color syntax](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_colors/Relative_colors), which received significant publicity

I'm currently working on CSS anchor positioning, a new spec coming to Chrome and soon to other browsers. This feature simplifies anchoring UI elements, like context menus, to each other, eliminating the need for complex positioning scripts. Anchor positioning will be released in Chrome 125 around the middle of next month, and I aim to document it before then.

Thanks to everyone who reviewed my work, helping to get these features published.

## Closing comments

[Vadim] We'll figure out the date for the next community call, which might be in June. That's all for today. Have a great day, and see you next month or in pull requests or issues on GitHub!
