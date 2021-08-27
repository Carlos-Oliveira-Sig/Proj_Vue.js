<template>
  <div class="assignbtn">
     <div class="containerbtnassign">
        <input type="submit" class="submit-btn" value="Try it free 7 days then $20/mo.thereafter">
      </div>   
  </div>
</template>

<script>
export default {
  name: 'btnAssign',
}
</script>

<style scope>

.containerbtnassign input {
  background-color: purple;
  border-radius: 12px;
  border-color: purple;
  width: 460px;
  padding: 10px;
  margin: 0;
  font-weight: bold;
  font-size: 12pt;
  color:white;
  border-style: solid;
  cursor: pointer;
  outline: none;
  transition: all .4s ease-out;
}

.containerbtnassign input:hover {
  background-color: white;
  color: purple
}



.assignbtn {
    display: flex;
    height: 42px;
    width: 460px;
}


</style>