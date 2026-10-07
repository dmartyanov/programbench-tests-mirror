# ProgramBench tests mirror

A mirror of the Hugging Face dataset
[`programbench/ProgramBench-Tests`](https://huggingface.co/datasets/programbench/ProgramBench-Tests)
for environments whose network can reach GitHub release downloads but not Hugging Face's file CDN.

Each release holds one asset per ProgramBench task, `<instance id>.tar`: that task's files at the
dataset commit named in the release tag, laid out as a Hugging Face hub cache
(`hub/datasets--programbench--ProgramBench-Tests/{blobs,snapshots,refs}`). Unpacking an asset into
`$HF_HOME` lets `huggingface_hub.snapshot_download("programbench/ProgramBench-Tests",
repo_type="dataset", allow_patterns="<instance id>/**")` find every file locally. The files are
unmodified; each release lists every asset's SHA-256.

| Release | Dataset commit | Tasks |
|---|---|---|
| `programbench-tests-de0ddfb63759` | `de0ddfb637590c7ecb54fa0b5301f6dc7dfbcee5` | 200 |

## License

MIT, as the source dataset. Each task directory keeps the upstream program's `LICENSE` and
`ATTRIBUTION.md`. ProgramBench: <https://programbench.com>,
<https://github.com/facebookresearch/ProgramBench>.
