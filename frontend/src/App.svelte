<script>
  import logo from './assets/images/logo.svg'
  import Tify from 'tify'
  import 'tify/dist/tify.css'
  let manifestUrl = "Please enter the IIIF manifest URL 👇"
  let name;
  let demoManifest = 'https://manifests.sub.uni-goettingen.de/iiif/presentation/PPN578154684/manifest'

  function showManifest() {
    new Tify({
      container: '#app',
      manifestUrl: name,
    })
  }

  function demo() {
    name = demoManifest;
    showManifest()
  }
</script>

<main>
    <img alt="TIFY Logo" id="logo" src="{logo}">
    <div class="result" id="result">{manifestUrl}</div>
    <div class="input-box" id="input">
        <input autocomplete="off" bind:value={name} class="input" id="name" type="text" placeholder="{demoManifest}"/>
        <button class="btn" on:click={showManifest}>Show</button>
    </div>
    <div class="hint">
        <p>If you just want to try, <a href="#" on:click="{demo}">click here</a></p>
    </div>
</main>

<style>

    #logo {
        display: block;
        width: 50%;
        height: 50%;
        margin: auto;
        padding: 10% 0 0;
        background-position: center;
        background-repeat: no-repeat;
        background-size: 100% 100%;
        background-origin: content-box;
    }

    .result {
        height: 20px;
        line-height: 20px;
        margin: 1.5rem auto;
    }

    .input-box .btn {
        width: 60px;
        height: 30px;
        line-height: 30px;
        border-radius: 3px;
        border: none;
        margin: 0 0 0 20px;
        padding: 0 8px;
        cursor: pointer;
    }

    .input-box .btn:hover {
        background-image: linear-gradient(to top, #cfd9df 0%, #e2ebf0 100%);
        color: #333333;
    }

    .input-box .input {
        width: 400px;
        border: none;
        border-radius: 3px;
        outline: none;
        height: 30px;
        line-height: 30px;
        padding: 0 10px;
        background-color: rgba(240, 240, 240, 1);
        -webkit-font-smoothing: antialiased;
    }

    .input-box .input:hover {
        border: none;
        background-color: rgba(255, 255, 255, 1);
    }

    .input-box .input:focus {
        border: none;
        background-color: rgba(255, 255, 255, 1);
    }

</style>
