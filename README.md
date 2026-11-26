# Heavyside

Public company website and WordLens documentation, hosted at https://heavysidetech.github.io.

## Pages

- Home: https://heavysidetech.github.io/
- WordLens privacy policy: https://heavysidetech.github.io/dictionary/privacy/
- WordLens support: https://heavysidetech.github.io/dictionary/support/

The website is plain HTML and CSS at the repository root. There are no build dependencies, scripts, analytics, or external fonts.

## Preview

From this repository, run:

```sh
python3 -m http.server 8000
```

Open http://localhost:8000. Check the privacy and support routes directly as well as through navigation.

## Publish

1. The repository uses **Settings > Pages > Deploy from a branch**, with `main` and `/ (root)` selected.
2. Push changes to `main`; GitHub runs its built-in Pages deployment automatically.
3. Wait for the deployment to succeed and verify all three public URLs above without signing in.

The root `.nojekyll` file tells GitHub to serve the static files without Jekyll processing. No custom domain or custom Actions workflow is needed. Keep private files and secrets out of this public repository.

## WordLens release

Publish and verify the website before shipping the app's updated links. Set the Privacy Policy URL and Support URL in App Store Connect to the URLs above. The iOS source lives in `heavysidetech/dictionary`; its internal project name remains DictionaryLens.

Keep the policy aligned with the app's actual data handling and revise its effective date when the policy changes. The policy was reviewed against the iOS source on November 25, 2026. Support and privacy questions use https://github.com/heavysidetech/heavysidetech.github.io/issues; submissions are public.
