<template>
  <div>
    <ul>
        <li v-for="article in data" :key="article.title">
            <NuxtLink :to="article._path">{{  article.title  }}</NuxtLink>
        </li>
    </ul>
  </div>
</template>

<script setup>
    const { data } = await useAsyncData('blog-list', () => queryContent('/blog').find())
</script>

<style>
    ul {
        display: flex;
        flex-direction: column;
        list-style: none;
    }

    li {
        background: #bbbbbb;
        
    }
</style>

