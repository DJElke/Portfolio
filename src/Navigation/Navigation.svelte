<script context="module">
    import Home from '../Components/Index.svelte';
    import About from '../Components/About.svelte';
    import Skills from '../Components/Skills.svelte';
    import Projects from '../Components/Projects.svelte';
    import Contact from '../Components/Contact.svelte';

    export const navOptions = [
        {page: "EDJ", component: Home},
        {page: "Contact", component: Contact},
        {page: "Projects", component: Projects},
        {page: "Skills", component: Skills},
        {page: "About", component: About}
    ];
</script>