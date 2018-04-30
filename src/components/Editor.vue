<template>
    <div class="editor">
      <h1>エディター画面</h1>
      <span>{{ user.displayName }}</span>
      <button @click="logout">ログアウト</button>
    </div>
</template>

<script>
    export default {
      name: "editor",
      data() {
        return {
        }
      },
      props: ['user'],
      methods: {
        logout: function() {
          firebase.auth().signOut();
        }
      }
    }
</script>

<style scoped>

</style>
