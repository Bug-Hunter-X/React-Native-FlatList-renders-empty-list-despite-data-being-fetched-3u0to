# React Native FlatList Empty List Bug

This repository demonstrates a common bug in React Native where a FlatList component renders an empty list even after data has been fetched asynchronously. The problem arises from a race condition between data fetching and the component's rendering.

## Bug Description

The `MyComponent` fetches data using an asynchronous function.  If the data fetching takes longer than the initial render, the FlatList renders with an empty array, causing the empty list to appear. 

## Solution

The solution involves using a loading state and checking for null values before rendering the FlatList.