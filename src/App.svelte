<script>
    import { Router, Link, Route } from "svelte-routing";
    import IndexRouter from "./routes/IndexRouter.svelte"
    import Preload from "./components/Preload.svelte"
    import {onMount} from "svelte";
    let ready = false;
    let timer = 1000
    onMount(()=>{
        ready = true;
    })
    export let url = "";
</script>
<Preload {timer}/>
<Router url="{url}">
    <Route path="/*url" component="{IndexRouter}" />
</Router>
