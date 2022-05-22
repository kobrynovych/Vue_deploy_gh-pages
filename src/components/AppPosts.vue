<template>
  <div>
      <div>text: {{asd}}</div>
      <div>text: {{asd2}} {{asd3}}</div>

      <!-- <input :value='asd2' @change="handleChange" /> -->
      <!-- <input :value='asd2' @change="handleChange($event, 'asd')" /> -->
      <input v-model="asd2" />
      <div>{{asd2}}</div>


      <!-- if -->
      <div>
          <span>show el: </span>
          <span v-if="true">asdasd</span>

          <span>hide el: </span>
          <span v-if="false">asdasd</span>
          <span v-else>2222</span>

          <!-- 1. -->
          <!-- <div v-if="type === 'A'">A</div>
          <div v-else-if="type === 'B'">B</div>
          <div v-else-if="type === 'C'">C</div>
          <div v-else>D</div> -->

          <!-- 2. -->
          <h1 v-show="true">Hello!</h1>
          <h1 v-show="false">Hello!</h1>

      </div>
      <!-- ./if -->


      <!-- for -->
      <ul>
        <!-- цикл для обєктів -->
        <!-- <li v-for="el in jsonplaceholder" :key="el.id">{{el}}</li>    -->

        <!-- цикл для масивів -->
        <!-- <li v-for="el of jsonplaceholder" :key="el.id">{{el.title}}</li> -->
        <!-- <li v-for="(el, index) in jsonplaceholder" :key="el.id">{{index}}: {{el.title}}</li> -->
        <!-- <li v-for="({id, title}, index) in jsonplaceholder" :key="id">{{index}}: {{title}}</li> -->
      </ul>

      <!-- <ul>
          <template v-for="el in jsonplaceholder">
              <li :key="el.id">{{el.title}}</li>
              <li :key="el.id">{{el.id}}</li>
          </template>
      </ul> -->
      <!-- ./for -->


      <!-- computed: -->
      <div>fullName: {{fullName}}</div>

  </div>
</template>

<script>
// import { Datetime } from "vue-datetime";
// import VueTagsInput from '@johmun/vue-tags-input';

export default {
    components: {
        // Datetime,
        // VueTagsInput,
    },

    props: {
        // errors1: String,
        // errors2: Number,
        // errors3: Boolean,
        // errors4: Object,
        // errors5: Array,
        // errors6: Function,

        // propA: [String, Number],
        // propB: Number || String,

        // errors7: {
        //     type: Number,
        //     default: 0,
        // },
        // errors8: {
        //     type: Object,
        //     default: () => ({}),
        // },
        // errors9: {
        //     type: Array,
        //     default: () => [],
        // },
        // errors10: {
        //     type: Function,
        //     default: () => {},
        // },

        // id: {
        //     type: Number || String,
        //     required: true,
        //     default: () => Math.random()
        // },

        // propF: {
        //     validator: function(value) {
        //       return ['success', 'warning', 'danger'].indexOf(value) !== -1
        //     }
        // }
    },

    data() {
        return {
            asd: 2,
            asd2: 'asd2',
            asd3: true,
            asd4: [],
            asd5: {},
            asd6: null,
            // asd7: this.errors7,

            asdasd: 'asdasd',

            jsonplaceholder: null,

            intervalId: null,

            obj: {
              name: 'asdasd',
              name2: 'asdasd2',
            },

            f_name: 'Oleh',
            l_name: 'K.',
        };
    },

    created() {
      
    },

    mounted() {
        // this.getDate();

        // this.intervalId = setInterval(this.handleChange, 3000);

        // document.querySelector('.c-datetime').addEventListener('click', this.handleChange);
    },

    beforeDestroy () {
        // clearInterval(this.intervalId);
        // document.querySelector('.c-datetime').removeEventListener('click', this.handleChange);
    },

    // updated() {
        // this.asd = this.asd + 1;
        // this.asd = 12;
    // },

    watch: {
        // // 1. 
        // asdasd: {
        //     handler(newAsdasd, prevAsdasd) {
        //         if (newAsdasd && prevAsdasd) {
        //             this.asd = 12;
        //         }
        //     },
        //     deep: true,        // глибоке стеження, використовується для обєктів
        // },

        // // 2. 
        // 'obj.name': {
        //     handler(newName, prevName) {
        //         if (newName && prevName) {
        //             this.asd = 12;
        //         }
        //     },
        //     deep: true,        // глибоке стеження, використовується для обєктів
        // },
        // 'obj.name2': {
        //     handler(newName, prevName) {
        //         if (newName && prevName) {
        //             this.asd = 12;
        //         }
        //     },
        //     deep: true,        // глибоке стеження, використовується для обєктів
        // },

        // // 3. 
        // 'asd': 'getDate',
    },

    computed: {
        fullName() {
            return this.f_name + ' ' + this.l_name;
        },
    },
    
    methods: {
        // handleChange(event) {
        handleChange() {
            // this.asd2 = 'wwwww';
        },

        getDate() {
          // fetch('https://jsonplaceholder.typicode.com/todos')
          //   .then(response => response.json())
          //   .then(json => {
          //     this.jsonplaceholder = json;
          //   })
        },
    }
}
</script>