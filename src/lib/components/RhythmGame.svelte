<script lang="ts">
    import Background from "./Background.svelte";
</script>

<div id="rhythmGame">
    <Background/>
</div>

<style>
    *{
        --rhythmViewportHeight: 80vh;
    }

    #rhythmGame{
        height: var(--rhythmViewportHeight);
        border: 1px solid;
        width: calc(100vw  - 2px);
        
        overflow-x: hidden;
        background: #AADCFF;
    }
</style>