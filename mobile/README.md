# Life RPG — iOS wrapper (Capacitor)

Wraps the app's `index.html` (one level up) into a native iOS project. No build step for the web app itself — this just packages the existing file.

## Before opening Xcode (or after editing ../index.html)
`www/` is gitignored on purpose — it's just a copy of `../index.html`, kept out of git so there's only one real source of truth. Regenerate it and sync into the native project with:

```bash
cp ../index.html www/index.html
npx cap sync ios
```

## Then open in Xcode
```bash
npx cap open ios
```
Requires full Xcode installed (not just Command Line Tools) — Command Line Tools alone can't build/sign the app.
