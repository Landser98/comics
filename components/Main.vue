<template>
  <div class="main">
    <h3 class="main__title">Bad Map Projection: Liquid Resize</h3>
    <Pagination />
    <Content />
    <Pagination />
  </div>
</template>


<style lang="scss" scoped>
.main {
  display: flex;
  flex-direction: column;
  padding: 0 15px;
  align-items: center;
  background: #0e2f51;
  padding-top: 83px;
  &__title {
    font-style: normal;
    font-weight: 500;
    font-size: 22px;
    line-height: 26px;
    text-align: center;
    color: #ffffff;
  }
}
</style>