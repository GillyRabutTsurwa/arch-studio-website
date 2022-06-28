<script>
    import cardOne from "../static/image-del-sol.jpg";
    import cardTwo from "../static/image-228b.jpg";
    import cardThree from "../static/image-prototype.jpg";

</script>

<div class="featured">
    <div class="featured__title">
        <h4>Featured</h4>
        <button>See All &rarr;</button>
    </div>
    <div class="featured__cards">
        <div class="card-1"></div>
        <div class="card-2"></div>
        <div class="card-3"></div>
    </div>
</div>

<style>
    .featured {
        margin-bottom: 15rem;
    }
    
    .featured__title {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .featured__cards {
        height: 65vh;
        display: grid;
        grid-template-columns: repeat(3, 50rem);
        column-gap: 4rem;
    }

    .card-1,
    .card-2,
    .card-3 {
        background-repeat: no-repeat;
        background-size: cover;
    }

    .card-1 {
        background-image: url(../static/image-del-sol.jpg)
    }

    .card-2 {
        background-image: url(../static/image-228b.jpg)

    }

    .card-3 {
        background-image: url(../static/image-prototype.jpg)

    }
</style>
