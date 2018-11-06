<template>
  <section class="container">
    <div>
      <ul>
         <li>
          <el-card shadow="hover">
            <nuxt-link to="/category">ファイナンシャルプランナー</nuxt-link>
          </el-card>
      </li>
    </ul>
    </div>
  </section>
</template>

<script>
 import FlashCardTop from '@/components/FlashCardTop.vue'

export default {
  components: {
    FlashCardTop
  }
}
</script>

<style>

.container {
  min-height: 100vh;
  /* display: flex; */
  width: 40%;
  margin: 0 auto;
  margin-top: 30px;
}

/* .title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
} */
</style>
