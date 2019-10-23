<template>
<div class="wrapper">
  <div class="no">{{formatted}}</div>
</div>
</template>

<script>
import NumFmt from "ilib/lib/NumFmt";
const fmt = new NumFmt({
   locale: "de-DE"
});

//const str = fmt.format(1234567.89);

export default {
  name: "iLibExample",
  data: ()=>{
    return {
      testNo: 1234567.89
    }
  },
  computed: {
    formatted: function(){
      return fmt.format(this.testNo);
    }
  }
};
</script>

<style scoped>
.wrapper{
  width: 100%;
  display: flex;
  align-items: center;
}
</style>

