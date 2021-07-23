<template>

  <div class="container">
    
    <div class="row row1 ">
        
      <table class="table1 table-bordered ">
   
         <tbody class="firsttable">
           <tr>
             <td rowspan="5" width="150px">
               <img src="../assets/logo1.jpg" width="100%" height="100%"  alt="">
            </td>
            <th scope="row">INSPECTION</th>
              <td colspan="12">dfsdfhlhfjyfyfffsd</td>
           </tr>
          <tr>
             <th scope="row">SOURCE</th>
                <td colspan="12">DLHFLAFDLKSAJF</td>
     </tr>
     <tr>
       <th scope="row">SPAN START</th>
       <td colspan="5">DLHFLF</td>
       <th scope="row" colspan="4">SPAN END</th>
       <td colspan="3">DLHFLAFDJF</td>
     </tr>
 
     <tr>
       <th scope="row">POLE TYPE</th>
       <td >DF</td>
       <th scope="row">VOLTAGE</th>
       <td colspan="6">DLHF</td>
       <th scope="row">DATE</th>
       <td colspan="3">3/4/2021</td>
     
       
     </tr>
 
     <tr>
       <th scope="row">COORDINATES</th>
       <td colspan="10">2.3332333 4.565444</td>
       <th scope="row">PHASE</th>
       <td colspan="1">ALL</td>
     </tr>
 
 
      </tbody>
    </table>
   
  
 
   </div>

  <div class="row row2 rowpic">
    <div class="col-sm-6 col">
      <div class="title"><h5 >SITE CONDITION</h5>
      </div>

      <div class="card-body">
        
        <img src="../assets/index.jpeg" alt="">
              <!-- <button class="btn">button</button> -->
      </div>
    </div>
    <div class="col-sm-6 col">
      <div class="title"><h5 >SITE CONDITION</h5>
      </div>

      <div class="card-body">
        <img src="../assets/index.jpeg"  alt="">
              <!-- <button class="btn">button</button> -->
      </div>
    </div>

         
   </div>

   <div class="row row3 rowpic">
    <div class="col-sm-6 col">
      <div class="title"><h5 >CLEARANCE</h5>
      </div>

      <div class="card-body">
        <img src="../assets/index.jpeg" alt="">
              <!-- <button class="btn">button</button> -->
      </div>
    </div>
    <div class="col-sm-6 col">
      <div class="title"><h5 >POLE NO.</h5>
      </div>

      <div class="card-body">
        <img src="../assets/index.jpeg" alt="">
              <!-- <button class="btn">button</button> -->
      </div>
    </div>
   </div>
   <div class="row  row4">
    <table class="table2 table-bordered"  >
   
      <tbody class="firsttable">
        <tr>
          <th colspan="4">CLEARANCE FROM GROUND TO CONDUCTOR FOR 33KV</th>
          <th colspan="2" rowspan="2">AREA</th>
        </tr>
        <tr>
          <th rowspan="2">CLEARANCE</th>
          <th rowspan="2">>STANDARD(m)</th>
          <th colspan="2">COMPLIANCE</th>
        </tr>
        <tr>
          <th >YES</th>
          <th >NO</th>
          <td >CROSS ROAD</td>
          <td ></td>
        </tr>
    
        <tr>
          <td >ROAD</td>
          <td >6.10</td>
          <td ></td>
          <td ></td>
          <td >PADDY FIELD</td>
          <td ></td>
        </tr>
        <tr>
          <td >ROAD SIDE</td>
          <td >6.10</td>
          <td ></td>
          <td ></td>
          <td >NO ACCESS</td>
          <td >qwertrt</td>
        </tr>
        <tr>
          <td >NO ACCESS</td>
          <td >6.10</td>
          <td ></td>
          <td ></td>
          <td >OTHERS</td>
          <td ></td>
        </tr>
         </tbody>
       </table>

</div>
<div class="row row5">
  <div class="title2 ">RECOMMENDATION
  </div>

  <div class="form1">
    <form action="/action_page.php">
      <label  for="fname">CONDITION :</label>
      <input type="text" id="condition" name="firstname" placeholder="">
  
      <label for="lname">RECOMMENDATIONS :</label>
      <input type="text" id="recommendation" name="lastname" placeholder="">
  
      <label  for="country">REMARKS :</label>
      <input type="text" id="remarks" name="">
    </form>
  </div>

</div>


</div>
</template>
<script>


import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    setup() {
        
    },
})
</script>
<style scoped>
.container{
  margin-top: 20px; 
  margin-bottom: 20px; 
  padding:0;
  align-items: center;

 
  
  width:50%;
  height: 100%;
 
}
.row1{
  height: 10%;
  margin-bottom: 10px;
 
}

.table1, td, th {
border: 1px solid black;
}

.table1 {
border-collapse: collapse;
width: 100%;
height:100%;
}
.table1 td,th{
font-size: 12px;
text-align: left;
padding:2px 5px;
}
th{
background-color:#EEEEEE;
}
.row2{

  height:30%;
  margin-top:10px;
  display: flex;

   
}
.col{
    width: 50%;
    padding: 0; 
    border: 1px solid black;
    position: relative;
    /* box-sizing: border-box; */
}
.title{
   width: 100%;
   padding: 0;
   margin: 0;
   border: 0;
 height:20px;
 position: absolute;
  border-bottom: 1px solid black;
  padding-top:5px;
  
}

.title h5{
  /* position:relative; */
  bottom: 10px;
  font-size: 12px;
  
  text-decoration: none;
  text-align: center;
  vertical-align:middle;
}
.card-body{
  width: 100%;
  padding: 5px 5px 5px 5px;
  margin: 0;
}
.card-body img{
  width:100%;height:85%
}

.row3{

  height:30%;
  margin-bottom: 10px; 
  display: flex;
   
}
.row4{
height:auto;
margin-top: 0;
margin-bottom: 10px; 
 
}
.table2, td, th {
border: 1px solid black;
}

.table2 {
border-collapse: collapse;
width: 100%;

}
.table2 td{
font-size: 12px;
text-align:center;

}

.row5{
 
  padding:0;
  height:20%;
  border:1px solid black;

}
.title2{
  width: 100%;
  height:20;
  font-size: 12px;
  border-bottom:1px solid black;
}
.form1{
height:80%;
width: 100%;
padding:10px 5px 0px 10px;
border:0;
}
.form1 label{
  float: left;
  font-style: bold ;
  font-size: 12px;
}
input[type=text]{
  width: 100%;
  height:30px;
  background-color: white;
  margin-bottom: 5px;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 2px;
  box-sizing: border-box;
}
</style>


