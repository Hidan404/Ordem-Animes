<script lang="ts">
    import { marked } from "marked";
    import autores from "../../constants/autores";
    
    export let autorSelecionado = autores[0]
</script>

{#if autorSelecionado}
<div class="flex flex-col gap-5">
    <img src={autorSelecionado.imagem} alt="Foto do autor">
    <article class="prose lg:prose-xl prose-invert">
        {@html marked.parse(autorSelecionado.biografia)}
    </article>
</div>
{/if}