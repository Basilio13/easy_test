<template>
<h1>{{title}}</h1>
<ul>
    <li v-for="element in elements" v-bind:key="element">
       {{element}}
    </li>
</ul>
</template>

<script>
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