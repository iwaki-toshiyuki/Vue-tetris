<script lang="ts" setup>
  import { reactive } from "vue";
  import { useRouter } from "vue-router";

  const state = reactive({ name: "" });
  const router = useRouter();
  const playGame = () => {
    router.push({ name: "PlayPage", query: { name: state.name } });
  }
</script>

<template>
  <h1>操作説明</h1>
  <h3>下矢印で下移動する</h3>
  <h3>上矢印で即時落下させる</h3>
  <h3>左右矢印で横移動する</h3>
  <h3>スペースキーで回転する</h3>
  <button v-on:click="playGame()">
    プレイ画面に戻る
  </button>
</template>

<style>
</style>
