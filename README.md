# Expo DocumentPicker Android Null Uri Bug

This repository demonstrates a bug in the Expo DocumentPicker API on Android where the promise resolves with a null `uri` after file selection.  The issue is intermittent, but can cause significant problems for applications that rely on accessing the selected file's data.

## Steps to Reproduce

1. Run the provided `bug.js` example on an Android device.
2. Select a file using the DocumentPicker.
3. Observe that the `uri` is sometimes `null` even when the picker completes successfully.

## Workaround

A potential workaround (implemented in `bugSolution.js`) is to add error handling and retry the file selection process in case of a null `uri`.  This is not an ideal solution, but it mitigates the problem.

## Solution

The ideal solution would be a fix within the Expo DocumentPicker API itself to prevent the `null` `uri` from being returned.  This issue should be reported to the Expo community.