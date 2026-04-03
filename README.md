# idit-viewer

A local web dashboard for browsing your [Personal Idit](https://github.com/idit-life/personal-idit) chain.

## What it does

- Timeline view of all chain entries
- Filter by signer, entry type, or search text
- Expand entries to see full content, hashes, and signatures
- One-click chain verification (checks every hash link)
- Auto-refreshes every 30 seconds
- Works with any Idit server

## Usage

### Option 1: Open directly

Start your Idit server, then open `index.html` in a browser:

```bash
idit serve
# then open index.html in your browser
```

### Option 2: URL parameter

```
index.html?server=http://192.168.1.100:18793
```

### Option 3: Serve alongside Idit

Drop `index.html` somewhere your web server can reach it. The viewer connects to any Idit API endpoint — just enter the URL in the top bar.

## API endpoints used

- `GET /health` — connection check
- `GET /chain/stats` — entry counts, signers, types
- `GET /chain?limit=N&offset=0` — entry list
- `GET /chain/verify` — full chain hash verification

## Requirements

A running [Personal Idit](https://github.com/idit-life/personal-idit) server. That's it. No build step, no dependencies, no node_modules.

## License

MIT
