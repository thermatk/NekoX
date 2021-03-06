# NekoX

NekoX is an open source third-party Telegram android app.

- Google play store: (https://play.google.com/store/apps/details?id=nekox.messenger)
- Update news : https://t.me/NekoX-Dev
- Feedback: https://t.me/NekoXChat
- Feedback (Persian) : https://t.me/NekogramX_Persian
- Feedback: https://github.com/NekoX-Dev/NekoX/issues
- FAQ: https://telegra.ph/NekoX-FAQ-03-31
- FAQ (Chinese): https://telegra.ph/NekoX-%E5%B8%B8%E8%A6%8B%E5%95%8F%E9%A1%8C-03-31


## Telegram-FOSS Changes:

*Replacement of non-FOSS, untrustworthy or suspicious binaries or source code:*
- Do location sharing with OpenStreetMap(osmdroid) instead of Google Maps
- Use Twemoji emoji set instead of Apple's emoji
- Google Play Services GCM replaced with Telegram's push service
- Has to show a notification on Oreo+, ask Google
- **SECURITY:** Old BoringSSL prebuilts are replaced with the newest upstream source code built at compile time
- **SECURITY:** Old FFmpeg prebuilts are replaced with the newest upstream source code built at compile time
- **SECURITY:** Bundled libWebP is updated

*Removal of non-FOSS, untrustworthy or suspicious binaries or source code and their functionality:*
- Google Vision face detection and barcode scanning (Passport)
- Google Wallet and Android Pay integration
- Google Voice integration
- HockeyApp crash reporting and self-updates
- Google SMS retrieval. You have to type the code manually

*Other:*
- Allow to set a proxy before login
- Added the ability to parse locations from intents containing a `geo:<lat>,<lon>,<zoom>` string
- Force static map previews from Telegram

## Nekogram Changes

- Repeat others' message in one click.
- Save to saved messages in one click.
- Ignore messages from blocked users.
- Forward messages without quoting.
- Create a mention by user's ID.
- Allow non-admin users to view group chat permissions and administrators.
- Select a map preview provider for normal dialogs.
- Promote/restrict user directly from contextual menu clicking on user's message.
- Show user chat history in groups from contextual menu clicking on user's message.
- Delete single downloaded file.
- Customize stickers display size.
- Show and export message details.
- Unlimited favorite stickers.
- Filter chats list: users, groups, channels, bots, admin, unmuted.
- Multi-accounts (up to 8).
- Log in with bot accounts.
- Decide whether to sync contacts on first login.
- Show ID and data center.
- Transparent status bar.
- Change displaying name order.
- Hide mobile number from navigation menu drawer and settings menu.
- Built-in Chinese and Japanese language.
- Use system font and emojis.
- Store cache into app's private directory.
- Hide proxy sponsor channels.
- Toogle to show sensitive media contents in public channels.

## NekoX Changes

- Built-in Vmess, Shadowsocks, SSR proxies support
- Built-in public proxy list
- Proxy subscription support.
- Proxies import and export, remarks, speed measurement, sorting, delete unusable nodes, etc.
- Scan the qrcode (any link, can add a proxy).
- The ( vemss / vmess1 / ss / ssr ) proxy link in the message can be clicked.
- Allow auto disable proxy when VPN is enabled
- Add stickers without sticker pack
- Sticker set list backup / restore / share
- Instant View translation support
- Delete all messages in group
- Dialog sorting is optional "Unread and can be prioritized for reminding" etc.
- Allow to skip "regret within five seconds"
- Unblock all users support
- Google Cloud Translate / Yandex.Translate support
- Custom cache directory (supports external storage)
- Custom AppId and Hash (optional NekoX / Andorid / Android X or Manual input)
- Custom server (official, test DC or Manual input)
- Keep the original file name when downloading files
- View the data center you belong to when you don't have an avatar
- Proxies, groups, channels, sticker packs are able to shared as QRCodes.
- Force English emoji keywords to be loaded
- Add "@Name" when long press @ user option
- Enhanced notification service, optional version without Google Services.
- Built-in Material Design themes / Telegram X style icons

## How to get Google Cloud Translate Key

https://telegra.ph/google-cloud-trans-key-04-26

## Compilation Guide

### Specify APP_ID and APP_HASH

Just fill out TELEGRAM_APP_ID and TELEGRAM_APP_HASH in local.properties

### Build Types

#### Debug

`./gradlew assemble<Variant>Debug`

The default debug key is used, and placing yours is not needed.

#### Release

`./gradlew assemble<Variant>Release`

The difference between release and other build types is that it adds fcm and firebase crash analysis, if you don't like them, use releaseNoGcm.

To compile the release version, please place your keysotre at TMessageProj/release.jks, and fill in KEYSTORE_PASS, ALIAS_NAME, ALIAS_PASS in local.properties, environment variables are also recommended

If you don't use NekoX's APP_ID and APP_HASH, you need to register a physical firebase app and replace google-services.json to ensure fcm works

#### Foss

`./gradlew assemble<Variant>Foss`

OK, a version without firebase cloud messaging and precompiled native libraries, maybe this makes you feel more free, or your phone does not have Google services.

To compile the foss version, please refer to [this script](.github/workflows/foss.yml).

### Build Variants

Available variant list:

`Afat`, ( android 4.1 + )
`MinApi21` ( android 5 + )

## Localization

Join project at https://nekox.crowdin.com/nekox and https://neko.crowdin.com/ .

## Credits

<ul>
    <li>Telegram-FOSS: <a href="https://github.com/Telegram-FOSS-Team/Telegram-FOSS/blob/master/LICENSE">GPLv2</a></li>
    <li>Nekogram: <a href="https://github.com/Nekogram/Nekogram/blob/master/LICENSE">GPLv2</a></li>
    <li>v2rayNG: <a href="https://github.com/2dust/v2rayNG/blob/master/LICENSE">GPLv3</a></li>
    <li>AndroidLibV2rayLite: <a href="https://github.com/2dust/AndroidLibV2rayLite/blob/master/LICENSE">LGPLv3</a></li>
    <li>shadowsocks-libev: <a href="https://github.com/shadowsocks/shadowsocks-libev/blob/master/LICENSE">GPLv3</a></li>
    <li>shadowsocksRb-android: <a href="https://github.com/shadowsocksRb/shadowsocksRb-android/blob/master/LICENSE">GPLv3</a></li>
</ul>