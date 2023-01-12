<script setup>
  const title = ref('My Project: best')

  </script>

<template>
    <div>
        thi is my best project.
    </div>

    <div>
      <Head>
        <Title>{{ title }}</Title>
        <Meta name="this the page for my best project" :content="title" />
      </Head>
      <h1>{{ title }}</h1>
    </div>
</template>