<script lang="ts" setup>
async function getData() {
  const response = await fetch("https://xkcd.com/614/info.0.json", {
    mode: "no-cors",
  });
  const data = response.json();
  console.log(data);
}
onMounted(async () => {
  await getData();
});
</script>

<template>
  <div class="content">
    <img src="../assets/images/content.png" alt="" />
  </div>
</template>


<style lang="scss" scoped>
.content {
  display: flex;
  justify-content: center;
}

@media (max-width: 767px) {
  .content img {
    width: 90vw;
    height: 300px;
  }
}
</style>