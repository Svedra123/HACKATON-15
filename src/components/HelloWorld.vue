<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  
    <div id="contenedor">

          <div class="ima1">

              <div class="fvid" >

                  <div class="imgini">
                      <div class="edit">
                          <img class="edpet" id="btnED" onclick="ModalED()" src="../fotos/edit.png" alt="">
          





                          <span >Edit</span>
                      </div>


                      <div class="close">

                          <img class="delete" id="boton2" @click= "Modal2()" src="../fotos/delete.png" alt="">
                      

                          <div id="verModal2" class="modalContainer2">
                              <div class="modal-content2">
                                  <span class="closeEl1">×</span>
                                  <h2 style="padding-top: 30px;">Estas seguro que quieres eliminar este video??</h2>
                                  
                                  <button id="btnAP" class="btn">Aceptar</button>
                                  <button id="btncancelar" class="btn">Cancelar</button>

                              </div>
                          </div>
                          <span >Delete</span>
                      </div>

                  </div>

                  <img class="foto" src="../fotos/logo.png" alt="">

              </div>




      <div style="text-align: left; padding-left: 10px;">

                  <h3 style="font-size: 18px;margin-bottom: 9px;">Técnicas de programación </h3>

                  
                  <div style="font-size: 11px; color: #303030;">
                          0 visualizaciones
                  </div>

                  <article style="font-size: 12px;color: #808080;line-height: 18px;">
                      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eligendi possimus culpa doloribus. Quidem recusandae necessitatibus 
                      tempore dignissimos, neque, iure quo delectus optio nisi numquam aspernatur cumque eius blanditiis atque facilis?
                  </article>
                  <br>

    
    
      </div>
      <button class="btndetalle">Ver Detalle</button>

    </div>
  
  </div>
  </div>


</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  directives: {
    focus: {
      inserted: function Modal2() {

      let modal = document.getElementById("verModal2");
      let btn = document.getElementById("boton2");
      let span = document.getElementsByClassName("closeEl1")[0];
      let body = document.getElementsByTagName("body")[0];
      let cancelar = document.getElementById("btncancelar");
      
      let imaF = document.getElementsByClassName("ima1")[0];
      let deleteF = document.getElementById("btnAP");



      return Eliminar(modal,btn,span,body,cancelar, imaF, deleteF)
      }
    }
  }
}







</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

#contenedor {
    grid-column: 4;
    width: 1083px;
    height: auto;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    padding: 20px;
    grid-row-gap: 25px;
}

.ima, .ima1 {
    width: 255px;
    height: 450px;
    left: 22px;
    top: 97px;
    border: 1px solid #A1A1A1;
    box-sizing: border-box;
    box-shadow: 0px 0px 8px #000000;
    text-align: center;
    font-family: Roboto;
    font-style: normal;
    font-weight: bold;
}

.imgini {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 5px;
    font-size: 12px;
}

.close {
    display: inline-grid;
    text-align: -webkit-right
}

.edit {
    display: inline-grid;
    text-align: initial;
}

.foto {
    margin-top: 0px;
}

.delete {
    border: 1px solid #A1A1A1;
    transform: rotate(45deg);
}



.formcont, .formcontED {
    display: none;
    position: fixed; 
    z-index: 1;
    padding-top: 200px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%; 
    overflow: auto; 
    background-color: rgb(0,0,0);
    background-color: rgba(0,0,0,0.4);
    border: olive;
    
}

.formtAM , .formtED{
    display: grid;
    grid-template-columns: 1fr 1fr;
    width: 500px;
    height: 600px;
    padding-left: 40px;
    padding-top: 40px;
}

.geneAM, .geneED {
    width: 600px;
    height: 700px;
    border: aqua;
    background: azure;
    margin-left: 300px;
}

.barraAM, .barraED{
    display: grid;
    grid-template-columns: 1fr 1fr;
}

.close2, .close0 {
    margin-left: 150px;
    text-align: center;
    padding-top: 25px;
}

#boton2 , #boton3{

    background-color: none;
    display: block;
}

.modalContainer2, .modalContainer3 {
    display: none; 
    position: fixed; 
    z-index: 1;
    padding-top: 200px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%; 
    overflow: auto; 
    background-color: rgb(0,0,0);
    background-color: rgba(0,0,0,0.4);
}

.modalContainer2 .modal-content2, .modalContainer3 .modal-content3  {
    background-color: #fefefe;
    margin: auto;
    padding: 20px;
    border: 1px solid lightgray;
    width: 60%;
    text-align: center;
    height: 205px;
    width: 470px;
}

.modalContainer2 .closeEl1, .modalContainer3 .closeEl2 {
    color: black;
    float: right;
    font-size: 28px;
    font-weight: bold;
}

.btn {
    margin-top: 30px;
    width: 130px;
    height: 42px;
}

.btndetalle {
    width: 225px;
    height: 34px;
    left: 37px;
    top: 554px;
    background: #00C1AA;
    box-shadow: 0px 0px 6px rgba(0, 0, 0, 0.25);
    color: white;
    border: none;
}

.fvid {
    background-color: greenyellow;
}

</style>
