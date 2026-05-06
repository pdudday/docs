# His Love - Remote Promise Catalog

This folder contains the promise catalogs that the app checks for updates.

## How it works

1. The app checks `manifest.json` once per day
2. If a translation's `version` number is higher than what the app has cached, it downloads the new JSON
3. The app uses the downloaded version instead of the bundled one
4. If the download fails or the repo is unreachable, the app uses its bundled data

## To add/update promises

1. Edit the relevant `*_promises.json` file
2. Increment the `version` number in `manifest.json` for that file
3. Update the `count` to reflect the new total
4. Commit and push to `main` branch

## JSON format

Each promise file is a JSON array:
```json
[
  {
    "id": "Category:EnglishReference",
    "verse": "Verse text in the target language",
    "reference": "Localized book name + chapter:verse",
    "category": "Love"
  }
]
```

### Categories (must be exactly one of):
Love, Protection, Provision, Peace, Strength, Salvation, Healing, Guidance, Faithfulness, Hope, Comfort, Forgiveness

### ID format:
`Category:EnglishReference` — e.g., `"Love:John 3:16"`
This ensures favorites persist across languages.

## Translations

| File | Language | Translation | License |
|------|----------|-------------|---------|
| kjv_promises.json | English | King James Version | Public domain |
| rvr_promises.json | Spanish | Reina-Valera 1909 | Public domain |
| almeida_promises.json | Portuguese | Almeida Recebida | Public domain |
| lsg_promises.json | French | Louis Segond 1910 | Public domain |
| luther_promises.json | German | Luther 1912 | Public domain |
| riveduta_promises.json | Italian | Riveduta (Luzzi) | Public domain |
| synodal_promises.json | Russian | Synodal 1876 | Public domain |
| cuv_promises.json | Chinese | Chinese Union Version | Public domain |
| vandyck_promises.json | Arabic | Van Dyck 1865 | Public domain |
