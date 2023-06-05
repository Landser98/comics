<template>
  <div class="pagination">
    <ul class="pagination__list">
      <li class="pagination__list-item pagination__list-item-blue">
        <i class="fa-solid fa-backward-step"></i>
      </li>
      <li class="pagination__list-item pagination__list-item-orange">
        <i class="fa-solid fa-chevron-left"></i>
      </li>
      <li class="pagination__list-item pagination__list-item-text">Random</li>
      <li class="pagination__list-item pagination__list-item-orange">
        <i class="fa-solid fa-chevron-right"></i>
      </li>
      <li class="pagination__list-item pagination__list-item-blue">
        <i class="fa-solid fa-forward-step"></i>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.pagination {
  padding-top: 30px;
  padding-bottom: 45px;
  &__list {
    display: flex;
    justify-content: center;
    gap: 40px;
    align-items: center;
    cursor: pointer;
    &-item {
      padding: 23px 33px;
      color: white;
      transition: all 0.3s;
      

      &-blue {
        background: #0a2037;
      }
      &-blue:hover {
        background: #f26a15;
      }
      &-orange {
        background: #f26a15;
        border-radius: 50%;
      }
      &-orange:hover {
        background: #0a2037;
      }
      &-orange:hover > i {
        opacity: 0.3;
      }
      &-text {
        width: 320px;
        background: #f26a15;
        text-align: center;
        text-transform: uppercase;
        border: 1px solid transparent;
      }
      &-text:hover {
        background: white;
        border: 1px solid #f26a15;
        color: #f26a15;
      }
    }
  }
}

@media(max-width:767px) {
  .pagination {
    &__list {
      gap: 15px;
      &-item {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 10px;
        width: max-content;
      }
      
    }
  }
}
</style>

