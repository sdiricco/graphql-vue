<template>
  <h1>Welcome to vue / graphql example</h1>
  <div>
    {{ result }}
  </div>
</template>

<script setup lang="ts">
import { useQuery } from '@vue/apollo-composable';
import gql from 'graphql-tag';

const QUERY = gql`
  query {
    hello
  }
`
const { result } = useQuery(QUERY);
</script>

<style scoped>
</style>
