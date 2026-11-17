# Benchmarks

Static site at `https://jxb1st.github.io/benchmark-collection/`: one page per benchmark (InteractionBench, IVG-Bench, StreamingBench, OVO-Bench, VideoMemBench, Video-MME,
MVBench, LongVideoBench, MLVU, LVBench and CG-Bench) with its statistics, how it was built (pipeline figures
drawn from the paper and the authors' prompts, collapsed by default), its evaluation metrics, and up to three
examples per task type, each with its annotation as released and a short 480p clip where the videos could be
obtained. The companion site is
`https://jxb1st.github.io/training-data-collection/`.

- `index.html`: overview table and the list of datasets. `<dataset>/index.html`: one page per dataset.
- `<dataset>/clips/`: short excerpts re-encoded at 480p H.264 with a mid-clip poster frame.
- `<dataset>/data/samples.json` and `stats.json`: the examples with their annotation fields, and the
  statistics shown on the page, computed from the released annotation files where available.
- `style.css` and `collection.css` are copies of the experiment panel's stylesheets.
- `ivgbench/` has no clips: IVG-Bench is three simulators plus case definitions, so its examples are cases with
  their scheduled events, and its figures show how an episode runs.

Examples are chosen deterministically from the released annotations with a preference for short
questions and short videos. Where videos are not available (YouTube-only or gated archives, licensed
datasets), the example is annotation only and the page says so. Annotation text is verbatim.
