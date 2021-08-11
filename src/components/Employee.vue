<template>
  <div>
      <h1>Employee List</h1>
      <table border="1px">
          <tr>
              <td>Code</td>
              <td>Symbol</td>
              <td>Rate</td>
          </tr>
          <tr v-for="item in list" v-bind:key="item.code">
              <td>{{item.code}}</td>
              <td>{{item.description}}</td>
              <td>{{item.rate}}</td>
          </tr>
      </table>
  </div>
    
</template>

<script>
import axios from 'axios'


export default {
    name:"Employee",
    data()
    {
        return{list:undefined}
    },
    mounted()
    {
       // Vue.axios.get('127.0.0.1:4001/api/register')
       // .then((resp)=>{
           // this.list = resp.data.data
        //    console.warn(resp)
     //   })

      axios
      .get('https://api.coindesk.com/v1/bpi/currentprice.json')
      .then(response => 
      this.list = response.data.bpi
      //console.warn(response.data.bpi)
      )
     // (this.info = response))
      

    }

    
}
</script>

<style scoped>

</style>