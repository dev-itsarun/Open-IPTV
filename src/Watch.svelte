<script>
  import Navbar from "./navbar.svelte";
  import { onMount } from "svelte";
  const endpoint = "https://iptv-org.github.io/api/streams.json";
  let posts = [];

  onMount(async function () {
    const response = await fetch(endpoint);
    const data = await response.json();
    posts = data;
  });
  
  function sliceit(t1) {
    return t1.slice(0, -3);
  }

  export let location = null;

</script>

<Navbar />
<main class="container pt-5">

  <section class="py-5">
    <div class="container px-5">
        <h1 class="fw-bolder fs-5 mb-4">Channels : </h1>
        <div class="card border-0 shadow rounded-3 overflow-hidden">
            <div class="card-body p-0">
                
                {#each posts as channels}
                <div class="row">
                    <div class="col-lg-12">
                        <div class="p-4 p-md-5">
                            <div class="h2 fw-bolder">{sliceit(channels.channel)}</div>
                            <p>M3u8 Link For VLC : </p>
                            <input value="{channels.url}" class="form-control"/> 
                            <br><br>
                            <a href="intent:{channels.url}#Intent;package=com.mxtech.videoplayer.ad;S.title={channels.channel};b.decode_mode=4;end"
                            class="btn btn-primary" >
                                <i class="bi bi-play-circle"></i> Watch In MxPlayer
                            </a>
                        </div>
                    </div>
                </div>
                <hr>
                {/each}

            </div>
        </div>
    </div>
</section>
</main>
