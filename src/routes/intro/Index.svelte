<script>
    import { link } from "svelte-routing";
</script>
<div class="intro-wrapper d-flex align-items-center justify-content-center text-center">
    <!-- Background Shape-->
    <div class="background-shape"></div>
    <div class="container"><img class="big-logo" src="{ps.env.LOGO_APP}" alt=""></div>
</div>
<div class="get-started-btn"><a class="btn btn-success btn-lg w-100" href="/login" use:link>Masuk</a></div>
