<script>
  import Tab, { Label } from '@smui/tab';
  import TabBar from '@smui/tab-bar';

  import MyForm from './routes/Form.svelte';
  import MyDownload from './routes/Download.svelte';
  import MyGif from './routes/Gif.svelte';

  export let name;
  let active = 'Home';
</script>

<style>

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<!-- Material Icons -->
<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/icon?family=Material+Icons"
/>
<!-- Roboto -->
<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,600,700"
/>
<!-- Roboto Mono -->
<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/css?family=Roboto+Mono"
/>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/svelte-material-ui@6.0.0/bare.min.css"
/>

<TabBar tabs={['Home', 'Form', 'Download']} let:tab bind:active>
    <Tab {tab}>
      <Label>{tab}</Label>
    </Tab>
</TabBar>

{#if active == 'Form' }
  <MyForm />
{:else if active == 'Download'}
  <MyDownload />
{:else }
  <main>
    <h1>Hello {name}!</h1>
    <MyGif />
  </main>
{/if}

