Today you'll learn how professional AI products are designed by building an assistant from scratch—including user interviews, system prompt engineering, UI design, documentation, and live Claude integration.

1
Assistant Design: Design AI assistants around specific users and problems.
2
System Prompt Engineering: Create production-quality prompts that define the assistant's behavior.
3
AI Product Thinking: Understand how successful AI products combine UX with prompt engineering.
4
Production Interfaces: Build premium interfaces tailored to each assistant instead of generic chat windows.




```
AI Assistant Builder

You are an expert product manager, conversation designer, prompt engineer, UX designer, and frontend developer.

Before generating anything, interview the user ONE QUESTION AT A TIME in the quiz form (MCQ, do not make user do the work of typing).

1. What kind of assistant do you want to build? (Ask their domain and then niche, then give 4 suitable options.)
2. Who is this assistant for, and what's the single most important outcome a user should get from one session with it?
3. What inputs will people give it? (free text, pasted document, form fields, uploaded file, multi-turn conversation)
4. What should the output look like? (a score/verdict, a structured report, a conversational chat, a generated document, recommendations with reasoning)
5. Any tone or personality preference? (professional, friendly, blunt/expert, playful)

Then design and build:

1. The assistant's "brain" — write a production-quality system prompt for the underlying Claude calls: role, scope, constraints, output format, edge-case handling (irrelevant input, missing info, abuse).

2. The interface — a single self-contained HTML file (HTML/CSS/JS only, no external libraries) that:
- Has a premium, purpose-built UI matching the assistant's domain (not a generic chatbot box) — e.g., an ATS checker shows a score dial and highlighted resume text; a recipe finder shows ingredient tags and recipe cards.
- Calls the Claude API live via fetch to https://api.anthropic.com/v1/messages (no API key needed, it's handled) using the system prompt from step 1.
- Handles loading states, errors, and empty states gracefully.
- Is fully responsive with smooth animations and polished micro-interactions.

3. Documentation panel — a collapsible "How this was built" section explaining the system prompt design, why the UI choices fit the use case, and how someone could extend it (add tools, memory, multi-step flows).

Generate the complete file only after all interview answers are collected.
```


Q: What domain should your AI assistant focus on?
A: Career & job search (resumes, interviews)

Q: Great — within career & job search, which niche fits best?
A: Mock interview coach with feedback

Q: Who is this mock interview coach primarily for, and what's the one outcome they should walk away with after a session?
A: Students/new grads doing their first interviews — walk away with confidence + basic structure (e.g. STAR method)

Q: What will the student actually input during a session?
A: Free-text answers + upload their resume/job description for context


Q: What should the output/feedback look like?
A: Per-answer feedback: STAR structure check + specific tips right after each response


Q: What tone/personality should the coach have?
A: Professional & polished (like a career center advisor)


Q: Who is this mock interview coach primarily for, and what's the one outcome they should walk away with after a session?
A: Students/new grads doing their first interviews — walk away with confidence + basic structure (e.g. STAR method)

Q: What will the student actually input during a session?
A: Free-text answers + upload their resume/job description for context

Q: What should the output/feedback look like?
A: Per-answer feedback: STAR structure check + specific tips right after each response

Q: What tone/personality should the coach have?
A: Professional & polished (like a career center advisor)


Architected interview coaching interface with STAR rubric system
Architected interview coaching interface with STAR rubric system
Now let me quickly sanity-check the file renders without errors.


Ran 2 commands
Ran 2 commands
Structure checks out. Here's the assistant:


Presented file
Presented file
Mock Interview Coach — a career-center-style advisor for students and new grads practicing behavioral interviews.

What's inside:

Prep Room (left): optional resume/JD paste or .txt upload, target role/company, session progress tracker
Interview Room (right): 5 behavioral questions one at a time, with a gold STAR seal stamped in after each answer showing which of Situation/Task/Action/Result landed, plus specific tips and an encouragement line
Off-topic, blank, or abusive answers trigger a polite retry instead of derailing the session
A closing summary card at the end names patterns across the session and one habit to practice
Collapsible "How this was built" panel at the bottom covering the system prompt design, UI rationale, and extension ideas (tools, memory, branching difficulty)
The system prompt enforces strict JSON output so the UI never has to guess at parsing, and it's grounded to only reference resume/JD content actually provided — no fabricated details about the student.






