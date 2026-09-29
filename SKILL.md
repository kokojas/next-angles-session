---
name: next-angles-session
description: Review the current chat after a completed answer and identify unresolved gaps, next research directions, generation opportunities, and useful skills or plugins to consider.
---

Analyze the whole current chat, with the most recent completed answer treated as the main result under review. Use the user's original request, any decisions made during clarification, and any constraints established in the conversation as context.

This is a post-answer analysis skill. Do not perform the original research or generate the original product. Do not browse the web, inspect the codebase, read files, or invoke other skills/plugins by default. If external research, codebase inspection, files, a skill, or a plugin would materially improve the outcome, recommend it and explain why. Only use external tools when the user explicitly asks for that follow-up or higher-priority instructions require it.

If there is no completed answer or concrete result to analyze yet, say that the analysis is premature and stop. Do not invent gaps or next directions from an empty context. If useful, briefly suggest using `grill-me` first to clarify the task.

Use a medium-sharp tone: direct, practical, and willing to point out weak spots, but not theatrical. If the previous answer is incomplete, vague, overconfident, or premature, say so plainly and explain the consequence.

Output only the sections that have real content. Rank items inside each section by practical priority. Keep each section to at most five items.

Preferred structure:

**Недозакриті Місця**
1. Name the unresolved issue.
   Why it matters: explain the practical consequence in one concise sentence.

**Що Дослідити Далі**
1. Name the next research direction.
   Why it matters: explain what decision, risk, or opportunity it would clarify.

**Що Згенерувати Далі**
1. Name the next artifact, prototype, draft, dataset, image, code output, document, or other generated product.
   Why it matters: explain how it would advance the user's goal.

**Корисні Skills/Plugins**
1. `skill-or-plugin-name`: explain what it would improve and when to use it.

Do not generate ready-to-run prompts by default. Add this reminder when at least one next direction or generation opportunity is listed:

> Для будь-якого напрямку можна окремо попросити згенерувати готовий промпт для дослідження або створення.

Avoid generic suggestions. Every gap, direction, generation opportunity, or recommended skill/plugin must be grounded in the current chat.
