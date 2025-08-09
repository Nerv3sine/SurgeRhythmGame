<script lang="ts">
    import './rhythmBackground.css'
    import './rhythmGame.css'

    // order of which elements should appear, from back -> front
    const backgrounds : string[] = [
        'skydetail', 
        'hit effects',
        'sun1',
        'pillar3',
        'cloud6',
        'pillar2',
        'cloud5',
        'cloud4',
        'cloud3',
        'sun2',
        'cloud2',
        'pillar1',
        'cloud1'
    ];

    const backgroundLoopDuration:number = 120;
    const animationSpeedDifferenceFactor: number = 5;
    const imgType:string = 'svg';

</script>

<div id="rhythmGame">
    <div id="rhythmBg" class="rhythmBg">
        {#each backgrounds as bg, idx}
            <div 
                class="rhythmBg movingBg"
                style="
                    background-image: url(/{bg}.{imgType});
                    animation: scroll {backgroundLoopDuration - idx * animationSpeedDifferenceFactor}s linear infinite;"
            ></div>
        {/each}
    </div>
    <div class="note">

    </div>
</div>