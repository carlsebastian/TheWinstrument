<script>
    import MusicButton from "./MusicButton.svelte";
    import * as instrumentList from '../../public/available_sounds.json'
    //let state = { instruments: [], instrumentList: [], indexSound: 0 };
    var colors = [
        "brown",
        "red",
        "darkSalmon",
        "pink",
        "orange",
        "yellow",
        "yellowgreen",
        "green",
        "lightblue",
        "blue",
        "purple",
        "indigo",
    ];
    var sounds = instrumentList.sounds[0].sounds;
    console.log(sounds);
</script>

<div>
    <h1>Orderrrrr Piano</h1>
    <div class="loop">
        {#each sounds as sound, index}
        <MusicButton
            key={sound.soundName + index}
            name={sound.soundName}
            color={colors[index]}
            textColor={colors[index]}
            url={"https://clever-platypus-047c9d.netlify.app/" + sound.src}
        />
        {/each}
    </div>
</div>

<style>
    .loop {
        display: flex;
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        justify-content: center;
    }

    h1 {
        color: #169bab;
        font-family: "Open Sans Condensed";
        font-size: xxx-large;
        text-decoration: underline;
    }
</style>
