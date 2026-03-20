# Training-app

## Step 1 — Bootstrap the Mobile App Shell (Expo Router + TypeScript)

This repository currently contains a static prototype (`index.html`).
The next step to get the app running is to create the production mobile shell using Expo Router and TypeScript.

### Prerequisites
- Node.js 20+
- npm 10+
- Expo CLI (`npx`-based usage is fine)

### Commands
```bash
# from repo root
npx create-expo-app@latest mobile --template tabs@latest --yes
cd mobile
npx expo install expo-router react-native-safe-area-context react-native-screens expo-linking expo-constants expo-status-bar
```

### Router setup
1. Ensure `app/` exists (Expo Router file-based routes).
2. Keep the first runnable route minimal:
   - `app/_layout.tsx`
   - `app/index.tsx`
3. Start with:
```bash
npm run start
```

### Definition of done for this step
- App boots in Expo Go or simulator.
- `app/index.tsx` renders a simple “Training App” home screen.
- No business logic yet (pure shell only).

### Why this is the next step
Creating the mobile shell first gives a stable runtime target for every future module (auth, program ingestion, validation gate, and training UI).
