<template>
    <div class="colors">
        <h3>Colors</h3>

        <ul>
            <li v-for="color in colors" :key="color.id">
                <span :class="color.name">{{ color.name }}</span>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'Colors',
  props: {
    colors: Array
  }
}
</script>

<style>
    ul {
        list-style-type: none;
        padding: 0;
    }
    li {
        display: inline-block;
        margin: 0 10px;
    }
    .red {
        color: red;
    }
    .green {
        color: green;
    }
    .blue {
        color: blue;
    }
</style>