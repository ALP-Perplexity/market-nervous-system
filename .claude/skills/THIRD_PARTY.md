# Third-party skills
Vendored verbatim (no local edits) on 2026-10-30 for Obsidian-compatible vault projection work (ADR-0003, PROPOSED).

| Skill | Source | Revision | License |
|---|---|---|---|
| obsidian-markdown, obsidian-bases, json-canvas, obsidian-cli | https://github.com/kepano/obsidian-skills | 3ccff5338ea700537839b21900aa5358a0402c98 | MIT (below) |

Not vendored from that repo: defuddle, knap (each needs a global npm CLI; new dependency approval required).
obsidian-cli needs a running Obsidian desktop app; it is for human/local sessions, not CI or cloud agents.
Review and rejected alternatives: docs/kb/13-obsidian-agent-memory-review.md.
To update: re-copy from a newer upstream revision, record the SHA here, and review the diff as external text.

## License
MIT License

Copyright (c) 2026 Steph Ango (@kepano)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
