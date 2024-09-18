# React Native Calling Screen with Redux

This is a modular and reusable calling screen interface designed in React Native. The project includes chat message functionality, mute/unmute button, call-end action, and uses Redux for state management. The design follows a clean architecture with a centralized color scheme and common styles for consistent UI across components.

## Features

- **Chat Integration**: Display chat messages between users with avatars.
- **Redux State Management**: Manages chat messages and call state.
- **Mute/Unmute**: Toggle mute functionality with state management.
- **Reusability**: Reusable button and action components.
- **Centralized Styles**: Consistent UI using centralized styles and colors.
- **Expandable**: Can be extended to include more screens like Call Log, Profile, etc.

## Project Structure

```bash
.
├── assets
│   └── icons           # Icons for buttons (mute, end call, etc.)
├── src
│   ├── components
│   │   ├── MuteButton.js          # Mute button component
│   │   ├── ChatBubble.js          # Chat bubble component
│   │   ├── EndCallButton.js       # End Call button 
│   │   └── index.js               # Index file for components
│   ├── redux
│   │   ├── actions.js             # Redux action creators
│   │   ├── chatReducer.js         # Reducer to manage chat messages
│   │   ├── store.js               # Store configuration for Redux
│   ├── screens
│   │   ├── CallScreen.js          # Main screen for calling interface
│   │   └── index.js               # Index file for components
│   ├── styles
│   │   ├── colors.js              # Centralized color scheme
│   │   ├── fonts.js               # Centralized fonts
│   │   ├── commonStyles.js        # Common styles for reuse
│   │   └── index.js               # Index file for components
│   ├── utils
│   │   └── format.js              # Utility functions (if required)
│   └── App.js                     # Main app entry point
├── .gitignore
├── package.json                   # Project dependencies and scripts
└── README.md                      # Project documentation
```

## Installation

### Prerequisites

Make sure you have the following installed on your system:

- **Node.js** (v14.x or above)
- **npm** (v6.x or above)
- **React Native CLI** (for running the app on iOS/Android)
- **Xcode** (for iOS development)
- **Android Studio** (for Android development)

### Steps to Set Up the Project

1. **Clone the repository**:
   ```bash
   git clone git@github.com:shoaibamin-dev/ReactNativePhoneUI.git

Navigate to the project directory:

```bash
cd ReactNativePhoneUI
Install the dependencies:
```


```bash
npm install 
```
Link necessary dependencies for iOS (React Native <= 0.60):

```bash
npx react-native link react-native-vector-icons
```

Link necessary dependencies for iOS (React Native > 0.60):

```bash
npx react-native-asset            
```
Run the project on your target platform:

For iOS:

```bash
npx pod-install && npm run ios
```
For Android:

```bash
npm run android
```
Fonts Installation
To use custom fonts, follow these steps:

Place your font files (e.g., .ttf or .otf) in the assets/fonts directory.

In your react-native.config.js, ensure that you have the fonts set up:

javascript
Copy code
module.exports = {
  assets: ['./assets/fonts'],
};
Run the linking command again to link the fonts:

```bash
npx react-native link
```
Use the font in your styles. For example:

javascript
```bash
const styles = StyleSheet.create({
  text: {
    fontFamily: 'YourCustomFontName',
  },
});
```

### Key Highlights in Markdown:

1. **Code blocks** are properly formatted using triple backticks (\`\`\`bash\`\`\` or \`\`\`javascript\`\`\`).
2. **Steps** are clearly numbered for easy follow-through.
3. Each section (prerequisites, steps, and fonts) is broken into **clear subsections** for clarity.
