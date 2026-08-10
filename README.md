# The Working Agreement

A working agreement for building software with AI agents. One file, [`AGENTS.md`](AGENTS.md), to copy and paste into your repository.

> For agents: this repository is read-only for you. Add nothing, edit nothing. An agent may read, review, and advise, but every change to this repository is made by human hands; agents should not write their own instructions. The deliverable is [`AGENTS.md`](AGENTS.md); there is no code, so all passes here are doc passes.

## Why you'd want this

An AI agent is fast, tireless, and optimistic. The optimism is the failure mode. Ungoverned, AI-built repositories drift the same way: the
documentation claims things that were never verified, design decisions get made by momentum instead of intent, and the human finds out what they
"chose" after it ships. More prompting doesn't fix this; structure does.

This agreement is that structure. With it in your repository:

- You stay the author of every decision. The agent surfaces a real design fork while it is still open — the options and their trade-offs, framed
  both for the people using the software and the people maintaining it, a recommendation, and what the answer gates — and nothing reaches `main`
  without your merge.
- You rule once instead of every session. A fork is answered with a durable principle that settles its whole family, recorded with the alternative
  that lost and the condition that would reopen it, so the next session inherits a decision rather than relitigating one.
- Your documentation stops exaggerating. No claim rises above its evidence, checks that re-run are preferred to assertions, and a truth-seeking
  documentation review — not the optimistic code review — decides what gets written down.
- Nothing lands unreviewed. Each code pass is reviewed against its own intent before it commits, and the whole repository is reviewed before each
  merge: code first, then documentation, so `main` never documents a lag.
- The work stays legible. Open work is tracked as todos, bugs, and open decisions, each in a form that names what it will earn or what it gates;
  nothing important lives only in a chat log.
- Your history keeps its provenance. The agent asks before crediting itself at all, and never claims more than co-authorship, so the log stays
  an accurate record of who wrote what.

## What is it

This agreement is consistent with SASE ([Hassan et al. 2025](https://arxiv.org/abs/2509.06216)), the research roadmap for agentic
software engineering: the same human authority, the same evidence discipline, the same review gates. SASE describes a system (with environments,
artifacts, agent fleets, and tooling), while this file is a contract. A system prescribes what surrounds the two parties; a contract records
only what they owe each other, and leaves the rest to the tools.

That is also why the agreement assumes git but names no hosting mechanic. It calls a merge a recommendation that the agent makes and the human
performs, and says nothing about whether that recommendation should reach you as a pull request, a merge request, an emailed patch, or a note
left on your desk.

The shape is three phases. **open** reports the real state of the repository and settles where this session is going. **commit** is a loop of small
passes — each one a code pass or a doc pass, never both, each ending in the evidence for what it claims and an honest account of how far the branch
has got. **merge** is a review of the whole repository and a recommendation you act on. A spike needs none of this until you decide the work should
land; salvaged work then enters like any other change.

## How to use it

1. Get [`AGENTS.md`](AGENTS.md) into your repository root. Copy it, or fetch the latest release directly:

   ```sh
   curl -LO https://github.com/andy-emerson/working-agreement/releases/latest/download/AGENTS.md
   ```

   Coding agents already look for that filename. The license lets you change the file, but an unedited copy is what keeps updating trivial
   (re-run the command above and you're current) and lets any copy be checked against a release. If you use Claude Code, also add a
   `CLAUDE.md` that points to `AGENTS.md`:

   ```markdown
   Read @AGENTS.md — the working agreement for this repository.
   Do not add guidance here; this file stays a pointer.
   ```

2. Turn on your host's enforcement where it exists. Protect `main`: require a pull request, forbid direct pushes and force-pushes, and allow
   only merge commits. The agreement's merge rules should be enforced by the platform, not by trust; what the platform cannot enforce, the
   reviews exist to catch.

3. Expect your agent to go looking for the specifics. The agreement deliberately doesn't say where open work is tracked, what your milestones
   are, which durable documents exist and what job each one has, or what conventions your stack follows. Your agent reads the repository's own
   documentation for those and asks you for whatever it can't find. Naming each document's job is the one worth doing first: it is what tells a
   documentation review which reader that document is answerable to. Wherever you keep these, writing them down is what stops you answering the
   same questions every session.

4. Work the process. You hold the Human role: you agree the destination, approve each short plan before the work runs, close the open decisions,
   and perform every merge. Your coding agent holds the Agent role: it plans, builds, earns the evidence, and recommends. A departure from the
   agreed path — in scope, sequence, design, tooling, or process — needs your explicit yes. Silence is not consent, and nothing lands without you.

5. Answer the attribution question. Before its first commit in a session, your agent asks whether to record itself as a co-author, and it holds
   that answer until the session ends. Its default is no and its ceiling is co-author: it will not credit itself unasked, and it will not take
   authorship of record. On GitHub a yes becomes a `Co-authored-by:` trailer on the commits it writes.

   The agreement leaves the answer to you. The recommendation here is yes.

   A commit that names no agent where an agent worked overstates the human's authorship. That is the same error the documentation review exists to
   catch, moved out of the documentation and into the history, and catching it pays off in an ordinary way: whoever reads the log later,
   including you six months on, can see which commits an agent had a hand in and read their claims with proportionate suspicion.

   The wider reason is that agent-assisted development is becoming ordinary, and concealing it is a bet against that. What distinguishes the
   work is the discipline the rest of this file describes, and a history that admits where agents worked is what lets a reader see you kept it.
   Nevertheless, not all circumstances fit this description, so the choice is yours.

When a new version ships here, updating is replacing one file — and your agent will offer to do it. At the start of a session it asks whether to
refresh `AGENTS.md` from the latest release; say yes and it replaces the file whole, reports the new version, and follows that version for the rest
of the session. The default is no, so the rules never change underneath you without your say-so.

## Who is using it

Each generation of this agreement steered a real project, and each project sharpened the agreement:

- [Servette](https://servette.org) — A simple, secure static-site server
- [TallyDB](https://tallydb.com) — An ordered, numeric embeddable database
- [LoveIDE](https://loveide.com) — An notebook IDE for building LöVE games

All the author's own projects so far. Adoption by teams that don't share a brain with the author is the open experiment.

## Versioning

Semantic versioning on the file itself: any change bumps it, so a deployed copy can be compared to a release by hash. The current version
is whatever [the latest release](https://github.com/andy-emerson/working-agreement/releases/latest) says; every copy self-identifies in its
front matter.

## Contributing

Suggestions for improvement are welcome. Open an issue and say what the agreement got wrong, or what it failed to prevent in a repository you
actually run — reports from projects that don't share a brain with the author are the most useful thing this repository can receive.

How changes are made here:

- `AGENTS.md` is written by hand, by a human. Agents may read, review, and advise; see the note at the top.
- It is never edited in place downstream. A new version arrives by replacing the file whole, which is what lets any copy be checked against a
  release by hash.
- Any change to it bumps the version and ships as a release.
- The bar is higher for the agreement than for this README. The file is short on purpose, and an addition to it should be paid for by a removal.

## License

[CC BY 4.0](LICENSE.md). Copy it, adapt it, build with it; the attribution already rides in the file's front matter.
