BlockStreak v2 - native Android app (WebView + Usage Access bridge)

Everything needed to build is here. Build with GitHub Actions (.github/workflows/build.yml).
APK appears under Actions > latest run > Artifacts > BlockStreak-APK.
debug.keystore is committed on purpose so updates install over the old app and keep your streak. Do not delete it.

Bundled game assets (sfx/*.ogg sounds, tex/*_ore.png textures) come from Mojang's Minecraft and belong to Mojang.
They are for your personal build only. Keep this GitHub repository PRIVATE and do not share the APK publicly.

v2.1: auto screenshots. ShotService (Accessibility Service) saves a screenshot every few minutes while Minecraft is open
into the app's private storage (files/autoshots). They show in Gallery > Auto-captured and can be downloaded one by one
to Downloads/BlockStreak/Auto. Needs Android 11+ and Accessibility access turned on in Profile.

v2.2: day info. After each auto screenshot, on-device text recognition (ML Kit, bundled, offline) looks for the words
Day, XP/Level, Biome and Position/Coords and stores the number or name next to them. Shown on each shot and in Stats > World log.
Add more words in app/src/main/java/com/codexter/blockstreak/DayInfo.kt.
