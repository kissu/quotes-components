<template>
  <div class="progress">
    <div class="progress-bar progress-bar-striped active"
      aria-valuenow='30' aria-valuemin='0' aria-valuemax='100'
      :style="{width: (quoteCount) * 10 + '%'}">
    </div>
  </div>
</template>

<script>
  export default {
    props: ['quoteCount', 'maxQuotes']
  }
</script>
