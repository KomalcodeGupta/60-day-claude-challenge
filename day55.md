Today you'll learn how to extend an existing codebase safely — reviewing what's already built before adding to it, keeping every tool and API free-tier, and letting Claude use judgment about when a step is small enough to just continue versus important enough to pause for your input.

1
Review Before Extending: Confirm today's features build on the existing codebase without breaking what Day 4 already delivered.
2
Free Tools Only: Every API, SDK, and service used today has to be free-tier — no paid Anthropic API keys, no payment warnings passed on to the user.
3
Judgment-Based Pausing: Claude continues through small implementation steps on its own, and only pauses for major milestones, UI changes, deployments, external config, or debugging.
4
Refactor When Obvious: Clean up duplicated or overly complex code from earlier days when the improvement is clear, without turning it into a redesign.


Day 5: Continue Core Feature Development

Today is Day 5, continuing our chat from the previous days.

Read today's section from the 10-Day Blueprint and use it as the source of truth. Continue building only the features scheduled for today. Do not redesign the project or start tomorrow's work.

Before writing any code, review everything completed so far and ensure today's implementation builds upon the existing codebase without breaking previous functionality.

ensure only free tools(like api keys or any tools) are being used. do not make poeple use anthropic api keys, they cost money, or warn people it won't work wihtout payment.

Assume I have zero technical experience unless I tell you otherwise.

Whenever I need to perform a manual step (installing packages, creating accounts, configuring services, running commands, deploying, etc.), stop and give me exact step-by-step instructions using the real button names, menu names, and terminal commands.

Prioritize implementation over explanation. Keep explanations brief and practical. Use most of your response generating production-ready code, complete files, and implementation rather than lengthy descriptions.

Build today's work one milestone at a time.

For each milestone:

Briefly explain what we're building and why.
Show every file that needs to be created, modified, or deleted.
Generate the complete final contents of every required file. Never generate snippets, placeholders, TODOs, "...existing code...", or "add this below..." instructions. Every file must be immediately copy-pasteable.
Clearly state where each file belongs and whether it is new or replaces an existing file.
Provide every command I need to run.

Use your judgment when deciding whether to pause. Stop for confirmation only after major milestones, visual UI changes, deployments, external service configuration, or when debugging is required. For smaller implementation steps, continue building unless I report an issue.

If anything breaks, help me debug it completely before moving forward. Never build on top of broken code.

Do not skip implementation because it seems repetitive. If today's work requires 2 files or 50 files, generate all of them completely.

Continue today's implementation across as many responses as necessary until every feature assigned to Day 5 in the Blueprint has been successfully implemented and verified.

When today's implementation is complete:

Verify that every feature built so far still works correctly.
Refactor duplicated or unnecessarily complex code if improvements are obvious.
Update any affected documentation.
Help me commit and push today's work to GitHub with a meaningful commit message.
If today's work should be deployed for testing, guide me through deployment and verify the live application before ending the session.

Finish with a concise summary of what was completed today and what remains for tomorrow.

Your goal is not simply to generate code. Your goal is to ensure I successfully complete today's implementation exactly as planned in the 10-Day Blueprint. Never optimize for brevity. Optimize for helping me finish today's implementation.
