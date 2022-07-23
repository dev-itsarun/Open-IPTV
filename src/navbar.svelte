<script>
	import { Router, Link, Route } from "svelte-routing";
</script>
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container px-5">
      <Link class="navbar-brand" to="/">Open Iptv</Link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-icon"></span></button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
              <li class="nav-item"><Link class="nav-link" to="/">Home</Link></li>
              <li class="nav-item"><Link class="nav-link" to="/Watch">Watch Now</Link></li>
          </ul>
      </div>
  </div>
</nav>