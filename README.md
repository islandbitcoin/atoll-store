# Island Bitcoin — Umbrel community app store

A single Umbrel community app store (`id: atoll`) hosting all of Island Bitcoin's apps.

## Add this store to your Umbrel

1. Open your Umbrel → **App Store** → **⋯** → **Add community store**
2. Paste this repo's URL:
   ```
   https://github.com/islandbitcoin/atoll-store
   ```
3. Install any app below from the Island Bitcoin store.

## Apps

| App | id | What it does |
|-----|----|--------------|
| **Pact** | `atoll-pactd` | Sovereign agent relationship bonds over Nostr & Lightning |
| **Kathreftestr** | `atoll-kathreftestr` | Mirror a livestream to Nostr (NIP-53), with Lightning zaps |

## Layout

Each app lives in a folder named `atoll-<app>` (the Umbrel rule: every folder must be
prefixed with the store `id`). Inside each:

```
atoll-<app>/
├── umbrel-app.yml       # id must equal the folder name (atoll-<app>)
├── docker-compose.yml   # APP_HOST is <id>_web_1
└── icon.svg
```

## Adding a new app

1. Create `atoll-<app>/` with `umbrel-app.yml` (`id: atoll-<app>`), `docker-compose.yml`
   (`APP_HOST: atoll-<app>_web_1`), and `icon.svg`.
2. Point the icon URL at `…/atoll-store/main/atoll-<app>/icon.svg`.

This store is also tracked by the [`atoll`](https://github.com/islandbitcoin/atoll) parent repo
alongside the Start9 packages and registry.
