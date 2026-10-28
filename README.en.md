# Image Motion and Dreamina Video Assistant / 广告图动效与即梦视频助手

[简体中文](README.md) | **English**

Analyze product/ad images while preserving text, logos and shape; preview prompts and commands before authorized video generation.

[Download complete project ZIP](https://github.com/hezonglinhzl-creator/varla-electric-mobility-skills-and-tools/raw/main/packages/skill-image2-motion-agent.zip) · [All projects](https://github.com/hezonglinhzl-creator/varla-electric-mobility-skills-and-tools)

## Features

- English prompts with Chinese review
- Logo sweeps, text entrances and product motion
- A non-credit-consuming dry run

## What is included

| Part | Location |
| --- | --- |
| Dreamina Image-to-Video Command Wrapper | [dreamina-image2video](apps/dreamina-image2video/README.en.md) |
| Skill instructions | [SKILL.md](skill/image2-motion-agent/SKILL.md) |

## Download and extract

1. Open this repository, choose **Code → Download ZIP**, or use the complete-project download above.
2. Right-click the downloaded ZIP and choose **Extract All**. Open the extracted folder containing this README.
3. Keep the whole folder together. Start the program first using the next section, then install/use its skill.

Installation also writes PACKAGE-LOCATION.json beside the installed SKILL.md, mapping the bundled programs to their actual extracted directories. Keep the full extracted folder; rerun the installer after moving it. Existing Skill content is preserved by default while paths are refreshed.

## 1. Set up the program first

### Dreamina Image-to-Video Command Wrapper (`dreamina-image2video`)

Python and your own Dreamina CLI/login; command previews do not require generation.

Open `apps/dreamina-image2video` first. Build CLI commands from JSON jobs, default to dry-run and execute only with --execute.

1. Install image2-motion-agent. The wrapper is `image2-motion-agent-program-package/image2-motion-agent/scripts/dreamina_image2video.py`.
2. Create your job.json with image, prompt, duration, poll and video_resolution.
3. First run `python image2-motion-agent-program-package/image2-motion-agent/scripts/dreamina_image2video.py --job C:/path/job.json`.
4. Check `will_consume_credits: false` and review the prompts.
5. Before real generation, inspect `dreamina -h` for your installed version and log in. Add `--execute` only after explicit approval of the same job.

[Full program / browser-extension guide](apps/dreamina-image2video/README.en.md)

You manage the third-party CLI version and credits; no account or free credits are provided.

## 2. Install the Skill

1. At the extracted project's root, double-click `安装Skill.cmd` on Windows.
2. The installer copies `skill/image2-motion-agent` to `%USERPROFILE%\.codex\skills\image2-motion-agent`. Existing same-name skills are skipped; check the displayed result.
3. Reopen Codex and start a new chat. Use the exact skill name shown below.
4. If scripts cannot run under your organization policy, open install.ps1 for review or copy the skill directory manually to the same destination.

## 3. First task

| Prepare | Details |
| --- | --- |
| Input | One image, requested motion, duration and aspect ratio. |
| Output | Image analysis, bilingual prompts, a JSON job file and generation command. |

```text
Use image2-motion-agent to add a text entrance and logo sweep while preserving all text and the bike shape. Show prompts and a dry run first.
```


## Limits and troubleshooting

A dry run does not render video. Execution needs your Dreamina CLI, login and credits plus explicit --execute.

| Problem | Next step |
| --- | --- |
| Skill not visible | Check the installer output and destination SKILL.md, reopen Codex and start a new chat. |
| Program fails to start | Open its directory in PowerShell and run the documented command so the error remains visible; check that program's README. |
| Browser panel missing | Select the exact folder containing manifest.json, check supported websites and refresh the website tab. |
| External service unavailable | Supply your own authorization/settings and verify access. Keep local output rather than claiming a sync/send succeeded. |

## Privacy and status

This is a source/skill distribution. No real accounts, OAuth tokens, customer/KOL lists, contracts, orders, mailbox exports or business media are included. You configure your own services. Documentation and package paths were checked; live orders, sends and publications were not executed as part of documentation validation.
