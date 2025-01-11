# Home Quest

## Overview

Home Quest is a feature-rich mobile application for exploring, filtering, and managing real estate properties. It is built using the Expo framework with React Native and integrates with Appwrite for backend services, providing a seamless experience for users to find their ideal homes.

---

## Features

- **User Authentication**: Google OAuth2 login for secure authentication.
- **Property Listings**: View featured, recommended, and all properties with rich details.
- **Search and Filters**: Powerful search and filtering options to refine results.
- **Dynamic Routing**: View property details using file-based routing.
- **Agent and Review Details**: Comprehensive agent profiles and property reviews.
- **Responsive Design**: Tailwind CSS and NativeWind integration for flexible styling.
- **Global State Management**: Custom context provider for user and app state.

---

## Project Structure

```
Real-Estate-app/
├── README.md
├── app.json
├── babel.config.js
├── image.d.ts
├── metro.config.js
├── nativewind-env.d.ts
├── package.json
├── tailwind.config.js
├── tsconfig.json
├── app/
│   ├── _layout.tsx
│   ├── global.css
│   ├── sign-in.tsx
│   └── (root)/
│       ├── _layout.tsx
│       ├── (tabs)/
│       │   ├── _layout.tsx
│       │   ├── explore.tsx
│       │   ├── index.tsx
│       │   └── profile.tsx
│       └── properties/
│           └── [id].tsx
├── assets/
│   ├── fonts/
│   ├── icons/
│   └── images/
├── components/
├── constants/
├── lib/
└── scripts/
```

---

## Installation

### Prerequisites

- Node.js (>=16.0.0)
- npm or yarn
- Expo CLI

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/Prish20/Real-Estate-app
   cd Real-Estate-app
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables:

   - Create a `.env` file in the root directory and configure the following variables:

     ```env
     EXPO_PUBLIC_APPWRITE_ENDPOINT=YOUR_APPWRITE_ENDPOINT
     EXPO_PUBLIC_APPWRITE_PROJECT_ID=YOUR_PROJECT_ID
     EXPO_PUBLIC_APPWRITE_DATABASE_ID=YOUR_DATABASE_ID
     EXPO_PUBLIC_APPWRITE_PROPERTIES_COLLECTION_ID=YOUR_PROPERTIES_COLLECTION_ID
     EXPO_PUBLIC_APPWRITE_GALLERIES_COLLECTION_ID=YOUR_GALLERIES_COLLECTION_ID
     EXPO_PUBLIC_APPWRITE_REVIEWS_COLLECTION_ID=YOUR_REVIEWS_COLLECTION_ID
     EXPO_PUBLIC_APPWRITE_AGENTS_COLLECTION_ID=YOUR_AGENTS_COLLECTION_ID
     ```

4. Start the app:

   ```bash
   npx expo start
   ```

---

## Scripts

| Command                 | Description                           |
| ----------------------- | ------------------------------------- |
| `npm start`             | Start the Expo development server.    |
| `npm run android`       | Start the app on an Android emulator. |
| `npm run ios`           | Start the app on an iOS simulator.    |
| `npm run web`           | Start the app in a web browser.       |
| `npm run reset-project` | Reset the app to a fresh state.       |
| `npm test`              | Run all unit tests.                   |
| `npm run lint`          | Lint the codebase.                    |

---

## Configuration

### Tailwind CSS

Tailwind is configured in `tailwind.config.js`. The following customizations have been added:

- Fonts: Rubik (Regular, Bold, Light, etc.)
- Colors: Primary, Accent, Black, Danger, etc.

### Appwrite Backend

The Appwrite backend provides services for authentication, data storage, and queries. Configure it in `lib/appwrite.ts`:

```typescript
client.setEndpoint(process.env.EXPO_PUBLIC_APPWRITE_ENDPOINT!)
      .setProject(process.env.EXPO_PUBLIC_APPWRITE_PROJECT_ID!);
```

---

## Key Components

### Components Directory (`/components`)

- **Cards**: Displays property details.
- **Filters**: Provides property filtering options.
- **Search**: Search bar with debounce.
- **Comments**: Shows user reviews on properties.
- **NoResults**: Placeholder for empty search results.

### Lib Directory (`/lib`)

- **`appwrite.ts`**: Configures and manages Appwrite services.
- **`global-provider.tsx`**: Manages global state.
- **`useAppwrite.ts`**: Custom hook for querying Appwrite.
- **`seed.ts`**: Data seeding script for development.

### Constants Directory (`/constants`)

- **Icons**: Centralized icons.
- **Images**: Static image references.
- **Data**: Mock data for development.

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m "Add feature"`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---
