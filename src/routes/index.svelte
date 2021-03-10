<script>
    import {Link,Router,Route} from  "svelte-routing"
    import App from "../App.svelte"
    export let url=""
</script>
<Router url="{url}">
    <Route path="/index" component="{App}"/>
    <Route path="/" component="{App}"/>
</Router>
