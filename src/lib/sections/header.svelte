<script lang="ts">
    import { ArrowDownIcon } from 'svelte-feather-icons'
</script>

<header>
    <div class="wrapper">
        <h1>Zunami</h1>
        <a href='#about' id='arrow'>
            <ArrowDownIcon size="48"/>
        </a>
    </div>
</header>

<style lang="scss">
    @use './src/styles/variables.scss';

    header {
        .wrapper {
            min-height: 60vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            gap: 10px;
            h1 {
                font-size: 72px;
            }
            #arrow {
                background: variables.$primary;
                box-shadow: 0px 4px 4px rgba(0, 153, 255, 0.4);
                color: white;
                height: 64px;
                width: 64px;
                border-radius: 100%;
                display: flex;
                align-items: center;
                justify-content: center;
            }
            
        }

    }

</style>