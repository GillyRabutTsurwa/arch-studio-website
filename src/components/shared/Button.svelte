<button>
    <slot name="text">See Our Portfolio &rarr;</slot>
</button>

<style>
    button {
        cursor: pointer;
        display: inline-block;
        outline: none;
        border: none;
        padding: 2rem 3.5rem;
        background-color: #333;
        color: #eee;
    }

    .btn-footer {
        align-self: center;
        transform: translateX(-5rem);
    }
</style>