<script>
    export let name, title, content;
</script>
<div>
    <h4>
        <strong>{name},</strong> {title}
    </h4>
    <p>
        {content}
    </p>
</div>
<style>
    div {
        max-width: 40rem;
    }
    h4 {
        font-size: 1.125rem;
    }
    p {
        font-size: 1rem;
    }
</style>
