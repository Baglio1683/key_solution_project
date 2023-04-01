<script>
import { propsToAttrMap } from '@vue/shared';



export default {

    name: 'AppInput',

    data() {
        return {

            text: " ",

        }

    },
    emits: ['submit'],

    methods: {
        cleanText() {
            this.text = "";
        }
    }
}

</script>

<template>
    <div class="container">
        <div class="row justify-content-center pt-3">
            <div class="col-6">
                <div class="form-group text-center">
                    <label for="text">Inserisci Commento</label>
                    <input type="text" class="form-control mb-3 mt-3" placeholder="scrivi commento" v-model="text"
                        @keyup.enter="$emit('submit', this.text) ; cleanText()">
                    <button class="btn btn-primary" @click="$emit('submit', this.text) ; cleanText()">Submit</button>
                </div>
            </div>

        </div>
    </div>
</template>

<style></style>