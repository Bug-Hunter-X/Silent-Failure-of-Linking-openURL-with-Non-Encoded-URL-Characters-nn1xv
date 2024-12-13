# Silent Failure of Expo Linking.openURL

This repository demonstrates a bug in Expo's `Linking.openURL` API where the function fails silently when provided with a URL containing certain special characters that are not properly URL-encoded.  The issue is that there's no clear error message or indication of failure, making debugging challenging. 

## Steps to Reproduce

1. Clone this repository.
2. Run the `bug.js` example.
3. Observe that the URL with improperly encoded characters fails to open, with no error reported.
4. Compare to the `bugSolution.js` example, which demonstrates how to correctly handle URL encoding to prevent the issue. 

## Solution

Always URL-encode the URL string before passing it to `Linking.openURL`. The `bugSolution.js` file provides a corrected example. 

This issue highlights the importance of robust error handling and proper URL encoding when working with external links in React Native applications built with Expo.