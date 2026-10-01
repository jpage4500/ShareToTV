# Privacy Policy — Share to TV+

**Last updated: September 29, 2026**

Share to TV+ ("the app") is made by Joe Page. This policy covers the Android version (phones, tablets,
Android TV, Google TV and Fire TV), and the iOS, macOS, Windows and Linux versions.

The short version: **there is no account, no advertising, and no third-party analytics or tracking
SDK.** What you share, your recent list and the TVs the app finds live on your device. To find the
video in a link you share, the app fetches that link, the way a browser would. The video itself goes
from the site to your TV over your own network — never through the developer.

---

## What stays on your device

- **Your settings**, and the **Recent** list: the links you've shared, their titles and thumbnails.
- **The TVs the app has found**: each one's name, model, network address and the apps it has, so the
  list shows straight away next time.
- **On a TV**, the list of what phones have sent it, for its own Recent menu.
- **A log file** of what the app did, including links you shared and the TVs it talked to. It's only
  uploaded in the cases under "Diagnostics" below.
- **Sign-in cookies** for Instagram or Facebook, if you sign in to them (see "Signed-in sites").

These are stored in the platform's normal settings and storage (Android `SharedPreferences` and app
storage, iOS `UserDefaults`, and files under `~/.cast-to-tv/` on desktop). None of it is uploaded
except as described below, and deleting the app removes it.

---

## Links you share

When you share a link to the app, it works out which video on that page to send:

- It fetches the page, and sometimes the players embedded in it, from your device, as a phone browser
  would. The site sees that request and your IP address, the same as if you had opened the link.
- If the page builds its player with JavaScript, the app opens it in a **hidden browser** on your
  device for up to 15 seconds and notes which video the page loads.
- For some sites the app asks the site's public interface for the video instead (below).
- YouTube and streaming-service links (Netflix, Prime Video, Disney+…) aren't scanned: they're handed
  to the matching app on your TV. For a YouTube link, the app asks YouTube for the video's title.

None of this goes to the developer.

---

## Your local network

- **Finding TVs.** The app looks for TVs on your Wi-Fi with the standard discovery protocols (mDNS /
  Bonjour, SSDP / DIAL, Google Cast). iOS asks your permission for this the first time.
- **Sending a video.** The app sends the TV you pick the video's link, its title, and any request
  headers the video needs to play (such as the page it came from, or a site's cookie). This goes
  directly over your local network, not the internet, and not through the developer.
- **Relaying.** A video on your phone, or one a TV can't fetch by itself, is served to the TV by the
  app on your phone. Only the TV it was sent to is given the (random, unguessable) address to fetch it.
- **On a TV**, the app listens on your local network for a phone sending it a video. It opens the
  video in its own player, or in the TV's app for it (YouTube, Netflix…).

---

## Signed-in sites (Instagram, Facebook)

Neither site shows videos to anyone not signed in, so the app lets you sign in to them. This is
optional, and nothing is signed in until you do it.

- You sign in on **the site's own page**, in a browser inside the app. The app doesn't store your
  password.
- The site's sign-in cookies are kept on your device, like a browser's, and sent only to that site,
  to find the video in something you share.
- Signing out (Settings ▸ Signed-In Sites) deletes them. So does uninstalling the app.

---

## Services the app contacts

| Service | What it receives | When |
|---|---|---|
| The site of a link you share, and any player it embeds | The request, your IP address, and the page's own cookies | Each time you share a link or look deeper into one |
| [YouTube](https://policies.google.com/privacy) | A video's ID | A YouTube link you share, to show its title and thumbnail |
| [X](https://x.com/en/privacy) | A post's ID | An X / Twitter link you share |
| [Reddit](https://www.reddit.com/policies/privacy-policy) | A post's ID | A Reddit link you share |
| [TikTok](https://www.tiktok.com/legal/privacy-policy) | The video's page | A TikTok link you share |
| [Instagram](https://privacycenter.instagram.com/policy) / [Facebook](https://www.facebook.com/privacy/policy) | The post, with your sign-in cookies | A link you share, only after you've signed in to that site |
| Your TVs, Chromecasts and streaming sticks | The video's link, title and headers | When you send a video to one |
| [Supabase](https://supabase.com/privacy) (the developer's storage) | See "Diagnostics" | Only as described there |
| [GitHub](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement) | Nothing but the request itself | Update checks — **sideloaded Android and desktop only.** App Store and Play Store builds never do this |

Each service handles what it receives under its own privacy policy. The developer does not receive a
copy of these requests.

---

## Diagnostics

Some things are sent to the developer, to fix problems:

- **After a crash**, the next time the app starts it uploads its log file with the crash's details.
- **When you send feedback** (About ▸ Support / Feedback) or **report a link** that didn't work, the
  app uploads your message, its log file, and for a report, the link and what the app found on it.

---

## What the app never does

- No advertising, ad network, or ad ID.
- No third-party analytics, attribution, or tracking SDK.
- No account with the developer, and no email collection.
- No selling or sharing of data with anyone, for any purpose.
- No location, camera or microphone access.
- No reading of your photos or files, except one you share to the app to send to a TV.

---

## Children

The app isn't directed at children, and it doesn't knowingly collect anything from them. It has no
account system and collects no personal information from anyone.

---

## Your choices, in one place

| To do this | Go here |
|---|---|
| Sign out of Instagram or Facebook | Settings ▸ Signed-In Sites |
| Stop the phone relaying videos to a TV | Settings ▸ Relay Through This Device ▸ Never |
| Stop the app finding TVs (iOS) | Revoke Local Network permission in the iOS Settings app |
| Remove everything stored locally | Uninstall the app (desktop: delete `~/.cast-to-tv/`) |
| Have a support report or crash log deleted | Email the address below |

---

## Contact

Questions, or a deletion request: **joe.page.software@gmail.com**, or send an issue/question through the app
