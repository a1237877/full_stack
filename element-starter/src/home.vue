<template>
  
</template>

<script>
export default {

mounted() {
    // 请求数据
    fetch('localhost:8010/api/user/login').then(data => data.json())
    .then(data => console.log(data))
  },
}

</script>

<style>

</style>
