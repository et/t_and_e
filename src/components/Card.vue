<template>
<div class="card">
  <div class="card-content">
    <div class="media-content">
      <p class="title is-4">
        <a :href="url">{{ title }}</a>
      </p>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'card',
  props: {
    title: String,
    url: String
  }
}
</script>
