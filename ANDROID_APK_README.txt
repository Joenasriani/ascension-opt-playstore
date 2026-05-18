ASCENSION - Android APK WebView Ready Package

What was changed:
1. Removed Tailwind CDN from index.html.
2. Replaced Google Fonts remote loading with local Montserrat font files.
3. Removed the AI Studio CDN import map from index.html. The built game bundle already contains the runtime code, so the import map was not needed for this packaged build.
4. Kept gameplay, structure, UI, audio, and music files unchanged.
5. Included Play Store visual assets in /playstore-assets.

Image handling rule followed:
- No cropping.
- No stretching.
- Existing provided Play Store images were preserved as uploaded.

Android WebView recommendations:
- Enable JavaScript.
- Enable DOM storage.
- Allow audio after user interaction.
- Lock orientation according to final game choice, likely portrait if using the mobile portrait build.
- Package the /www or root web folder inside Android assets.

Remaining note:
- The minified JS bundle still contains non-runtime documentation/error URLs from included libraries, such as react.dev error-help links. Those are not AI Studio dependencies and were not edited because changing minified vendor code could risk game behavior.
