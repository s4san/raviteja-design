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
        width: 600px;
    }
    h4 {
        font-size: 18px;
    }
    p {
        font-size: 16px;
    }
</style>
