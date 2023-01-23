<script>
    import Textfield from '@smui/textfield';
    import Icon from '@smui/textfield/icon';
    import HelperText from '@smui/textfield/helper-text';
  
    let name = '';
    let surname = '';
    let birthdate = '';
</script>

<style>
  h1 {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  .user_form {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

</style>

<h1>
  Fill information
</h1>
<div class="user_form">
  <div>
    <Textfield bind:value={name} label="Name">
      <HelperText slot="helper">Helper Text</HelperText>
    </Textfield>
 
    <pre class="status">Value: {name}</pre>
  </div>
  <div>
    <Textfield bind:value={surname} label="Surname">
      <HelperText slot="helper">Helper Text</HelperText>
    </Textfield>
 
    <pre class="status">Value: {surname}</pre>
  </div>
  <div>
    <Textfield bind:value={birthdate} label="Birth Date">
      <HelperText slot="helper">Helper Text</HelperText>
    </Textfield>
 
    <pre class="status">Value: {birthdate}</pre>
  </div>
</div>