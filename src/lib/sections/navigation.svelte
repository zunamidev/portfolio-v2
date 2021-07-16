<script lang="ts">
    let navigation = [{name: 'Home', href: '#home'}, {name: 'About', href: '#about'}]
</script>

<nav>
    <ul>
        {#each navigation as { name, href }, i}
        <li><a href="{href}" id={`${i}`}>{name}</a></li>
        {/each}
    </ul>
</nav>
<style lang="scss">
    @use './src/styles/variables.scss';

    nav {
        z-index: 9999;
        background: variables.$secondary;
        width: 30vw;
        padding: 15px;
        border-radius: 0 0 25px 25px;
        position: fixed;
        left: 60%;
        ul {
            display: flex;
            flex-direction: row;
            li {
                list-style: none;
                display: block;
                padding: 12px;
                a {
                    color: white;
                    text-decoration: none;
                }
            }
        }
    }
</style>