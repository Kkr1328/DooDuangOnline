<script>
    import Button, { Label }  from '@smui/button';
    import ImageList, {
        Item,
        ImageAspectContainer,
        Image,
        Supporting,
    } from '@smui/image-list';

    async function download(){
        
    }
</script>

<style>
    main {
        text-align: center;
        padding: 1em;
        margin: 0 auto;
    }

    h1 {
      color: #ff3e00;
      text-transform: uppercase;
      font-size: 4em;
      font-weight: 100;
    }
</style>


<main>
    <h1>
        Download image
    </h1>
    <div>
        <Image
            alt="Page content placeholder"
            src="pic/page-content.jpg"
            style="display: block; max-width: 480px; height: auto; margin: 1em auto;"
        />
    </div>
    <Button on:click={download}>
        <Label>
            Download
        </Label>
    </Button>
</main>
