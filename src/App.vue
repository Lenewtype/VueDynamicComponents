<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br/>
                <button class="btn btn-primary" @click="currentComponent = 'appBlue'">Load Blue Template</button>
                <button class="btn btn-success" @click="currentComponent = 'appGreen'">Load Green Template</button>
                <button class="btn btn-danger" @click="currentComponent = 'appRed'">Load Red Template</button>
                <hr/>
                <component :is="currentComponent">
                    <template slot="blue">
                        <p>Blue Content!</p>
                    </template>
                    <template slot="red">
                        <p>Red Content!</p>
                    </template>
                    <template slot="green">
                        <p>Green Content!</p>
                    </template>
                </component>
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        },
        data: function() {
            return {
                currentComponent: 'appBlue'
            };
        }
    }
</script>

<style>
</style>
