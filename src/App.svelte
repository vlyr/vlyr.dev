<script lang="ts">
    import {Route} from 'tinro'; 
    import Home from './pages/Home.svelte'; // <h1>Contacts</h1>
    import './app.css';
</script>

<Route path="/"><Home /></Route>
<Route path="/blog/*">
    <Route path="/">
        <h1>Blog Main</h1>
        <nav>
            <a href="/portfolio/sites">Sites</a> 
            <a href="/portfolio/photos">Photos</a>
        </nav>
    </Route>
    <Route path="/:post" let:meta><h1>Blog post: {meta.params.post}</h1></Route>
</Route>
