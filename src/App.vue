<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
  import Header from './components/layouts/Header';

export default {
  name: "app",
  components: {
    Header,
  },
}
</script>

<style>
*
{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body
{
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.5;
}

.btn
{
  display: inline-block;
  border: none;
  border-radius: 2px;
  color: #fff;
  background: #555;
  padding: 7px 20px;
  cursor: pointer;
}

.btn:hover
{
  background: #666;
}
</style>
