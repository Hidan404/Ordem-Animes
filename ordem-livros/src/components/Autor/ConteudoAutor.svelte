<script>
   export let autor = null
</script>

{#if autor}
<div>
    <img src={autor.imagem} alt="Foto do autor">
</div>