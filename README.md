
# Test Push
# Storybook Setup

## Prerequisites
1. Disconnect from Anthem network
2. Initialize empty React Native project (https://facebook.github.io/react-native/docs/getting-started.html)
3. Install Xcode and download required iOS Simulator
4. Install Android Studio Emulator (https://docs.expo.io/versions/latest/workflow/android-studio-emulator/)

## Steps to run project
1. Navigate to the folder where you want to clone the project
2. Run the following command on terminal
```
git clone https://AG*****@bitbucket.anthem.com/scm/amplified2019/storybook.git
```
3. Navigate to project folder
```
cd storybook
```
4. Run yarn install or npm install to get latest packages installed
```
5. Run the following command to start the project
```
expo start
```

# Steps to setup a new Storybook Project
## Storybook

1. Follow the setup guide for Storybook for React Native (https://storybook.js.org/docs/guides/guide-react-native/)

## Creating Components

1. Create React Native UI components under the storybook/stories/{UIcomponent} folder of the project
```
storybook/stories/button/index.ios.js

import React from 'react';
import PropTypes from 'prop-types';
import { TouchableHighlight } from 'react-native';

export default function Button({ onPress, children }) {
  return <TouchableHighlight onPress={onPress}>{children}</TouchableHighlight>;
}

Button.defaultProps = {
  children: null,
  onPress: () => {},
};

Button.propTypes = {
  children: PropTypes.node,
  onPress: PropTypes.func,
};
```
2. Update the index.js file under storybook/stories to add the component to the navigator

```
storybook/stories/index.js 

import Button from './Button';
storiesOf('Button', module)
  .addDecorator(getStory => <CenterView>{getStory()}</CenterView>)
  .add('with text', () => (
    <Button onPress={action('clicked-text')}>
      <Text>Hello Button</Text>
    </Button>
  ));
```
## Running Storybook on Simulator

1. Navigate to the project folder
2. Run the following command on the terminal
```
expo start
```
3. Run the project on iOS or Android simulator based on preference




