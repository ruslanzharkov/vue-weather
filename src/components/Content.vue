<template>
    <div>
        <p>This child components of Content.vue are:</p>
        <ul>
            <li v-for="child in childComponents" v-bind:key="child">
                {{child}}
            </li>
        </ul>
        {{ weather_data }}
    </div> 
</template>

<script>
export default {
    props: ['weather_data'],
    data() {
        return {
            childComponents: ['TempVarChart.vue', 'Highlights']
        }
    },

    methods: {

    },

    computed: {
        
    }
}
</script>

<style>

</style>
