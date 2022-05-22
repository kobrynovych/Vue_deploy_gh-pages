<template>
    <div>
        <h1>AppPosts2</h1>

        <!-- props -->
        <div>text: {{name}}</div>
        <div>text2: {{name2}}</div>

        <!-- slot -->
        <slot></slot>
        <slot name="children2"></slot>
        <slot name="children3"></slot>

        <!-- onClick -->
        <button v-on:click="onClick()">Ok</button>
        <button @click="onClick()">Ok2</button>

        <!-- событие click не будет всплывать дальше -->
        <a @click.stop="() => {}"></a>
        <!-- событие submit больше не будет перезагружать страницу -->
        <form @click.prevent="() => {}"></form>
        <!-- модификаторы можно объединять в цепочки -->
        <a @click.stop.prevent="() => {}"></a>


        <!-- class -->
        <div class="active"></div>
        <div class="active" v-bind:class="{'active2': isActive === true}"></div>
        <div class="active" :class="{'active2': isActive === true}"></div>
        <div class="active" :class="{active2: isActive, 'text-danger': true}"></div>
        <div class="active" :class="isActive ? 'active2' : ''"></div>

        <!-- style -->
        <h1 
            style="color: red:"
            :style='{
                color: searchValue.length < 5 ? "red" : "blue",
                fontSize: searchValue.length < 3 ? "1rem" : "1.5rem"
            }'
        >
            Asd asd
        </h1>

        <!-- ref -->
        <input ref="search" v-model="searchValue" />

    </div>
</template>

<script>
export default {
    components: {

    },

    props: {
        name: {
            type: String,
            default: '',
        },
        name2: {
            type: String,
            default: '',
        }
    },

    data() {
        return {
            isActive: true,
            searchValue: '',
        };
    },

    created() {
      
    },

    mounted() {
        this.$refs["search"].focus();
        // this.$refs.search.focus();
        // this.$refs.search.value;
    },

    beforeDestroy() {

    },

    updated() {

    },

    watch: {

    },

    computed: {

    },
    
    methods: {
        onClick() {

        }
    }
}
</script>