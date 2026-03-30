# Paperclip for Umbrel

Community Umbrel app store packaging for [Paperclip](https://paperclipai.net) — the open-source AI agent orchestration platform.

## Install via Community App Store

1. In your Umbrel dashboard, go to **App Store → Community App Stores**
2. Add this repo URL (your GitHub URL after pushing this)
3. Search for **Paperclip** and install

## File Structure

```
umbrel-paperclip/
├── umbrel-app-store.yml     # App store manifest
└── paperclip/
    ├── umbrel-app.yml       # App metadata
    ├── docker-compose.yml   # Docker setup
    └── exports.sh           # Exported env vars
```

## Notes

- Data is persisted at `APP_DATA_DIR/data` (managed by Umbrel)
- Paperclip runs on port **3100**
- First run installs the npm package — takes ~1 min to start
- After install, open the app and run the onboarding wizard

## Migrating existing data

If you already have a Paperclip instance running, copy your data directory into
Umbrel's app data path before starting:

```bash
cp -r /data/.paperclip/instances/default/* ~/umbrel/app-data/paperclip/data/
```
