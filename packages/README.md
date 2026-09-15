# Claude V0.1.1 candidate

`lean-execution-0.1.1.zip` is an unreleased candidate for Claude retesting. It contains only the skill entrypoint and its two references, with SKILL.md at the archive root, matching the documented V0.1 packaging layout. The universal core remains authoritative.

Rebuild from the repository root with Python 3:

```sh
python3 - <<'PY'
from pathlib import Path
from zipfile import ZipFile, ZipInfo, ZIP_STORED
root = Path('skills/lean-execution')
with ZipFile('packages/lean-execution-0.1.1.zip', 'w') as archive:
    for name in ('SKILL.md', 'references/anti-patterns.md', 'references/quality-boundary.md'):
        info = ZipInfo(name, date_time=(2026, 9, 15, 0, 0, 0))
        info.compress_type = ZIP_STORED
        info.create_system = 3
        info.external_attr = 0o100644 << 16
        archive.writestr(info, (root / name).read_bytes())
PY
```

ZIP_STORED and fixed metadata make rebuilds byte-identical without depending on a compression library version.

Retest using the documented Claude Web path: Customize → Skills → Add → Upload Skills. Ensure only the candidate version is enabled for Lean runs and disable it for baseline runs. Record the actual model and installation outcome; the previous V0.1 upload does not verify this package. Run `evals/command-regressions.md` and record all results before promoting this candidate to a validated release.
