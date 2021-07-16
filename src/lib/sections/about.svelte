<script lang="ts">
// import Developer from '$lib/developer.svelte'
import Developer from '$lib/components/developer.svelte'
</script>
<section id="about">
    <div class="container">
        <h1>About me</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores odio consequatur accusantium quidem, commodi fugiat explicabo delectus repellendus animi aliquid officiis numquam quae et tenetur optio inventore, expedita, molestias velit.
        Illum commodi tenetur ratione laudantium cupiditate porro doloremque, fuga alias necessitatibus laboriosam culpa eius vitae similique ad? Vel exercitationem minus esse quasi. Mollitia velit totam dicta officia neque repellat est!
        Molestiae id inventore fugit exercitationem est sunt, assumenda quaerat neque enim sequi, quidem doloribus facere accusamus illo repellat sit maxime commodi cupiditate expedita eveniet atque. Ex facere iure fugiat nulla?
        Rerum aspernatur aperiam autem, nulla ipsum repellendus odit voluptatibus esse illo, molestias quam voluptatum! Dignissimos quaerat vel a suscipit sint officia, quae voluptatum fuga blanditiis temporibus distinctio adipisci, voluptatibus ab?
        Nemo at porro amet ullam odio accusantium. Aspernatur atque aliquam quibusdam fugit alias ipsam saepe, ex maxime repellendus harum aut doloribus veniam, id iste totam distinctio minima quam autem eius.
    </p>
    
    </div>
    <div id="image">
        <Developer></Developer>
    </div>
</section>
<style lang="scss">
    @use './src/styles/variables.scss';

    section {
        background-color: variables.$primary;
        display: grid; 
        grid-gap: 10px;
        grid-template-columns: 1fr 1fr;

        .container {
            color: white;
        }
        #image {
            position: relative;
            bottom: 6.4vh;
        }
    }
</style>