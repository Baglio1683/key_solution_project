<script>

import AppInput from './components/AppInput.vue';
import AppComments from './components/AppComments.vue';
import AppHeader from './components/AppHeader.vue';


export default {

  data() {
    return {
      comments: [],
    }
  },
  components: {
    AppInput,
    AppComments,
    AppHeader
  },
  methods: {
    addcomments(text) {
      this.comments.push(text);
    }
  },
}

</script>

<template>
  <AppHeader></AppHeader>
  <main>
    <AppInput @submit="addcomments"></AppInput>
    <div class="container mt-5">
      <div class="row justify-content-center ">
        <div class="col-6">
          <ul>
            <h2>Lista Commenti: </h2>
            <AppComments v-for="comment in comments" :comment="comment">
            </AppComments>
          </ul>
        </div>
      </div>
    </div>
  </main>
</template>


<style>

main{
  background-color: #ed5b27;
  color: white;
  min-height: 85vh;

}

</style>