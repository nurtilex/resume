<script setup>
import { AnOutlinedHome } from "@kalimahapps/vue-icons";
import { ChPerson } from "@kalimahapps/vue-icons";
import { McBriefcaseLine } from "@kalimahapps/vue-icons";
import { MdOutlinedSchool } from "@kalimahapps/vue-icons";
import { AdAutomation3p } from "@kalimahapps/vue-icons";
import { LaCommentSolid } from "@kalimahapps/vue-icons";
import { AnOutlinedMail } from "@kalimahapps/vue-icons";
import { ChMenuHamburger } from "@kalimahapps/vue-icons";

import { ref } from "vue";

const isOpen = ref(false);
const lang = ref('RU');
</script>

<template>
<nav class="nav">
  <button class="btn" @click="isOpen = !isOpen"> <ChMenuHamburger style="transform:  scale(1.4)"/> </button>
  <button class="btn" v-show="isOpen" @click="lang = lang === 'RU' ? 'EN' : 'RU'">{{ lang }}</button>
  <ul v-show="isOpen" class="list">
    <li class="item" >
      <a :data-tooltip="'introduce'" class="link" href="#introduce"><AnOutlinedHome /></a>
    </li>
    <li class="item">
      <a :data-tooltip="'about'" class="link" href="#about"><ChPerson /></a>
    </li>
    <li class="item">
      <a :data-tooltip="'experience'" class="link" href="#experience"><McBriefcaseLine /></a>
    </li>
    <li class="item" >
      <a :data-tooltip="'mentoring'" class="link" href="#mentoring"><MdOutlinedSchool /></a>
    </li>
    <li class="item">
      <a :data-tooltip="'skills'" class="link" href="#skills"><AdAutomation3p style="transform: scale(1.4)" /></a>
    </li>
    <li class="item">
      <a :data-tooltip="'recommendations'" class="link" href="#recommendations"><LaCommentSolid /></a>
    </li>
    <li class="item">
      <a :data-tooltip="'contacts'" class="link" href="#contacts"><AnOutlinedMail/> </a>
    </li>
  </ul>
</nav>
</template>

<style scoped lang="scss">
.nav {
  position: fixed;
  top: 2rem;
  right: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  gap: 1rem;
  width: 70px;
  height: 100vh;
  scroll-behavior: smooth;

  .btn {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: transparent;
    color: var(--text);
    font-size: 0.8rem;
    border: 1px solid var(--text-2);
    outline-color: transparent;

    &:hover {
      cursor: pointer;
      border-color: var(--secondary);
      color: var(--secondary);

      & > svg {
        stroke: var(--secondary);
      }
    }
  }

  .list {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    border: 1px solid var(--text-2);
    padding: 0.5rem 0;
    margin: 0;
    border-radius: 32px;
    list-style: none;

    .item {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 50px;
      height: 50px;

      & > a.link {
        display: block;
        width: 100%;
        height: 100%;
        position: relative;
        text-decoration: none;

        &::before {
          visibility: hidden;
          content: attr(data-tooltip);
          position: absolute;
          top: 26%;
          right: 110%;
          display: flex;
          justify-content: center;
          align-items: center;
          height: 25px;
          padding: 0 0.5rem;
          background: var(--text-2);
          color: var(--primary);
          border-radius: 8px;

          &:hover {
            visibility: visible;
          }
        }
        display: flex;
        justify-content: center;
        align-items: center;
        color: var(--text);
        &:hover {
          color: var(--secondary);

          &::before {
            visibility: visible;
          }
        }
      }
    }
  }
}
</style>