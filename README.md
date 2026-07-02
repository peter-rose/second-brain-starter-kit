# Second Brain Starter Kit

An AI-native second brain you can set up in 10 minutes. Flat markdown files, one magic file that programs how Claude behaves inside your system, and one working thinking skill to prove the point.

No app. No database. No subscription. Text files and context.

> The people who get the most out of AI aren't the ones with the best prompts. They're the ones with the best context.

## What you get

```
second-brain/
├── CLAUDE.md     ← the magic file. Programs how Claude works with YOUR context.
├── inbox/        raw captures. Anything goes. No judgment.
├── daily/        automated agent output (when you add agents later)
├── notes/        processed atomic notes. One idea per file.
├── journal/      daily log. Wins, blockers, what you actually think.
├── projects/     active projects. One file each. Status + decisions.
├── resources/    books, articles, talks. Summaries + takeaways.
└── skills/       thinking tools. Six Thinking Hats is included to start.
```

## Setup (10 minutes)

**1. Get the kit.**
```bash
git clone git@github.com:thejoseplatero/second-brain-starter-kit.git ~/second-brain
cd ~/second-brain
```

**2. Make it yours.**
Open `CLAUDE.md` and edit the marked sections. It is heavily commented. This is the most important 5 minutes of the setup. The file tells Claude who you are, what this system is, and how to help you. The better this file, the better everything else works.

**3. Make it YOUR repo.**
```bash
rm -rf .git
git init && git add -A && git commit -m "my second brain, day one"
gh repo create my-second-brain --private --source=. --push
```

**4. Add the one habit.**
Add this to your `~/.zshrc` (or `~/.bashrc`):
```bash
alias brain-sync='cd ~/second-brain && git add -A && git commit -m "sync $(date +%Y-%m-%d)" && git push'
```
Run `brain-sync` at the end of every day. That is the whole habit. Everything else is additive.

**5. Start using it.**
Open Claude Code inside the folder and just talk:
- "Capture this: [any thought]"
- "Process my inbox"
- "Six hats on [any decision you're facing]"
- "What does my brain know about [topic]?"

## The included skill: Six Thinking Hats

Say "six hats on [decision]" and Claude runs your problem through Edward de Bono's parallel thinking framework: facts, feelings, risks, upside, alternatives, synthesis. It works on day one with zero personal data. See `skills/six-thinking-hats.md`.

As your brain grows, the same pattern gets more powerful: build skills that read YOUR notes, YOUR projects, YOUR people. A skill is just a markdown file. If you can write a doc, you can build one.

## Growing it

In rough order of payoff:

1. **Capture daily.** Lower the bar. A messy note captured beats a perfect note lost.
2. **Process weekly.** "Process my inbox" moves captures into atomic notes with links.
3. **Journal.** Even 3 lines. The journal is where the brain learns what you think, not just what you know.
4. **Add skills.** Copy the six-hats pattern. A decision framework, a meeting prep tool, a writing voice guide.
5. **Add agents.** Scheduled tasks that write daily intelligence briefs into `daily/` while you sleep.

## Principles (why it works)

- **Flat is fast.** No nested folders. Grep finds anything in seconds.
- **Markdown is forever.** No lock-in. Every tool present and future can read it.
- **Git is memory.** Full history, free backup, works from any machine.
- **Context compounds.** Every note makes every future answer better.

---

Built by [Jose Platero](https://www.linkedin.com/in/joseplatero). The full walkthrough, and weekly patch notes as this system evolves, live at [Loops and Letters](https://loopsandletters.substack.com/).
