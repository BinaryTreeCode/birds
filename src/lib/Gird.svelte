
<script>
    import Model from "./Model.svelte"

    export let nombre = "el conejo"
    export let info = ["Model", "Info", "Info", "Info", "Info", "Info", "Info"];

    export let model = 'https://raw.githubusercontent.com/BinaryTreeCode/3d/master/conejo.gltf';
</script>

<div class="grid">
    <div class="title">
        <h1>Cucarachero de Pantano</h1>
    </div>
    <div class="text">
            {#each info as text}
                <li>{text}</li>
                <br>
                <br>
            {/each}
    </div>
    <div class="model">
        <Model />
    </div>
</div>

<style>
    .grid {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;

        color: rgba(255, 255, 255, 0.87);
    }
    .title {
        grid-row: 1;
        grid-column: 1 / 4;  

        align-self: center;
    }

    .text {
        grid-row: 2 / 4;
        grid-column: 1 / 2; 

        
    }
    .model {
        grid-row: 2 / 4;
        grid-column: 2 / 4;  
        text-align: center;;
    }
</style>


