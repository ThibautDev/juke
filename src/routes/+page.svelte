<script>
    var music = {
        name: "Master of puppets",
        band: "Metalica"
    };

    let camelCaseString = music.name.replace(/\b\w/g, function(match, index) {
        return index === 0 ? match.toLowerCase() : match.toUpperCase();
    }).replace(/\s/g, '');

    var path = {
        cover: `/src/assets/covers/${camelCaseString}.png`,
        track: `/src/assets/track/${camelCaseString}.png`
    };
</script>

<section>

    <div id="bg-image" style="background-image: url({path.cover});">test</div>

    <div id="album" class="center">
        <img src={path.cover} alt="Album cover">
    </div>
    
    <div id="title" class="center">
        <span id="music">{music.name}</span>
        <span id="band">{music.band}</span>
        <!-- <audio controls autoplay>
            <source src="/src/assets/tracks/masterOfPuppets.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
        </audio> -->

        <a href="?test=Master_of_puppets&band=Metalica">test</a>
    </div>  


</section>

<style>
    @font-face {
        font-family: 'RussoOne';
        src: url('$lib/fonts/RussoOne-Regular.ttf'),
    }

    section {
        height: 100%;   
        position: relative; 
        overflow: hidden;
        border-radius: 5px;
    }

    .center {
        margin: auto;
        width: 50vh;
        padding-top: 7vh
    }

    #album > img{
        border-radius: 5px;
    }

    #title {
        text-align: center;
        display: flex;
        flex-direction: column;

        color: #FFFFFF;
        font-family: RussoOne;
    }
    #title > #music {
        font-size: 3em;
    }
    #title > #band {
        font-size: 1.5em;
        color: #CCCCCC;
        font-family: Arial, Helvetica, sans-serif;
    }
    #bg-image {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: -1;

        filter: blur(40px);

        background-size: cover;
    }

</style>