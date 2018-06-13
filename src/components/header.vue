<template>
  <header>
    <h1 class="main-title"> Peliculas </h1>
    <nav>
      <button clsss="header_log" type="button"> Login </button>
      /
      <button clsss="header_log" type="button"> Sing Up</button>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'FilmsHeader',
  props: {
    msg: String,
  }
}


</script>

<style>

</style>
