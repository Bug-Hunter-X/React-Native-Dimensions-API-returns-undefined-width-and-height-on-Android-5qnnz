# React Native Dimensions API Undefined Width/Height on Android

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native on Android. The problem arises when accessing screen dimensions before the layout is fully measured, leading to undefined or inaccurate `width` and `height` values.

## Problem

The `Dimensions.get('window')` method might return an object with undefined `width` and `height` properties if called too early in the component's lifecycle, particularly during the initial render.

## Solution

The solution involves using the `Layout` component or `onLayout` prop to ensure that the dimensions are accessed after the layout has been determined.  This guarantees accurate measurements.

## Usage

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` or `yarn install`.
4. Run `npx react-native run-android` to run the project on an Android emulator or device.