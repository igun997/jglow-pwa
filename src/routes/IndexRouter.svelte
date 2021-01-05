<script>
    import { Router, Link, Route } from "svelte-routing";
    import IndexIntro from "./intro/Index.svelte"
    import IndexLogin from "./intro/Login.svelte"
    import IndexRegister from "./intro/Register.svelte"
    import IndexForget from "./intro/Forget.svelte"
    export let url = "";
</script>
<Router url="{url}">
    <Route path="/" component="{IndexIntro}" />
    <Route path="/login" component="{IndexLogin}" />
    <Route path="/register" component="{IndexRegister}" />
    <Route path="/forget" component="{IndexForget}" />
    <Route path="/*" component="{IndexIntro}" />
</Router>
