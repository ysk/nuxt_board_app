<template>
  <section class="container">
    <h1>{{title}}</h1>
    <p>{{message}}</p>

    <router-link to="/">Go to TOP</router-link>
  </section>
</template>


<script>
export default {
  data: function(){
    return {
      title:'Other',
      message: 'これは別ページです',
    };
  },
};
</script>


<style>
.container {
  padding:5px 10px;
}
h1 {
  font-size: 60pt;
  color: #345980;
}
p {
  padding-top:5px;
  font-size: 20pt;
}
pre {
  padding: 10px;
  font-size: 18pt;
  background-color: #efefef;
}
hr {
  margin:10px 0px;
}
</style>