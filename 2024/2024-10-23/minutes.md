# Minutes from MDN community meeting - 23rd October, 2024

**Attendees:** Ruth John (@Rumyra), Vadim Makeev (@pepelsbey), Pranshu Khanna (@pransh15), Claas Augner (@caugner), Brian Smith (@bsmth), Andi Piper (@argl), Florian Dieminger (@fiji-flo)

**Host:** Pranshu Khanna (@pransh15)

Pranshu: All right, welcome to the October community call for MDN. I am very happy that fall is upon us and so is this call. This month, we're starting with the agenda actually and to share the agenda in the chat and use this opportunity to remind again that this is Mozilla space and we expect everyone to abide by the CPG. Everyone's protected by the CPG. And in general, just don't be rude to folks.

Pranshu: Now, jumping on to the agenda, team updates. First up is me. The community page is now live! We've been working on it for two and a half months to transform it from a simple resource into a hub for contributors, providing recognition, guidance, and connection through community calls and Discord. I'm thrilled with the redesign, and this is just the first iteration—more updates will come. If you have feedback or suggestions, please let us know. The link is in the chat!

Pranshu: Moving to team updates. First up, Brian.

Brian: Thanks, Pranshu! My focus for the next two months is consolidating MDN examples from external repositories into Markdown files within the content repo. This reduces maintenance overhead, prevents code duplication, and streamlines updates.

Brian: Our goal is to move examples embedded on MDN pages directly into Markdown, starting with CSS examples. This will improve tooling, linting, and consistency across repositories.

Brian: We currently have 140 repositories, with 28 related to examples. The plan is to automate much of the migration while ensuring manual checks. The first step is breaking down a large pull request (130 files changed) into smaller, manageable ones.

Brian: This shift will also integrate better with MDN's code editors and Playground, leading to a more unified and efficient system. The next steps include tracking progress and refining automation efforts.

Brian: This is a great opportunity for contributors! There will be a tracking issue and instructions for those who want to help. Let me know if you have any questions.

Pranshu: I like this! Quick question—we currently have 20+ repositories for examples. What's the goal?

Brian: Ideally, we reduce them to one active repo, archiving the rest. We need to avoid maintaining duplicate code while ensuring smooth updates. The first step is focusing on six key repositories, starting with CSS examples.

Pranshu: Love it! Easier to maintain.

Brian: Exactly.

Pranshu: Any questions or feedback? Otherwise, that wraps up today’s updates. The floor is open for any additional discussions.

Florian: I wasn’t sure I’d be ready, but I’ve added myself to the agenda right now and will share this early. We’ve been working on an iteration of the build system—everything stays the same, just better and more efficient.

Florian: A key update is the new sidebar folder, where sidebars are now easily editable YAML files instead of macros. This simplifies maintenance and translation, as all translations will now be handled within content, removing the need for Yari-based translations.

Florian: The new project, RARI, is in its final stages. We’ve been releasing builds on GitHub, and while it’s not yet ready for full use, we’re automating the publishing process via npm. The goal is a seamless rollout, ensuring no disruption to current workflows.

Florian: RARI will allow users to opt into the beta with a simple command and integrate effortlessly with existing content repositories. While nothing major will change immediately, this update sets the stage for faster builds, better automation, and more streamlined content management.

Florian: We're making this update with feature parity, so changes will be minimal. Some improvements include better automation for badges and external links. A major benefit is faster local builds—MDN content now compiles in 4-5 seconds, making it easier to track changes across pages.

Florian: Our goal is to make the system more modular and flexible, allowing for faster iterations. A beta version should be ready by Friday or early next week, with the only major change being sidebar migration. Feedback is welcome!

Vadim: RARI is a binary. How does installation work, and is it compatible with Windows, Linux, and other platforms?

Florian: Yes, there are some limitations. We’ve created an npm package to handle installation, but binary distribution remains a challenge in today’s fragmented environment.

Florian: We created an npm package to simplify installation—it downloads and executes the binary automatically. Currently, we support Linux, macOS, and Windows (x86 & ARM), covering most users. If WebAssembly stabilizes, we may expand support further.

Vadim: So it’ll feel like a regular npm package?

Florian: Exactly! Just install it, and it works.

Brian: Any plans for improving the flaws dashboard or a successor?

Florian: The current flaws system is slow and flawed, but necessary. We’re logging issues by category and working on automated fixes, including better tracking of macro errors and broken links. Our goal is to reduce flaws to zero, making maintenance easier.

Florian: A key improvement is automating link fixes, and replacing incorrect URLs at scale. We’ll test this in Berlin, focusing on cleanup before enforcing stricter rules.

Brian: Sounds great!

Pranshu: That wraps up the October Community Call—thanks, everyone! See you at the content call on Monday.
