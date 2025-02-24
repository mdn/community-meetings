# Minutes from MDN community meeting - 23rd July 2024

**Attendees:** Ruth John (@Rumyra), Vadim Makeev (@pepelsbey), Pranshu Khanna (@pransh15), Dipika Bhattacharya (@dipikabh), Claas Augner (@caugner), Florian Scholz (@elchi3), Brian Smith (@bsmth), Andi Piper (@argl), Alejandro Alcalá (@GrayWolf9)

**Host:** Pranshu Khanna (@pransh15)

## Intro and overview

[Pranshu] Welcome to the July community call! If you're not a part of our Discord, please [join the MDN community](https://mdn.dev/discord). While you're in MDN spaces, make sure that you follow the [Mozilla Community Participation Guidelines](https://www.mozilla.org/en-US/about/governance/policies/participation/).

## MDN Birthday! (@pransh15)

[Pranshu] Thank you for joining us today for this special edition of our community call. We are thrilled to have you all here as we celebrate a significant milestone – MDN's 19th birthday! 🥳

Over the past 19 years, MDN has grown and evolved, becoming an invaluable resource for developers worldwide, and everyone on the call has contributed to making it what it is today. We are very grateful!

Since it is MDN's Birthday, that also means as if it's your birthday. So, Happy Birthday everyone! 🍰

## Updates from GitHub Work Week (@pransh15)

[Pranshu] We are excited to let the community know that we have wrapped up the GitHub work week and will implement the following changes:

- We held a GitHub work week to focus on how we work in sync with the community on GitHub.
- Focused on Stale PRs and Issues across the org. We closed a lot of issues, but the aim was never to get it below a target number.
- Discussed issue triage guidelines.
- Reworked teams to a new system that organizes them via team (e.g., MDN, Contributors, Peers, etc.). That includes removal of some teams like `yari-content-{locale}`, `mdn-{function}` that were based on repo access, etc.
- Reviewed access rights to all repositories.
- Evaluated our current pull request review process, received feedback from community members, and explored options for improvement.
- Closed/responded to old discussions (pre-2023)

You can read the full update in [GitHub Discussions](https://github.com/orgs/mdn/discussions/708).

## Scrimba Curriculum & MDN HTTP Observatory Feedback (@pransh15)

[Pranshu] MDN launched two new initiatives this month, [the new MDN HTTP Observatory](https://developer.mozilla.org/en-US/observatory) and [MDN's partnership with Scrimba](https://developer.mozilla.org/en-US/blog/mdn-scrimba-partnership/). We are open to feedback from the community.

## Reviewer and Localization Meeting (@pransh15)

[Pranshu] In the coming weeks, I wanted to propose starting a new Reviewer's & Localization meeting to discuss content focused topics on things the community and reviewers would like to discuss progress with the MDN Team and move forward with certain topics.

[Florian S] We used to have a weekly editorial meeting similar to this, and I'm glad we are bringing a similar version back.

## New callouts system (@pepelsbey)

[Vadim] There is an update on the new callout system, I'm not sure what the official terminlogy is, GitHub calls them Alerts (also known as admonitions in other systems).
This is the change:

Old method:

```md
> **Note:**
> This is a note
```

New method:

```md
> [!NOTE]
> This is a note
```

[Brian] This changes for folks who translate content as well, so `**Note:**` will have to be changed to `[!NOTE]` and so on.
It looks like [we will not be localizing the keywords](https://github.com/mdn/yari/pull/11108#issuecomment-2163751845) in the source so `WARNING` will be used in all locales in markdown, but displayed in rendered documents in a localized version.
Updates or confirmation on that coming soon, but it will be easier to maintain if the same keywords/syntax are used in all locales.
The new method is now updated on the [MDN writing guidelines](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Howto/Markdown_in_MDN#notes_warnings_and_callouts).

[Pranshu] This was it, another great community call. Thank you everyone for joining, a very Happy Birthday to MDN, and everyone! 🍰
