<template>
<VAlert
      variant="tonal"
      :color="data.color"
    >
      {{ data.message }}
    </VAlert>
</template>

<script>
export default {
    props:['data']
}
</script>