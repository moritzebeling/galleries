<script>

	import { onMount } from "svelte";
	import Swipe from "swipejs";

    import {images} from './images.js';

	let index = 0;
	let container;
    let swipeGallery;

	onMount(() => {

        swipeGallery = new Swipe(container, {
            draggable: true,
            continuous: true,
            slidesPerColumn: 2,
            callback: function(i, element) {
				index = i;
            }
        });

    });

</script>

<div class="swipe" bind:this={container}>
	<div class="swipe-wrap">
		{#each images as image, i}
			<div class="swipe-item width-{image.width}">

                <figure>
				    <img src="{image.url}" alt="Schmott" />
                </figure>

				<button title="Previous image" class="prev" on:click={swipeGallery.prev} />
				<button title="Next image" class="next" on:click={swipeGallery.next} />

			</div>
		{/each}
	</div>
</div>

<style lang="scss">

	.swipe {
        overflow: hidden;
        visibility: hidden;
        position: relative;
        height: 100%;
        width: 100%;
    }
    .swipe-wrap {
        overflow: hidden;
        position: relative;
        height: 100%;
    }
	.swipe-item {
        position: relative;
        height: 100%;
        width: 50%;
        float: left;
        &.width-1 {
            width: 50vw;
        }
        &.width-2 {
            width: 100vw;
        }
    }

	button {
        position: absolute;
        top: 0;
        width: 50%;
        height: 100%;
        z-index: 5;
        &.prev {
            left: 0;
            cursor: w-resize;
        }
        &.next {
            left: 50%;
            cursor: e-resize;
        }
    }

    figure {
        padding: 0.5rem;
        height: 100vh;
        img {
            display: block;
            width: 100%;
            height: 100%;
            object-fit: contain;
            object-position: center;
        }
    }

</style>
