<script>
    export let color = "light";
</script>

<h2 class={color}>
    <!-- <slot name="text"></slot> -->
    <slot></slot>
</h2>

<style>
    h2 {
        font-size: 7rem;
        margin-bottom: 2.5rem;
    }

    .light {
        color: #EEEFF4;
    }

    .dark {
        color: #1B1D23;
    }
</style>

