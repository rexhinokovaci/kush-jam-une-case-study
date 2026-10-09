# How it ships

- **One TypeScript codebase** for iOS and Android with Expo, built with EAS.
- **Separate backend** with its own deploy pipeline, so app releases and content changes never block each other.
- **Credentials outside git.** Store and billing service accounts stay out of the repo.
- **Remote config defaults** in the app, so it keeps working when the backend can't be reached.

## Stack

Expo · React Native · TypeScript · React Navigation · Cloudflare Workers · D1 · RevenueCat · AdMob · EAS
