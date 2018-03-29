<template>
  <ul class="tree">
    <li class="tree-item" v-for="(item, index) in tree" v-bind:key="index">
      <div class="tree-name">
        <a :href="'#'+item.id">{{item.name}}</a>
      </div>
      <tree v-if="item.tree" :tree="item.tree"></tree>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'tree',
  props: ['tree']
}
</script>

<style>
  .tree{
    padding-left: 2em;
  }
  .tree-name{
    cursor: pointer;
    outline: none;
  }
  .tree-name:hover{
    background: #eee;
  }
</style>
