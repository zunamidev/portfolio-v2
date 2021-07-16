<script lang="ts">
    export let name = "";
    export let language = "";
    export let url = "";
</script>
<a href={url}>
    <div class="project">
        <h3>{name}</h3>
        <span>
            <i class="devicon-{language ? language.toLocaleLowerCase() : ''}-plain"></i>
        </span>
    </div>
</a>
<style lang="scss">

a {
    text-decoration: none;
    color: white;
    .project {
        height: 25vh;
        width: 30vw;
        background: grey;
        border-radius: 20px;
        padding: 12px 17px;
    }

    i {
        font-size: 36px;
    }
}
</style>