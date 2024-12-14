# React Native FlatList Rendering Issue

This repository demonstrates a common issue in React Native where a FlatList component fails to render data after a successful API fetch.  The application fetches data correctly, but the FlatList remains empty despite the loading state resolving properly. The problem does not involve errors in fetching.  The provided solution addresses this issue.

## Problem Description
The `DataFetch` component fetches data from a public API (`https://jsonplaceholder.typicode.com/todos`). While the loading state indicates successful data retrieval, the FlatList remains blank.  No error is displayed. 

## Solution
The issue is likely caused by the `keyExtractor` not returning a unique key.  The `keyExtractor` must return a unique string for each item in the data array. If keys are not unique then the Flatlist may not render correctly. The solution provides a correct implementation of `keyExtractor` function.