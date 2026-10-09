# Kush Jam Unë?: case study

**The Albanian party guessing game** in the style of Heads Up: hold the phone to your forehead and your friends act out the card.

[Website](https://kushjamune.pages.dev) · Platforms: iOS · Android · backend on Cloudflare Workers

> Source code is private. This repo documents what was built and how. Ask for a live walkthrough of the real codebase.

## What I built

- **4,000+ cards** across Albanian categories: celebrities, TV, TikTok, the national team and more.
- **Content updates without app releases.** Categories, cards, packs and game settings all come from the backend.
- **Monetization.** Subscriptions and premium packs through RevenueCat, plus AdMob banner, interstitial and rewarded ads, with frequency set by the backend.
- **Admin panel** for managing categories and cards without touching code.
- **Party-ready design.** Dark mode, large type you can read from across the room, haptics, and a round summary.

## Results

- New categories go live the same day, with no store review.
- Ad frequency and pricing can be tuned remotely without shipping a new build.

## Lessons learned

- **When content is the product, keep it out of the binary.** Serving categories, cards, packs and settings from the backend means the game can change daily without app releases.
- **Decouple app and content pipelines.** A separate backend deploy pipeline means app releases and content changes never block each other.
- **Plan for the backend being unreachable.** Remote config ships with in-app defaults, so the game keeps working when the backend can't be reached.
- **Don't build billing you can buy.** RevenueCat gives one entitlement system across iOS and Android, with no receipt validation to maintain.

## FAQ

### How do new cards and categories reach players without an app update?

The app loads categories, cards, packs and game settings from a Cloudflare Workers API backed by D1. Content is managed in an admin panel, so new categories go live the same day.

### How is the game monetized?

Subscriptions and premium packs through RevenueCat, plus AdMob banner, interstitial and rewarded ads. Ad frequency is set by the backend, so revenue and retention can be balanced without shipping a build.

### Why Expo and React Native?

One TypeScript codebase covers iOS and Android, built with EAS, which keeps a content-driven game fast to iterate on.

### What happens if the backend is down?

The app ships with remote-config defaults, so it keeps working when the backend can't be reached.

### Can you build a content-driven mobile game or app for my business?

Yes. I'm a mobile app developer and DevOps engineer based in Tirana, Albania, building iOS and Android apps with subscriptions, ads and live content for clients across the Balkans and Europe. [Email me about your project](mailto:kovacirexhino@gmail.com?subject=Project%20inquiry).

## Read more

- [Architecture and key decisions](docs/architecture.md)
- [Delivery pipeline and stack](docs/engineering.md)

## Related case studies

- [Nearby Lens](https://github.com/rexhinokovaci/nearby-lens-case-study): smart-glasses detection over Bluetooth LE on iOS, watchOS, Android and Wear OS
- [Word game engine](https://github.com/rexhinokovaci/word-game-engine-case-study): one real-time multiplayer engine shipped as 7 localized games
- [Balkans Quiz](https://github.com/rexhinokovaci/balkans-quiz-case-study): per-country trivia apps with Apple Watch, widgets and an automated question pipeline

## About the author

**Rexhino Kovaci** is a DevOps engineer, mobile app developer and AI engineer based in Tirana, Albania, and the founder of [Modex Apps](https://modex.al). He has 5+ years in DevOps, including work as a DevOps Engineer at Lufthansa Industry Solutions on Volkswagen AG projects, and holds Microsoft DevOps Engineer Expert, Azure Administrator Associate, Azure Developer Associate, HashiCorp Terraform Associate and New Relic Full-Stack Observability certifications. He builds for clients across the Balkans and Europe.

---

**Want something like this built for your business?** I build mobile apps, web apps and AI products end to end. [Email me about your project](mailto:kovacirexhino@gmail.com?subject=Project%20inquiry) · [Full profile](https://github.com/rexhinokovaci)

<sub>This case study is licensed under [CC BY 4.0](LICENSE). Product names and trademarks belong to their owners.</sub>
