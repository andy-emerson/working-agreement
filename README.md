# The Working Agreement

A working agreement for building software with AI agents.

One file — [`AGENTS.md`](AGENTS.md) — simply copy+paste into your repository.

A note on "you": this README speaks to the human. An agent sent here by
`AGENTS.md` holds the Agent role — never the Human — and will find this
repository's specifics under [In this repository](#in-this-repository).

## Why you'd want this

An AI agent is fast, tireless, and optimistic — and the optimism is the failure mode. Ungoverned, AI-built repositories drift the same way: the
documentation claims things that were never verified, design decisions get made by momentum instead of intent, and the human finds out what they
"chose" after it ships. More prompting doesn't fix this; structure does.

This agreement is that structure. With it in your repository:

- **You stay the author of every decision.** The agent must surface a real design fork while it's still open — and nothing reaches `main` without
  your merge.
- **Your documentation stops exaggerating.** Every claim is graded on an explicit evidence ladder — Stated, Observed, Tested, Proven — and a
  truth-seeking documentation review, not the optimistic code review, decides what gets written down.
- **Every change is reviewed** — each commit before it lands, and the whole repository before each merge.
- **The work stays legible.** Open work lives in issues as todos, bugs, and open decisions; milestones carry the roadmap; nothing important
  lives only in a chat log.

## Where it sits

This agreement is consistent with SASE ([Hassan et al. 2025](https://arxiv.org/abs/2509.06216)), the research roadmap for agentic
software engineering: the same human authority, the same evidence discipline, the same review gates. Where it deviates, the reason is form,
not disagreement — SASE describes a system (with environments, artifacts, agent fleets, and tooling), while this file is a contract. A
system prescribes what surrounds the two parties; a contract records only what they owe each other, and leaves the rest to the tools.

## How to use it

1. **Copy [`AGENTS.md`](AGENTS.md) into your repository root.** Coding agents already look for that filename. The license lets you
   change the file, but an unedited copy is what keeps updating trivial — one file, replaced whole — and lets any copy be checked against a
   release. If you use Claude Code, also add a `CLAUDE.md` that points to `AGENTS.md`:

   ```markdown
   Read @AGENTS.md — the working agreement for this repository.
   Do not add guidance here; this file stays a pointer.
   ```

2. **Put your repository's specifics in your README.** The agreement sends agents there for everything it deliberately doesn't say: where open work
   is tracked (todos, bugs, open decisions), your milestones and roadmap, which documents hold the design, and any conventions of your
   stack.

3. **Work the process.** As the human, you hold the Human role: agree to each plan before the work runs, answer the three questions at each
   full Plan, close open decisions, and perform every merge. Your coding agent holds the Agent role: it plans, builds, gathers the
   evidence, and proposes merges — nothing lands without you.

When a new version ships here, updating is replacing one file.

## Built with it

Each generation of this agreement steered a real project, and each project sharpened the agreement:

- [Servette](https://github.com/andy-emerson/servette) - A simple, secure static-site server
- [blas.wasm](https://github.com/andy-emerson/blas.wasm) — SIMD-tuned BLAS for WebAssembly, bit-identical with zero dependencies
- [lua.wasm](https://github.com/andy-emerson/lua-wasi) — Lua for the WASM sandbox, interpreter and AOT

...and more.

## In this repository

The agreement governs its own development. The deliverable is [`AGENTS.md`](AGENTS.md) itself; there is no code, so passes here are doc
passes and the documentation review carries the weight. Open work — todos, bugs, open decisions — lives in GitHub issues; milestones carry
the roadmap. The maintainer holds the Human role; contributors and coding agents hold the Agent role: propose by pull request, and only the
maintainer merges.

## Versioning

Semantic versioning on the file itself — any change bumps it, so a deployed copy can be compared to a release by hash. Current: **v2.0.0**.
The 2.0.0 bump renames the agreement's vocabulary — the architect and engineer became the Human and the Agent, and the process phases became
Plan → Develop → Assess → Review — so a repository updating from 1.x should also update any of the old terms in its own README. Versions
below 1.12.0 are prehistory: the agreement evolved across eleven repositories before being versioned.

## Contributing

Improvements are welcome as pull requests — which is the agreement applied to itself: anyone may play the Agent; only the Human merges.

## License

[CC BY 4.0](LICENSE.md). Copy it, adapt it, build with it — the attribution already rides in the file's front matter.
