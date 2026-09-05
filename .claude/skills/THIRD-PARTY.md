# Third-party skills

Skills in this directory that came from elsewhere, and where to get updates.

## creative-writing-skills

Twenty-four skills vendored from
[haowjy/creative-writing-skills](https://github.com/haowjy/creative-writing-skills)
by Jimmy Yao.

| | |
|---|---|
| Upstream version | 0.5.8 |
| Upstream commit | `fd7a3ad9cd7697a0645ff6ff4bd5e809cf7673a3` |
| Vendored on | 2026-09-05 |
| License | Apache-2.0 — see [LICENSE-creative-writing-skills](LICENSE-creative-writing-skills) |

Copied verbatim from the upstream `cw/skills/` directory, unmodified:

```
character-sim          creative-research      creative-writing-craft
creative-writing-modes creative-writing-muse  grill-with-docs
information-hierarchy  intent-modeling        kb-management
knowledge-layers       llm-writing            md-validation
project-setup          qi-layer               reader-sim
reflect                shared-dao             story-memory
story-planning         story-review           structured-artifact
writing-principles     writing-staffing       zoom-out
```

### What did not come across

Upstream ships these skills as a Claude Code plugin whose intended entry
point is the `muse` agent. Vendoring takes the skills only, so the plugin's
11 agents (muse, writer, critic, outliner, brainstormer, editor,
continuity-checker, style-creator, reader-sim, character-sim,
web-researcher), 5 slash commands (`/bs`, `/critique`, `/kb`, `/write`,
plus the README command), and hooks are not here. On claude.ai the author
recommends `creative-writing-muse` as the stand-in entry point when only
skills are available, and that skill is included.

### Updating

These are copies, so upstream updates do not arrive on their own. To refresh:

```bash
git clone --depth 1 https://github.com/haowjy/creative-writing-skills /tmp/cws
cp -r /tmp/cws/cw/skills/* .claude/skills/
```

Then update the version and commit fields above. Take care not to clobber
local edits — `lyric-writer` is ours and is not part of this set.
