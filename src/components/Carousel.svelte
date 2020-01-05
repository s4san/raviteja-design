<div>
    <img src="ldq.svg" alt="Open quote">
    <slot></slot>
    <img src="rdq.svg" alt="End quote">
</div>
<style>
    img {
        align-self: flex-start;
    }
    img:first-child {
        margin-right: 2.5rem;
    }
    img:last-child {
        margin-left: 2.5rem;
    }
    div {
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>
