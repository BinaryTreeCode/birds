<script>
  import Gird from "./lib/Gird.svelte";
import Grid from "./lib/Gird.svelte"


  let html = { 
        "nombre": "Cucarachero de Pantano",
        "modelo": "https://raw.githubusercontent.com/BinaryTreeCode/3d/master/Cistothorus%20apolinari%20V3.gltf",
        "info": ["Reino: Animalia", "Filo: Chordata","Clase: Aves","Orden: Passeriformes","Familia: Troglodytidae","Género: Cistothorus","Especie: C. apolinari"]
    }
</script>

<div>
  
<Grid {...html}/>
</div>

<style>
  div {
    height: 100%;
    width: 100%;
  }
</style>
