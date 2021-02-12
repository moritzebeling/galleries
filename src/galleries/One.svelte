<script>

    import {images} from './images.js';

</script>

<div>

    {#each images as image}
        <figure class="width-{image.width}">
            <img alt="Schmott" src="{image.url}" />
        </figure>
    {/each}

</div>

<style lang="scss">

    div {
        display: flex;
        flex-wrap: wrap;
        padding: 0.2rem;
        .width-1 {
            flex: 1 1 50%;
        }
        .width-2 {
            flex: 1 1 100%;
        }
    }

    figure {
        padding: 0.2rem;
    }

</style>
