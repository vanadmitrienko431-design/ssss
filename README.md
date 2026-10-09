# Shina Tracker → APK

Вариант 1 (без установки Android Studio): GitHub Actions
1. Создай пустой репозиторий на GitHub, залей туда все файлы этой папки.
2. Вкладка Actions → "Build APK" → Run workflow.
3. Через 3–5 минут скачай артефакт Shina-Tracker-apk (app-debug.apk).

Вариант 2 (локально, нужны Node 20, JDK 17, Android SDK):
  npm install
  npx cap add android
  npx cap sync android
  cd android && ./gradlew assembleDebug
  APK: android/app/build/outputs/apk/debug/app-debug.apk

Напоминания: плагин @capacitor/local-notifications уже в package.json. В APK в разделе настроек появится блок «Напоминание».
