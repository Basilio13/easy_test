<template>
<h1>{{title}}</h1>
<ul>
    <li v-for="element in elements" v-bind:key="element">
        <p>{{element.id}}.
            <span>{{element.first_name}}</span>{{' '}}
            <span> {{element.last_name}}</span>
        </p>
    </li>
</ul>
</template>

<script>
//Импорт json
import json from '../../data.json'
export default {
    data() {
        return {
    title: 'List',
    elements: json
    }
}
}
</script>

//Стили
<style scoped>
    li {
        border: 1px solid rgb(175, 175, 175);
        display: flex;
        justify-content: space-between;
        padding: 5px;
    }
</style>