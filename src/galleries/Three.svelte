<script>

    import {images} from './images.js';

    let s = 0;
    function side( w ){
        s += w;
        return s % 2 === 0 ? 'right' : 'left';
    }

</script>

<div class="cols-1">
    <figure>
        <img alt="Schmott" src="https://ik.imagekit.io/j7cyz1dg5lc/portfolio/gigi-studios/gigi-short.jpg?tr=w-1280" />
    </figure>
</div>

<div class="cols-2">
    <div class="col left">
        <figure>
            <img alt="Schmott" src="https://ik.imagekit.io/j7cyz1dg5lc/portfolio/gigi-studios/gigi-barcelona-still-life-campaign-2018-captured-by-schmott-001.jpg?tr=w-1280" />
        </figure>
        <figure>
            <img alt="Schmott" src="https://ik.imagekit.io/j7cyz1dg5lc/portfolio/gigi-studios/gigi-barcelona-still-life-campaign-2018-captured-by-schmott-005.jpg?tr=w-1280" />
        </figure>
    </div>
    <div class="col right">
        <figure>
            <img alt="Schmott" src="https://ik.imagekit.io/j7cyz1dg5lc/portfolio/gigi-studios/gigi-barcelona-still-life-campaign-2018-captured-by-schmott-002.jpg?tr=w-1280" />
        </figure>
        <figure>
            <img alt="Schmott" src="https://ik.imagekit.io/j7cyz1dg5lc/portfolio/gigi-studios/gigi-barcelona-still-life-campaign-2018-captured-by-schmott-006.jpg?tr=w-1280" />
        </figure>
    </div>
</div>

<div class="cols-1">
    <figure>
        <img alt="Schmott" src="https://ik.imagekit.io/j7cyz1dg5lc/portfolio/gigi-studios/gigi-barcelona-still-life-campaign-2018-captured-by-schmott-008.jpg?tr=w-1280" />
    </figure>
</div>

<div class="cols-2 padding-bottom">
    <div class="col left">
        <figure>
            <img alt="Schmott" src="https://ik.imagekit.io/j7cyz1dg5lc/portfolio/gigi-studios/gigi-studios-captured-by-schmott-001.jpg?tr=w-1280" />
        </figure>
        <figure>
            <img alt="Schmott" src="https://ik.imagekit.io/j7cyz1dg5lc/portfolio/gigi-studios/gigi-barcelona-still-life-campaign-2018-captured-by-schmott-005.jpg?tr=w-1280" />
        </figure>
    </div>
    <div class="col right">
        <figure>
            <img alt="Schmott" src="https://ik.imagekit.io/j7cyz1dg5lc/portfolio/gigi-studios/gigi-studios-captured-by-schmott-003.jpg?tr=w-1280" />
        </figure>
        <figure>
            <img alt="Schmott" src="https://ik.imagekit.io/j7cyz1dg5lc/portfolio/gigi-studios/gigi-studios-captured-by-schmott-005.jpg?tr=w-1280" />
        </figure>
    </div>
</div>

<style lang="scss">

    .cols-1 {
        padding: 0.5rem;
        padding-bottom: 0;
    }
    .cols-2 {
        display: flex;
        flex-wrap: wrap;
        padding: 0.25rem;
        padding-bottom: 0;
        .col {
            flex: 1 1 50%;
            padding: 0.25rem;
            padding-bottom: 0;
            figure {
                height: 200vh;
            }
            figure + figure {
                margin-top: 0.5rem;
            }
            img {
                display: block;
                position: sticky;
                top: 0.5rem;
            }
        }
    }
    .padding-bottom {
        padding-bottom: 0.5rem;
    }
    .col.right {
        padding-top: 100vh;
        figure:last-child {
            height: 100vh;
        }
    }

</style>
