# slohmaier.github.io

Universal Links configuration for Meta Wearables apps.

## Configured Apps

- **SprintGuide** (com.slohmaier.SprintGuide) - Lane guidance for track runners
- **SightBridge** (com.slohmaier.SightBridge) - Meta Wearables app

## Usage

1. This site provides the `.well-known/apple-app-site-association` file for Apple Universal Links
2. All visitors are automatically redirected to [slohmaier.com](https://slohmaier.com)
3. Each Meta Wearables app uses `slohmaier.github.io` as its Universal Link domain

## Setup

**Important:** Replace `TEAMID` in `.well-known/apple-app-site-association` with your actual Apple Developer Team ID.

## Adding a New App

Edit `.well-known/apple-app-site-association` and add a new entry:

```json
{
  "appID": "TEAMID.com.slohmaier.YourAppBundleID",
  "paths": ["*"]
}
```

Then commit and push:

```bash
git add .well-known/apple-app-site-association
git commit -m "Add new app to Universal Links"
git push
```
