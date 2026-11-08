# Optimized Kanboard build

This folder contains the optimization patch produced for the official Kanboard source.

The complete upstream source remains available at:
https://github.com/kanboard/kanboard

## Apply

```bash
git clone https://github.com/kanboard/kanboard.git kanboard
cd kanboard
git checkout -b optimized-beta
git apply ../kanboard/patches/performance-stability.patch
```

The patch changes only:

- `assets/js/src/BoardPolling.js`: prevents duplicate polling timers and overlapping refresh requests;
- `assets/js/src/App.js`: prevents duplicate loading indicators.

The Qwen Tasks beta plugin is available in `plugins/QwenTasks` at the repository root.
