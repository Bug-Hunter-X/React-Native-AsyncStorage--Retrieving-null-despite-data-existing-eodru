# React Native AsyncStorage Data Retrieval Issue

This repository demonstrates a common bug encountered when using AsyncStorage in React Native: retrieving null or undefined values even when data has been stored.  The issue stems from asynchronous operations and the timing of data writing and retrieval.

## Bug Description

The code in `AsyncStorageBug.js` attempts to retrieve data from AsyncStorage immediately after setting it.  Due to the asynchronous nature of AsyncStorage, the retrieval operation may complete before the data is fully written, resulting in null or undefined values being returned.

## Solution

The solution provided in `AsyncStorageBugSolution.js` addresses this by using Promises or async/await to ensure the data is written before attempting retrieval. This approach synchronizes the operations, preventing the premature retrieval of incomplete data.