# The Working Agreement

A working agreement for building software with AI agents.

One file — [`AGENTS.md`](AGENTS.md) — simply copy+paste into your repository.

## Why you'd want this

An AI engineer is fast, tireless, and optimistic — and the optimism is the failure mode. Ungoverned, AI-built repositories drift the same way: the
documentation claims things that were never verified, design decisions get made by momentum instead of intent, and the human finds out what they
"chose" after it ships. More prompting doesn't fix this; structure does.

This agreement is that structure. With it in your repository:

- **You stay the author of every decision.** The agent must surface a real design fork while it's still open — and nothing reaches `main` without
  your merge.
- **Your documentation stops exaggerating.** Every claim is graded against its evidence, and a truth-seeking documentation review — not the
  optimistic code review — decides what gets written down.
- **Every change is reviewed** — each commit before it lands, and the whole repository before each merge.
- **The work stays legible.** Open work lives in issues as todos, decisions, and deferred records; milestones carry the roadmap; nothing important
  lives only in a chat log.

## How to use it

1. **Copy [`AGENTS.md`](AGENTS.md) into your repository root.** Coding agents already look for that filename. The license lets you
   change the file, but an unedited copy is what keeps updating trivial — one file, replaced whole — and lets any copy be checked against a
   release. If you use Claude Code, also add a `CLAUDE.md` that points to `AGENTS.md`:

   ```markdown
   Read @AGENTS.md — the working agreement for this repository.
   Do not add guidance here; this file stays a pointer.
   ```

2. **Put your repository's specifics in your README.** The agreement sends agents there for everything it deliberately doesn't say: where open work
   is tracked (todos, bugs, deferred decisions), your milestones and roadmap, which documents hold the design, and any conventions of your
   stack.

3. **Work the process.** You're the architect: answer the three questions with your agent at each pass, rule on deferred decisions, and perform
   every merge. Your agent is the engineer: it plans, builds, gathers the evidence, and proposes merges — nothing lands without you.

When a new version ships here, updating is replacing one file.

## Built with it

Each generation of this agreement steered a real project, and each project sharpened the agreement:

- [Servette](https://github.com/andy-emerson/servette) - A simple, secure static-site server
- [blas.wasm](https://github.com/andy-emerson/blas.wasm) — SIMD-tuned BLAS for WebAssembly, bit-identical with zero dependencies
- [lua.wasm](https://github.com/andy-emerson/lua-wasi) — Lua for the WASM sandbox, interpreter and AOT

...and more.

## Versioning

Semantic versioning on the file itself — any change bumps it, so a deployed copy can be compared to a release by hash. Current: **v1.12.1**. Versions
below 1.12.0 are prehistory: the agreement evolved across eleven repositories before being versioned.

## Contributing

Improvements are welcome as pull requests — which is the agreement applied to itself: anyone may play engineer; only the architect merges.

## License

[CC BY 4.0](LICENSE.md). Copy it, adapt it, build with it — the attribution already rides in the file's front matter.
