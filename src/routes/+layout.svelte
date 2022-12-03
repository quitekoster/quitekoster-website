<script>
    import '../app.css';
    import Navigation from '../sections/navigation/navigation.svelte';
</script>

<Navigation />
<div class="mx-auto max-w-screen-xl px-4 md:px-6 py-2.5">
    <slot />
</div>