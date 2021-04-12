<template>
    <div id="app">
        <div>
            <NewCarousel />
        </div>
        <!-- <div class="table-box">
            <NewTable />
            <NewTable />
        </div> -->
    </div>
</template>

<script>
import NewCarousel from "./components/NewCarousel.vue";
// import NewTable from "./components/NewTable.vue"

export default {
    name: "App",
    methods: {
        say: function (message) {
            alert(message)
        }
    },
    components: {
        NewCarousel,
        // NewTable
    },
    data() {
        return {
            title: "030",
            vHtml: "<p>ˊ ˇ`/</p>",
            user: {
                name: "vuuue",
            },
            items: [{ text: "Hello" }, { text: "Love You" }],
            condition: true,
        };
    },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#app .table-box {
    margin: 50px 0 0 0;
}
</style>
