<template>
  <div class="col-md-8">
    <h3 class="reply">评论回复：</h3>
    <h2 v-show="comments.length === 0">暂无评论，点击左侧添加评论！！！</h2>
    <ul class="list-group">
      <Item v-for="(comment,index) in comments" :key="index" :comment="comment"
            :deletecomment="deletecomment" :index="index"/>
    </ul>
  </div>
</template>

<script>
  import Item from './Item'

  export default {
    name: 'List',
    props:['comments','deletecomment'],
    components:{
      Item
    }
  }
</script>

<style scoped>
  .reply {
    margin-top: 0px;
  }
</style>
