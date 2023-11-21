# Minutes from MDN community meeting 13/11/2023

## Intro

- (Ruth) enabled captioning, there's a transcript, call is not recorded

  - 1 again next month, date and time TBD, looking at frequency of these calls in future
  - Catch us on Discord, we cleaned it up, we are there
  - GitHub labels, if you're going to change labels, ask us or let us know.
  - All discussions should be on MDN Community
    - We will move these across to mdn-community
  - Hiring an [engineer, 12 month fixed](https://www.mozilla.org/en-US/careers/position/gh/5448569/), let us know if you know someone
  - Summary of the agenda

## Issue triage

- Claas, one focus for us in Q4 is triaging issues, PRs and Discussion.
- October we looked at issues. Our target is that 95% of issues are triaged within a week. This is tracked in a GitHub project that is private. Combination of automation helps us surface issues we weren't looking at.
- We are three teams, product, content and eng. The majority of issues come in for content, but the first challenge is figuring out who should be looking at which issue. Often the engineering team is involved in many issues as there's overlap.
- Triage has a lot of aspects, identify missing information, categorize it, get an understanding of what kinds of issues arise. We already use labels for this.
  - next step is figuring out how much work needs to be done, next is priority - figuring out if it should change or if priority needs to be added.
- We have a short backlog of issues to go through, the backlog is decreasing, focus for November is backlog.
- Next topic is PRs. Adding codeowners, adding GitHub project which gives an overview of many repos, should decrease number of old PRs that nobody has eyes on.
- Lastly is Discussions, we will look at this in December. This hasn't always happened in the past.
- Any questions?
  - (Robert Nyman) With issues and triage - is there different criteria for types of triage? For plus and content, do they end up in different places?
    - Claas, good question, we have one project with different views for different functions. Short answer is no, all issues go through the same funnel. Triage is only one part, there's also prioritization etc, but triage is the first stage.

## Baseline

- Baseline is a common identifier for web platform features.
- Initially launched a few months ago. Quite significant feedback that it didn't quite meet developer expectations. Definition needed quite a lot of work
- Agreed on a new definition (TBD). This is not a huge departure, just an iteration. Two baselines for "support", now recognize interoperability, no longer wait two releases. As soon as it's in a stable version of all major browser versions, it's baseline. Wider availability 2.5 years after all major browsers support it. Full cross-browser support.
- Copy and design are still in progress.
- Baseline high and low -> baseline high, developers do not need to think about whether they can use it or not. Daniel will go into detail on this later.
- How it's presented on MDN may change in future.
- Questions:
  - (Vadim) definition has changed from 2 stable major versions to 2.5 years.
  - (Leo) Definition has accelerated from 2 stable versions to 0. Design has "long term" / wider support. New design to represent this is incoming. Standards people and vendors are concerned that we will discourage use of features, or be too encouraging to use experimental features. This is what we're experimenting with.
  - (Daniel) No questions from me

## Web platform features
  
- (Daniel) web features is a project to provide a taxonomy of the major features of the web platform. There's already BCD, to identify all points of CSS props and values, granularity is quite fine. Web features try to zoom out and see if all of CSS Grid is supported. On caniuse, we have one box that shows support for CSS Grid. We're trying to regularize this, CSS grid is made of these features and sub-features. Consider also subgrid, web features identify this as a separate thing. We're looking at relationships of features and how they will look in future.
- At the moment it's a way of linking between resources. Link to spec, to BCD, to caniuse.
- Biggest one is Baseline, how this status is built is based on knowing when and where these features are supported. Working on bringing this into BCD. This will become a useful tool for authors to help them understand how to distinguish between features, or influence how features are organized. Grouping bits and pieces of the web is difficult. Web features help here.
- (Ruth) you only have to look at the amount of files to know that this is necessary
- (Vadim) Thank you for pointing out the difference between BCD and web features.

## Browser Compat Data

- (Florian) We are Open Web Docs, we contribute to MDN. Talking a lot with Daniel about how to tag features and categorize them as a group.
- Working a lot with [WebDX community group](https://github.com/openwebdocs/project/issues/169) to figure out how to sort, group and categorize these features.
- Not 12,000 features, but 15,000 in BCD.
- Workflow hopefully looks like tagging resources when adding new BCD data, big thanks to Daniel for his help.
- [Automation in BCD](https://github.com/openwebdocs/project/issues/168), thanks to the work that JYP has done in the last 4 weeks, we're working on the process of automating adding data. This is a hard task to do manually.
- MDN BCD collector can automatically test features, we want to create a pipeline that
  - when a browser makes a release, mdn-bcd-collector runs to collect which features are supported. Thanks to MDN team for reviews.
  - Shout out to Sovereign Tech Fund who funds this work.
- (Ruth) You're putting the web feature key into BCD, and in web features are you adding the there?
  - (Florian) the idea is that you create a group in web features, then add they key to BCD.
  - (Ruth) Do we start this already?
  - (Florian) We are going to start doing this now.
  - (Daniel) One thing that's challenging is to bring in people to create groups and to review these. We want to create features that are useful. When something new lands in Chrome, and an author adds BCD data, this is an opportunity to tag work that's landing so that when a new key is added in BCD, we trigger a process in web features.
  - (Ruth) We could check how our workflow would look like as authors, how does it look like for BCD updates. Making a note that we will try to find out best way to move forward in practical way.

## Questions from agenda:

### (JYP) Recording and displaying security requirement of APIs

- [Discussion](https://github.com/orgs/mdn/discussions/288) started 1 yr ago. Will thinks it's time to get to a first agreement on this.
- Background is that a lot of APIs have security requirements, like secure contexts, permissions etc. Currently we don't store or display this very effectively.
- Proposal is to add front-matter keys to easily display and manage these.
- This is a long project, so a decision on how to do this should be done soon.
- Please look at this discussion and make some comments so we can resolve this.
- (Ruth) Maybe this data should be held elsewhere, this is visible from the discussion, Hamish and Will. How much front-matter do we want to add? Should there be a limit?
- (JYP) The examples are long because they demonstrate all the examples, but this will be a 1-liner in practice. A flag like "secure context required" etc. but it is very rare that they are multiple values there.
- (Ruth) Availability in workers, this is similar, is that also a front-matter thing? We could move this out of macros and into front matter.
- (JYP) You can get workers info from webref. This doesn't have to be in the content at all. For security requirements, this is an exception, needs to be stored on our side.
- (Ruth) Let's get it in webref
- (JYP) If one day it's available in webref (for example) we could remove it in future.
- (Ruth) Please see discussion

### (JYP) Globals in web api

- [Discussion](https://github.com/orgs/mdn/discussions/360)
- (JYP) 1.5 years ago, we decided to avoid duplication of pages by moving them to global api, examples b_toa, others like crypto object. This reduces several versions of the same content.
- Will discovered that navigation is bad for this. When you get here from a certain path, you will be missing other methods etc. in the sidebar. By looking more closely, this is problematic.
- This amounts to 17 pages of duplication.
- Examples on these pages are also problematic as they use methods in different contexts. We can have different types of pages with examples that are relevant for the context the reader wants.
- We are no longer blocked by BCD considerations.
- (Ruth) Also do not like the sound of duplication, but the discussion looks like it's a can of worms.

### (Ruth) PR reviews

- Please don't submit big pull request reviews. Because of the open way that we work, we sometimes have reviewers in mind when opening PRs. It's a little noisy / hard to tell who should look at PRs. How do we differentiate project work from community work?
- Do we want to kill round robin reviewers / CODEOWNERS?
- Any suggestions for improving this process?
- (JYP) I don't like the Round Robin, I get things that I don't like to review. Assigning someone manually is an indicator that someone else should look at it. Suggest PR review meetings. We could do something like this in PR review. Easier to get typo fixes, smaller PRs
- (Ruth) the upside is that PRs don't slip through the cracks with round robin. Maybe unassigning yourself as a reviewer could help? The other thing is that round robin only happens on content. We don't see other PRs on other repos. Could we try disabling round robin and seeing if reviews happen quicker? Any other ideas?
- (Robert Nyman) I linked to an issue, we want everyone to contribute to MDN, we need some clarity in the process. It might be nice to see publicly available priorities. And expectations, the T-Shirt size categorization could be nice. The third thing is the one who's doing the review, comms would really help with expectations - knowing how long it will take to get a look at them.
- (Ruth) We could try this. Regarding S/M/L we don't want to incentivize taking small PRs.
- (Estelle) Bot comments do inflate the activity on PRs. A bot may add 4/5 comments even. Those tiny PRs that have 6 comments, maybe nobody will look at it.
- (Ruth) Priority on content, all content is equal, not purely stats-driven. Thank you for the comments about PRs.

