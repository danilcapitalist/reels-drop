# reels-drop

Public drop folder for finished reels on their way to Metricool: `YYYY-MM/<case>-<lang>.mp4`. Metricool copies the video to its own storage, after which the file is removed here.

## Publishing session

Publishing runs in a cloud session that has **only this repository** attached. Such a session reads `.claude/settings.json` from `main`, which allows the Metricool scheduling tools and the git commands for the clean-up, so the post goes out without approval prompts (sessions with two or more repositories ignore this file).

1. The render session (danilfrolovsite) pushes the compressed MP4 here.
2. The publishing session schedules the post in Metricool (brand 6334293, Asia/Bangkok) with a link to the file pinned to the commit hash, then deletes the file and pushes.

The rules for the post itself (networks, trial reels, AI labels, captions) are in `reels/README.md` of danilfrolovsite.
