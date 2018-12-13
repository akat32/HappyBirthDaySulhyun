<template>
    <router-view/>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
@font-face{font-family: 'NotoSansCJKkr-Medium'; src:url('./assets/font/NotoSansCJKkr-Medium.otf');}
@font-face{font-family: 'NotoSansCJKkr-Bold'; src:url('./assets/font/NotoSansCJKkr-Bold.otf');}
@font-face{font-family: 'NotoSansCJKkr-Regular'; src:url('./assets/font/NotoSansCJKkr-Regular.otf');}
input{
  -webkit-appearance: none;
  -webkit-border-radius: 0;
}
body{
  margin : 0;
}
a:link { color: red; text-decoration: none;}
a:visited { color: black; text-decoration: none;}
a:hover { color: blue; text-decoration: underline;}
a.noul:hover { text-decoration:none !important }
</style>
