<template>
    <p>The user is {{age}} years old</p>
    <button type="button" @click="onClickAge">Update Age</button>
    <p>{{ ageDoubled }}</p>
</template>

<script>
export default {
    name: "User",
    props: {
        age: {
            type: Number,
            //required: true,
            //default: 20
            validator(value) {
                return value < 130
            }
        }
    },
    emits: ['age-change'],
    computed: {
        ageDoubled() {
            return this.age * 2
        }
    },
    methods: {
        onClickAge() {
            this.$emit('age-change', 3)
        }
    }
}
</script>