
# 01 — LLM Pins

**Marking important moments in long AI conversations.**

---

## The problem

Heavy LLM users who maintain long conversations for learning, brainstorming, planning, or goal tracking lose continuity when they cannot mark or navigate important moments within a conversation.

When a conversation grows long, the only way to find something from earlier is to scroll. Sometimes sections disappear entirely due to context compression. There is no way to mark a line in the moment you notice it matters.

---

## User research

I reached out to people across different backgrounds and asked one question: when a chat gets too long, do you face the scrolling problem?

| User | Use case | Workaround | Works? |
|------|----------|------------|--------|
| Engineering student | Learning Python | Re-prompts to retrieve info | Partially |
| Data analyst | Daily work with ChatGPT and Copilot | Opens a new chat, transfers context | No |
| Consultant | Extended work sessions | None | No |
| Medicine student | Learning and studying | None | No |
| My mother | Has favourite book narrated by ChatGPT | None | No |
| 3 other professionals | Various | None | No |

More than 20 people validated. None of them developers. None with workarounds that actually work.

---

## What already exists

### Level 1 — across chats
Pinning and organising chats into folders. Exists natively. Does not solve the problem.

### Level 2 — within a chat
Chrome extensions like Claude Toolbox and ChatGPT Bookmark attempt message-level bookmarking.

Problems:
- Chrome desktop only — no mobile support
- Require installation and setup
- Not available natively in the interface
- Reviews show poor reliability

### Level 3 — marking in the moment
Nobody has built this. This is the gap.

There is also an open feature request on Anthropic's own GitHub:
[github.com/anthropics/claude-code/issues/32874](https://github.com/anthropics/claude-code/issues/32874) — marked inactive.

---

## Why this is not a memory problem

Persistent memory solves what the model knows across sessions. It does not solve how you navigate what was said within a conversation.

Even with perfect persistent memory, you would still scroll to find a specific moment.

**Control F or any other search method cannot fix this either.** To search, you need to know exactly what you are looking for. But this is not a search problem. When you are learning or brainstorming, you notice something matters in the moment — before you know you will need to find it later.

Think about a book. As you read, you highlight sentences. Not because you plan to search for them later. Because in that moment, something matters. At the end of the chapter you do not reread everything. You look at what you marked.

That is what is missing.

---

## Who this is for

Everyone. Not just developers.

ChatGPT, Claude, and every other chat agent are not just for tech and IT people. They are for everyone from all possible backgrounds. Because whether we like it or not, LLMs are slowly becoming systems people will learn from, search through, trust and interact with daily. Almost like a second brain.

The solution should be just as inclusive.

---

## The proposed solution — Pins

A native marking feature within a longitudinal long conversation. 

### How it works

**Marking:**
Select any text in a conversation. A hover or selection menu appears with a Pin option. The selected text gets a dark teal background with white text — visually distinct, immediately clear.

**The Pins pane:**
A collapsible panel that is closed by default. Toggle it open via a Pins button in the chat header. On desktop and mobile: slides in from the right. 

The pane shows all pinned lines in order, one below the other. Clean and scannable.

**Navigation:**
Click or tap any pin in the pane to jump directly to that moment in the conversation.

**Compaction:**
If a section has been compressed, the pin remains visible in the pane but is shown at reduced opacity with a "compressed" label honest about its limitation rather than a dead link.

### Why this works

- Maps to the book highlighter mental model — no learning curve
- Works identically on mobile and desktop
- No installation, no setup, no subscription
- Available to everyone by default

### V1 scope — deliberately simple

One highlight colour. No tags. No folders. No search within pins. Just mark, see, jump.

Ship this and learn from how people use it. The data will tell you whether colour coding or search is needed in V2.

---

## What I learned from this process

I started this thinking I wanted a bookmark feature. Through three LinkedIn posts, user research, and investigating existing tools, I arrived at something more precise:

**The problem is not retrieval. It is marking.**

Retrieval assumes you know what you are looking for. Marking is about capturing something in the moment before you even know why it matters. Those are fundamentally different problems and they require fundamentally different solutions.

---

*Priyanka Ranganathan — [priyarb.com](https://www.priyarb.com)*
