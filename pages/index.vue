<template>
  <div class="home">
    <div class="card" style="width: 18rem;">
      <div class="card-body">
        <h5 class="card-title">Username</h5>
        <h6 class="card-subtitle mb-2 text-muted">User email</h6>
        <p class="card-text">User Address</p>
        <a href="#" class="card-link">Card link</a>
        <a href="#" class="card-link">Another link</a>
      </div>
    </div>
  </div>
</template>

<style>
  .home{
    margin: 10px;
  }

  .card {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    transition: 0.3s;
    width: 40%;
    border-radius: 5px;
    background-color: #f1f1f1;
  }

  .card:hover {
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
  }

  .container {
    padding: 2px 16px;
  }
</style>
<script>
export default {
  name: 'IndexPage',
  data: () => ({
    users: []
  }),
  async fetch() {
    this.users = await this.$http.$get('https://api.nuxtjs.dev/posts')
  },
}
</script>
