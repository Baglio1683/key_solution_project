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
    },


    deleteElement(index) {

      this.comments.splice(index, 1);

    }


  },
}

</script>

<template>
  <AppHeader></AppHeader>
  <main>
    <AppInput @submit="addcomments"></AppInput>
    <div class="container mt-5">
      <div class="row justify-content-center">
        <hr>
        <div class="col-6">
          <h2 class="mb-4">Lista Commenti: </h2>
          <AppComments v-for="(comment, index) in comments" :comment="comment" :index="index" @delete="deleteElement">
          </AppComments>
        </div>
      </div>
    </div>
  </main>
</template>


<style lang="scss">
main {
  background-color: #ed5b27;
  color: white;
  min-height: 85vh;

}
</style>