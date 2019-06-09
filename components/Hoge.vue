<template lang="html">
    <div class="">
        <h1>{{ title }}</h1>
        Hello, I'm {{ name }}
        <div>
            {{ reverse }}
        </div>
        <div>
            <button type="button" name="button" @click="plus">
                {{ num }}
            </button>
        </div>
        <div :class="['hide', { seven: num === 7 }]">
            click 7 times
        </div>
            <div class="slot">
                <slot />
            </div>
        </div>
</template>

<script>
export default {
    mounted() {
        console.log('mounted')
    },
    props: {
        title: {
            type: String,
            default: 'Default title'
        }
    },
    data() {
        return {
            name: 'ikasaCTO',
            num: 0
        }
    },
    methods: {
        plus() {
            this.num++
        }
    },
    computed: {
        reverse() {
            return this.name.split('').reverse().join('')
        }
    }
}
</script>

<style lang="scss" scoped>
    .hide {
        display: none;
        &.seven{
            display: block;
        }
    }
    .slot {
        color: red;
    }
</style>