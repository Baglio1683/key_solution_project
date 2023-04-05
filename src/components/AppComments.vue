<script>

export default {

    name: 'AppComments',



    emits: ['delete'],

    props: {

        comment: String,
        index: Number
    }


}

</script>

<template>
    <div class="card rounded-4 mb-3">
        <div class="card-body rounded-4 border-danger-subtle">
            <h5 class="card-title">Commento {{ index + 1 }}</h5>
            <p class="card-text">{{ comment }}</p>
            <button class="btn btn-danger" @click="$emit('delete', index)">elimina commento</button>
        </div>
    </div>
</template>

<style scoped>
div {
    background-color: white;
    color: black;
    word-wrap: break-word;
    white-space: normal;
}
</style>