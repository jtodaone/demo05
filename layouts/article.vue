<template>
    <main>
      <h1> Articles </h1>
      <article>
        <slot />
      </article>
    </main>
  </template>

  <script>
  export default {
  
  }
  </script>
  
  <style>
    main {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
    }

    h1 {
        font-family: 'Heletica';
    }

    article {
        width: 800px;
    }
  </style>