<template>
  <div class="avideo">
    <h1>Agregar Video</h1>

    <form id="formED" class="formcontED" action="">
                              
      <div class="geneED">

        <div class="formtED">
                                  
          <input type="text" name="titulo" id="" placeholder="Titulo" >
          <input type="text" name="url" id="" placeholder="Url" >
          <input type="text" name="descripcion" id="" placeholder="Descripcion" >
        </div>                          

      

        <button class="btn">Aceptar</button>
        <button id="btncanED" class="btn">Cancelar</button>


      </div>
                              
    </form>

  </div>
</template>

<script>
// @ is an alias to /src
// v-model= "agregarVideo"
// @click= "agregarVideo" 


export default {

    
     video: [
      {titulo: '1', url:'1' , descripcion: '1'}
     ],



    agregarVideo () {
        this.video.push({
         titulo: this.agregarVideo, url: this.agregarVideo, descripcion: this.agregarVideo
       });
      this.agregarVideo = ''

   }
    

}

</script>

<style  scoped>
    .formcont, .formcontED {
    position: fixed; 
    z-index: 1;
    padding-top: 200px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%; 

    
}

.formtAM , .formtED{
    display: grid;
    grid-template-columns: 1fr 1fr;
    width: 500px;
    height: 42px;
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

</style>