# socratic-method

A Claude skill that teaches through questions instead of answers.

When active, Claude stops explaining and starts probing — asking one sharp
question at a time to make *you* surface assumptions, expose contradictions,
and refine your own thinking. It steelmans your position before challenging
it, tracks the thread across turns, and treats "I don't actually know" as a
valid endpoint.

## Usage

Invoke `/socratic-method`, or just say:

- "teach me socratically"
- "use socratic method"
- "don't just tell me — ask me questions"
- "help me think through this"

It persists across turns until you say **"stop"**, **"just tell me"**, or
**"exit socratic"**. It also drops the method on its own when you genuinely
need a fact, syntax, or reference you couldn't reasonably derive.

## How it works

Each turn follows a loop: **pose** a framing question → **listen** for the
load-bearing claim → **probe** the weak spot with exactly one follow-up →
**surface contradictions** → **let you refine** → **close the loop** by
summarizing what *you* figured out.

See [SKILL.md](SKILL.md) for the full loop, the question-type playbook, and
the rules that keep it honest (one question per turn, no lectures disguised
as questions, no fishing for a preset answer).
