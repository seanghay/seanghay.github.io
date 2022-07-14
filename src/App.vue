<script setup>
import { ref, onMounted } from 'vue'
const timestamp = ref(0)


function invalidate(delta) {
  timestamp.value = new Date().toISOString()
  requestAnimationFrame(invalidate)
}

onMounted(() => {
  requestAnimationFrame(invalidate)
})

</script>


<template>
  <div class="container">
    <h1>hello there!👋 </h1>
    <p>rust, android, java, kotlin, javascript, node.js, deno and design.</p>
    <ul>
      <li><a href="https://seanghay.com">blog</a></li>
      <li><a href="https://github.com/seanghay">github</a></li>
      <li><a href="https://facebook.com/yath.seanghay">facebook</a></li>
      <li><a href="https://instagram.com/seanghay_yath">instagram</a></li>
      <li><a href="https://t.me/seanghay_yath">telegram</a></li>
      <li><a href="https://twitter.com/seanghay_yath">twitter</a></li>
    </ul>
    <small style="background-color: #333; color: white; padding: .2em .4em; border-radius: .2em;">{{ timestamp }}</small>
  </div>
</template>
<style>
:root {
  font-family: monospace;
  font-size: 14px;
  background-color: linen;
}


.container {
  max-width: 720px;
  margin: 0 auto;
  padding: 2em;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

ul,
li {
  padding: 0;
  list-style: none;
}

li {
  display: inline;
}

li a {
  padding: .5em 1em;
  background-color: rgba(0, 0, 0, .1);
  margin: .5em;
  display: inline-block;
  border-radius: .2em;
  color: black;
  border: 1px solid rgba(0, 0, 0, .1);
  font-weight: bold;
  text-decoration: none;
}

#bg {
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
}
</style>