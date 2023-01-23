<template>
  <div class="wrapper">
    <!-- header -->
    <div class="wrapper-content">
      <div class="view">
        <div class="container">
          <Form @onSubmit="handleSubmit"/>
          <TweetsList :items="items"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import './assets/scss/main.scss'
import TweetsList from '@/components/TweetsList.vue';
import Form from './components/Form.vue';

export default {
  name: 'App',
  components: {
    TweetsList,
    Form
  },
  data: () => ({
    items: [
      {
        id: 1,
        body: 'hello vue 3',
        likes: 12,
        avatar: 'https://avatars.dicebear.com/api/male/1.svg',
        date: new Date(Date.now()).toLocaleString()
      },
      {
        id: 2,
        body: 'hello world',
        likes: 6,
        avatar: 'https://avatars.dicebear.com/api/male/2.svg',
        date: new Date(Date.now()).toLocaleString()
      }
    ]
  }),
  methods: {
    handleSubmit(item) {
      this.items.push(item)
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
