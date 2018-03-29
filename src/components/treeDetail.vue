<template>
  <div class="tree-detail">
    <details class="tree-detail-item" v-for="item in tree">
        <summary class="tree-detail-summary">{{item.name}}</summary>
      <tree-detail v-if="item.tree" :tree="item.tree"></tree-detail>
    </details>
  </div>
</template>

<script>
  export default {
    name: 'tree-detail',
    props: ['tree']
  }
</script>

<style>
  .tree-detail{
    padding-left: 2em;
  }
  .tree-detail-summary{
    cursor: pointer;
    outline: none;
  }
  .tree-detail-summary:hover{
    background: #eee;
  }
</style>
