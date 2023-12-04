<script setup>
import { AkLinkedinBoxFill } from "@kalimahapps/vue-icons";
import { AkTelegramFill } from "@kalimahapps/vue-icons";
import { AkGithubFill } from "@kalimahapps/vue-icons";
import { AkInstagramFill } from "@kalimahapps/vue-icons";
</script>

<template>
  <aside class="sidebar">
    <header class="header">
      <h1>Nurtilek</h1>
      <div>Frontend Developer</div>
    </header>
    <section class="image"></section>
    <h3 class="email">nurtilex@gmail.com</h3>
    <h4 class="location">Base in Bishkek, Kyrgyzstan</h4>
    <div class="contacts">
      <a class="btn btn--linkedin" href="https://www.linkedin.com/in/nurtilex/" target="_blank"><AkLinkedinBoxFill /></a>
      <a class="btn btn--telegram" href="https://t.me/nurtilex" target="_blank"><AkTelegramFill/> </a>
      <a class="btn btn--github" href="https://github.com/nurtilex" target="_blank"><AkGithubFill/> </a>
      <a class="btn btn--insta" href="https://www.instagram.com/nurtilex/" target="_blank"><AkInstagramFill/> </a>
    </div>
    <button class="action-btn">Contact Me</button>
  </aside>
</template>

<style scoped lang="scss">

.sidebar {
  position: sticky;
  top: 1rem;
  left: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1.3rem;
  min-width: 30%;
  max-width: 35%;
  height: 95vh;
  color: var(--text);
  border: 1px solid var(--text-2);
  background: transparent;
  border-radius: 16px;
  padding: 1rem 2rem;

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 90%;
  }

  .image {
    width: 80%;
    height: 250px;
    border-radius: 16px;
    border: 1px solid var(--text-2);
  }

  .email, .location {
    margin: 0.3rem 0;
  }

  .contacts {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 70%;

    .btn {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      border: 2px solid var(--text-2);
      color: var(--text);

      &:hover {
        cursor: pointer;

        &.btn--linkedin {
          border-color: royalblue;
          color: royalblue;
        }
        &.btn--telegram {
          border-color: dodgerblue;
          color: dodgerblue;
        }
        &.btn--github {
          border-color: #606065;
          color: #606065;
        }
        &.btn--insta {
          border-color: #c22c75;
          color: #c22c75;
        }
      }
    }
  }

  .action-btn {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 1rem 2.5rem;
    background: var(--secondary);
    color: var(--primary);
    width: 80%;
    font-size: 1.2rem;
    font-weight: 700;
    border-radius: 16px;
    outline-color: transparent;
    border-color: transparent;

    &:hover {
      cursor: pointer;
    }
  }
}
</style>
<script setup>
</script>