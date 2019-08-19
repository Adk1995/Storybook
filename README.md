# Storybook Setup
## Prerequisites

1. Disconnect from Anthem network
2. Initialize empty React Native project (https://facebook.github.io/react-native/docs/getting-started.html)
3. Install Xcode and download required iOS Simulator
4. Install Android Studio Emulator (https://docs.expo.io/versions/latest/workflow/android-studio-emulator/)

## Storybook Setup

1. Follow the setup guide for Storybook for React Native (https://storybook.js.org/docs/guides/guide-react-native/)

## Creating Components

1. Create React Native UI components under the storybook/stories/{UIcomponent} folder of the project
2. Update the index.js file under storybook/stories to add the component to the navigator

```
import Datepicker from './Datepicker';
storiesOf('Datepicker', module).add('DatesIOS', () => <Datepicker showApp = {linkTo('Button')} />);

```




