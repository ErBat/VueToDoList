<template>
    <div>
        <input v-model="inputVal">
        <button v-on:click="addItem(inputVal)">Add item</button>
    </div>
</template>

<script>
export default {
    data() {
        return { inputVal: '' }
    },
    methods: {
        addItem: function (value) {
            store.commit('addItem', value)
        }
    }
}
</script>