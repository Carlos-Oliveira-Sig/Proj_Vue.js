<template>
  <div class="home">
    <div class="containerbtn">
      <btnAssign /> 
    </div>
    <div class="containercad">    
      <formCad />
    </div>
    <div class="containertext">
      <textmsg />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import formCad from '@/components/formCad.vue'
import btnAssign from '@/components/btnAssign.vue'
import textmsg from '@/components/textmsg.vue'


export default {
  name: 'Home',
  components: {
    formCad,
    btnAssign,
    textmsg
  }
}
</script>

<style scope>

 .home {
   Display: flex;
   background-image: url('/img/bgimg.png');
   background-color: rgb(255, 0, 106);
   background-repeat: no-repeat;
   background-size: cover;
   width: 100%;
   height: 963px;
   flex-direction: column;
   align-items: flex-end;
}

.home 

.containerbtn {
  padding-bottom: 40px;
  padding-top: 70px;
  padding-right: 350px;
}

.containercad {
  padding-right: 350px;
}

.containertext {
  padding-right: 900px;
  width: 600px;
  
}


</style>

