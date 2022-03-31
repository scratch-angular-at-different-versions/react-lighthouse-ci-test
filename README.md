A create react app that has lighthouse setup

`git clone https://github.com/scratch-angular-at-different-versions/react-lighthouse-ci-test.git`

```bash
npm install
npm run build


npm install -g @lhci/cli@latest 
lhci autorun
```

fallback installation: `install -g @lhci/cli@0.3.x`

```json
{
  "ci": {
    "assert": {
      "preset": "lighthouse:recommended",
      "assertions": {
        "categories.pwa": "off",
        "bypass": ["error", {"minScore": 0}],
        "offline-start-url": ["error", {"minScore": 0}],
        "service-worker": ["error", {"minScore": 0}],
        "works-offline": ["error", {"minScore": 0}],
        "redirects-http": ["warn", {"minScore": 0}],
        "render-blocking-resources": ["warn", {"maxLength": 1}],
        "uses-http2": ["warn", {"minScore": 0}]
      }
    }
  }
}
```
