<template>
<div class="title">
  <img src="https://th.bing.com/th/id/Rf5d1c97d6d391c40bd3f5caae69bca3b?rik=MgSZ%2bIDQgVdyQw&riu=http%3a%2f%2fwww.wired.com%2fwp-content%2fuploads%2f2015%2f07%2fFEATURED-TWITTER_Loss-01-1200x630.jpg&ehk=p%2fpt6fyTxtmqVOoraqYeM4JwbCZMhjsgpQywziVXb8w%3d&risl=&pid=ImgRaw">
  <h1>Twotter</h1>
</div>
</template>

<script>
export default {
  name: "Title"
}
</script>

<style scoped>
.title {
  display: flex;
    align-items: center;
  background-color: #2CABE0;
  /* border: 5px solid black; */
}
h1{
  font-family: "Helvetica Neue",Helvetica;
  color: white;
  /* border: 5px solid black; */
  margin-left: 150px;
}
img{
  position: absolute;
  height: 100px;
  width: 150px;
  /* border: 5px solid black; */
}
</style>
