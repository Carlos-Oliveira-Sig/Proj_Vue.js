<template>
  <div class="textHome">
    <div class="titletext">
        <p> Learn to code by </p>
        <p> watching others</p>
    </div>
    <div class="subtitletext">
      <p> see how wxperienced developers solve problems in real-time. <br/>
       Watching scripted tutorials is great, but understanding how  <br />
       developers think is invaluable.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'textmsg',
}
</script>

<style lang="scss" scoped>

.textHome {
  display: flex;
  flex-direction: column;
  
  
}

.titletext p {
  margin: 0;
  padding: 0;
  color: white;
  font-size: 30pt;
  font-weight: bold;
}

.subtitletext p {
  margin: 0;
  padding-top: 20px;
  color: white;
  font-size: 15pt;
  font-weight: bold;
}

</style>