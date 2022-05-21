<script setup lang="ts">
import SvgIcon from '../components/SvgIcon.vue'
</script>

<template>
  <div class="wrapper">
    <header>
      <SvgIcon name="mangosteen" />
      <h1>凤果记账</h1>
    </header>
    <main class="main" ref="{main}">
      <div class="card">
        <SvgIcon name="pig" />
        <h2>
          会赚钱
          <br />
          还要会省钱
        </h2>
      </div>
    </main>
    <footer>
      <div class="actions">
        <router-link class="fake" to="/start"> 跳过 </router-link>
        <router-link to="/welcome/2">下一页</router-link>
        <router-link to="/start">跳过</router-link>
      </div>
    </footer>
  </div>
</template>

<style lang="scss">
.wrapper {
  height: calc(100vh - var(--welcome-nav-height));
  display: flex;
  flex-direction: column;
  background-image: linear-gradient(
    to bottom,
    var(--welcome-bg-start) 0%,
    var(--welcome-bg-end) 100%
  );
  margin-bottom: var(--welcome-nav-height);
  > header {
    flex-shrink: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-top: 66px;
    color: #d4d4ee;
    > svg {
      width: 64px;
      height: 69px;
    }
  }
  > main {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    position: relative;
    margin: 16px 16px var(--welcome-nav-gap);
  }
  > footer {
    flex-shrink: 0;
  }
}

.slide_fade_enter_active,
.slide_fade_leave_active {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  transition: all 0.5s ease-out;
}

.slide_fade_enter_from {
  transform: translateX(100vw);
}
.slide_fade_leave_to {
  transform: translateX(-100vw);
}

.card {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  background: var(--welcome-card-bg);
  border-radius: 8px;
  padding: 16px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  > h2 {
    margin-top: 40px;
  }
}

.actions {
  position: fixed;
  z-index: var(--z-index-bottom-nav);
  background: var(--welcome-bg-end);
  width: 100%;
  max-width: 480px;
  left: 50%;
  bottom: 0;
  transform: translateX(-50%);
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 24px;
  height: var(--welcome-nav-height);
  padding: 0 16px;
  color: var(--welcome-text);
  padding-bottom: var(--welcome-nav-gap);
  > .fake {
    visibility: hidden;
  }
}
</style>
