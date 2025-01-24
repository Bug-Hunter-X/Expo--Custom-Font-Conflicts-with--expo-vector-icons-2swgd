# Expo: Custom Font Conflicts with @expo/vector-icons

This repository demonstrates a bug related to using custom fonts alongside the `@expo/vector-icons` package in Expo projects.  The issue involves missing or incorrectly displayed icons when custom fonts are loaded.

## Problem
The problem arises from a potential conflict between how Expo handles font loading and the internal mechanisms of `@expo/vector-icons`.  Specifically, the `Ionicons` icon set might not render correctly when a custom font is loaded, resulting in missing or improperly displayed icons.

## Solution
The solution involves carefully managing the order and method of font loading to ensure compatibility with `@expo/vector-icons`. The primary fix is to ensure your custom font is properly loaded before attempting to render icons that rely on `Ionicons` assets. This might involve adjusting your `App.js` or other relevant component to handle font loading in a specific sequence.  Alternatively, you may need to explore methods of font preloading or other strategies to ensure the proper initialization of all fonts before they are used in your application. 