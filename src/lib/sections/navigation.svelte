<script lang="ts">
    import { MenuIcon } from 'svelte-feather-icons'

    let navigation = [{name: 'Home', href: '#home'}, {name: 'About', href: '#about'}]
    let isActive = false;
</script>

<nav>
    <div id='mobile' on:click="{() => { isActive = !isActive }}">
        <MenuIcon size="36"></MenuIcon>
    </div>
    <ul id="{ isActive ?'active': 'deactive'}">
        {#each navigation as { name, href }, i}
        <li><a href="{href}" id={`${i}`}>{name}</a></li>
        {/each}
    </ul>
</nav>
<style lang="scss">
    @use './src/styles/variables.scss';

    #active {
        display: block;
    }

    #deactive {
        display: none;
    }

    nav {
        #mobile {
            display: none;
        }
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
    
    @media screen and (max-width: 768px) {
        nav {
            #mobile {
                display: block;
            }
            width: initial;
            left: 70%;
            color: white;
            #desktop {
                display:none;
            }  
            &:hover {
                background: variables.$primary;
            } 
        }
    }
</style>