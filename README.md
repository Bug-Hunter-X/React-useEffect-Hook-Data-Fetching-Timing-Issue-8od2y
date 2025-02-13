# React useEffect Hook Data Fetching Timing Issue

This repository demonstrates a common issue encountered when using the `useEffect` hook in React for data fetching. The component fetches data from an API but the loading state is displayed too briefly, even if the API request takes longer.

## Bug Description

The `MyComponent` uses `useEffect` to fetch data. The loading message is rendered while fetching, but the UI jumps directly to displaying the data fetched, even if the data fetch takes longer. This is not ideal, as it gives the impression of immediate data availability when there might be some delay.

## Solution

The solution involves checking if the data is still being fetched. Only after we are certain data has arrived, then we render it.