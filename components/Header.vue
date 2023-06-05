<template>
  <header class="header">
    <div class="header-background"></div>
    <div class="header__content-progress-bar"></div>
    <div class="header__content">
      <div class="header__content-container">
        <h1
          class="header__content-title header__content-fade-in header__content-typing-text"
        >
          TEST FROM I-ONE WEB AGENCY
        </h1>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
  height: 508px;
  display: flex;
  transition: all 0.3s;
  position: relative;
  &-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: url("~~/assets/images/header-bg.png");
    background-attachment: fixed;
    animation: fade-in-background 2s forwards;
  }
  &__content {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0 15px;
    width: 100%;
    &-container {
      max-width: max-content;
    }
    &-title {
      font-style: normal;
      font-weight: 500;
      font-size: 44px;
      line-height: 52px;
      letter-spacing: 0.1em;
      color: #ffffff;
      transition: all 0.3s;
    }
    &-progress-bar {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0;
      height: 5px;
      background-color: #f26a15;
      animation: fill-progress 4s forwards, hide-progress 1s forwards;
    }
    &-typing-text {
      overflow: hidden;
      white-space: nowrap;
      border-right: 0.15em solid #f26a15;
      animation: typing 4s steps(40) infinite;
      opacity: 0;
      animation: fade-in 2s forwards;
      width: 100%;
    }
  }
}

@keyframes fill-progress {
  0% {
    width: 0;
  }
  100% {
    width: 100%;
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
    width: 0;
  }
  50% {
    border-color: transparent;
  }
  100% {
    opacity: 1;
    width: 100%;
  }
}
@keyframes fade-in-background {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
@media (max-width: 767px) {
  .header__content-title {
    font-size: 20px;
  }
}
</style>