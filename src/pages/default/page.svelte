<script>

import Logo from './components/Logo.svelte';

</script>

<div class="default">
    Default Page

    <Logo />
</div>

<style>

.default
{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

:global(.logo)
{
    margin-top: 30px;
}

</style>
