# Movie1 incremental Telegram export — 2026-11-22

This batch adds **21 photo posts**, source IDs **3835–3855**, from the user's `ChatExport_2026-11-22.zip`. It is completely separate from the earlier completed **3,780-post** migration.

## Verified source summary

- Original ZIP SHA-256: `dae307085f6a9ba3a7b52a14575640112811dbf793fea1391107d82bfeb02d52`
- Original `result.json` SHA-256: `160cb4832abb4a12bcd678ee55a4458638c3acdeb5f1eb12c3aa504440082725`
- Source channel ID: `1881963160`
- Target channel: `Bollywood Movie` (`-1004492918137`)
- Full-size photos: **21**; thumbnails: **21**
- Non-channel URLs preserved: **61**
- Telegram promotional URLs removed from new captions: **42**

## Planned repository structure

```
telegram_exports/2026-11-22/
  README.md
  raw/
    result.json
    messages.html
    css/  js/  images/  photos/
  processed/
    posts.jsonl
    manifest.json
  notebooks/
    Telegram_Movie1_Nov22_21_Posts_Kaggle.ipynb
```

**Upload status:** The readme and summary metadata can be committed via the connected GitHub integration. The **binary photo files and original raw export are not yet in this repository path**; do not assume that the folder is a complete backup until the media sync succeeds. The complete structured archive and notebook were prepared separately from the uploaded ZIP.

## Kaggle workflow

1. Upload `ChatExport_2026-11-22.zip` to a Kaggle Dataset and add that Dataset as the notebook's **Input**.
2. Enable Internet, and grant the notebook access to `TELEGRAM_BOT_TOKEN`.
3. Optionally add `GITHUB_TOKEN` as a Kaggle secret, using a fine-grained GitHub token scoped to `kawakaze430/Movie1`, with **Contents: Read and Write**. The notebook can upload extracted files through the Git Data API as one commit. Kaggle-GitHub account linking alone does not imply API credentials.
4. Use **Save Version → Save & Run All**. The uploader validates the destination, sends only 21 photo posts, and writes a checkpoint after each confirmed send.

**Never rerun the uploader without its matching checkpoint after messages might already have been sent.** The notebook does not edit or resend the older 3,780 posts.

Post only media and links you are authorized to distribute; do not include bot tokens in the repository.
