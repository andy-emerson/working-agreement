# The Working Agreement

**A drop-in working agreement for human–AI software collaboration.
One file — [`AGENTS.md`](AGENTS.md) — copied unchanged into your repository.**

## Why you'd want this

An AI engineer is fast, tireless, and optimistic — and the optimism is the
failure mode. Ungoverned, AI-built repositories drift the same way: the
documentation claims things that were never verified, design decisions get
made by momentum instead of intent, and the human finds out what they
"chose" after it ships. More prompting doesn't fix this; structure does.

This agreement is that structure. With it in your repository:

- **You stay the author of every decision.** The agent must surface a real
  design fork while it's still open — and nothing reaches `main` without
  your merge.
- **Your documentation stops exaggerating.** Every claim is graded against
  its evidence, and a truth-seeking documentation review — not the
  optimistic code review — decides what gets written down.
- **Every change is reviewed** — each commit before it lands, and the whole
  repository before each merge.
- **The work stays legible.** Open work lives in issues as todos, decisions,
  and deferred records; milestones carry the roadmap; nothing important
  lives only in a chat log.

## How to use it

1. **Copy [`AGENTS.md`](AGENTS.md) into your repository root.** Coding
   agents already look for that filename. Don't edit the file — it works
   unchanged, and staying unchanged is what makes updating trivial.
2. **Add a short "how we work" note to your README** — the file's final
   section lists the handful of things to record (your milestones, your
   companion documents, your conventions).
3. **Work.** Your agent reads the agreement and follows it; you play
   architect — set direction, rule on decisions, merge integrations.

When a new version ships here, updating is replacing one file.

## Built with it

Each generation of this agreement steered a real project, and each project
sharpened the agreement:

- [Servette](https://github.com/andy-emerson/servette)
- [blas.wasm](https://github.com/andy-emerson/blas.wasm) — SIMD-tuned BLAS
  for WebAssembly, bit-identical by design
- [lua.wasm](https://github.com/andy-emerson/lua-wasi) — Lua for the WASM
  sandbox, interpreter and AOT

## Versioning

Semantic versioning on the file itself — any change bumps it, so a deployed
copy can be compared to a release by hash. Current: **v1.12.0**. Versions
below 1.11.0 are prehistory: the agreement evolved across eleven
repositories before being versioned.

## Contributing

Improvements are welcome as pull requests — which is the agreement applied
to itself: anyone may play engineer; only the architect merges.

## License

[CC BY 4.0](LICENSE.md). Copy it, adapt it, build with it — the attribution
already rides in the file's front matter.
