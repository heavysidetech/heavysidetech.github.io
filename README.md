# Heavyside

Public company website and WordLens documentation, hosted at https://heavysidetech.github.io.

## Pages

- Home: https://heavysidetech.github.io/
- WordLens privacy policy: https://heavysidetech.github.io/dictionary/privacy/
- WordLens support: https://heavysidetech.github.io/dictionary/support/

The website is plain HTML and CSS in `site/`. There are no build dependencies, scripts, analytics, or external fonts.

## Preview

From this repository, run:

```sh
python3 -m http.server 8000 --directory site
```

Open http://localhost:8000. Check the privacy and support routes directly as well as through navigation.

## Publish

1. In this GitHub repository, open **Settings > Pages** and select **GitHub Actions** as the build and deployment source.
2. Push the site and workflow to `main`, or run **Deploy website to GitHub Pages** manually.
3. Wait for the deployment to succeed and verify all three public URLs above without signing in.

Only `site/` is uploaded. No custom domain is configured. Subsequent changes to the site deploy automatically from `main`.

## WordLens release

Publish and verify the website before shipping the app's updated links. Set the Privacy Policy URL and Support URL in App Store Connect to the URLs above. The iOS source lives in `heavysidetech/dictionary`; its internal project name remains DictionaryLens.

Keep the policy aligned with the app's actual data handling and revise its effective date when the policy changes. The policy was reviewed against the iOS source on November 25, 2026. Support and privacy questions use https://github.com/heavysidetech/dictionary/issues; submissions are public.
