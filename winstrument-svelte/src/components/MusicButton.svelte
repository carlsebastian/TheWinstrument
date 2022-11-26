<script>
    import Button from "./Button.svelte";

    export let key;
    export let textColor;
    export let url;
    export let name;
    export let color;

    let audioFile = new Audio(url);
    let isPlaying = false;
    let togglesound = (event) => {
            audioFile.play();
        
    };
</script>

<div>
    <p style=" color: {textColor}">{name}</p>
    <Button {color} on:click={togglesound} />
</div>

<style>
    p {
        font-family: "Open Sans Condensed";
        font-weight: bold;
    }
</style>
