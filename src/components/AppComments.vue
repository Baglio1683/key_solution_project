<script>

export default {

    name: 'AppComments',

    props: {
        comment: String
    }

}

</script>

<template>
    <li>
        {{ comment }}
    </li>
</template>

<style></style>