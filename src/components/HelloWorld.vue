<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        <h3>TODO</h3>
        <input placeholder="Add new todo item"></input>
        <input type="submit" v-on:click="msg = 'new message'"/>
        <ul>
            <li>
                <input type="checkbox"/>
                <span class="todo">First todo</span>
            </li>
        </ul>
    </div>
</template>

<script lang="ts">
import {Component, Prop, Vue} from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
    @Prop()
    private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
    margin: 40px 0 0;
}
ul {
    list-style-type: none;
    padding: 0;
}
li {
    display: block;
    margin: 0 10px;
}
a {
    color: #42b983;
}
.todo {
    margin-left: 10px;
}
</style>
