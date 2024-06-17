<!-- svelte-ignore a11y-no-noninteractive-tabindex -->
<!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
<!-- svelte-ignore a11y-click-events-have-key-events -->
<script>
    import Logo from "$lib/assets/Logo.png";
    import Bm from "$lib/assets/Burgermenu.png";
    import Close from "$lib/assets/close.png"

    let show = false;

    function handleClick() {
        show = !show;
    }
</script>

<header class="flex justify-center items-center">
    <nav class="">
        <div class="flex items-center gap-5">
            <a class="text-xl hidden lg:block" href="/">Hvem er vi?</a>

            <a class="text-xl hidden lg:block" href="/">Kontakt os</a>

            <img class="mx-10 w-64 lg:w-[300px]" src={Logo} alt="" />

            <a class="text-xl hidden lg:block" href="/">Bogføring & regnskab</a>

            <a class="text-xl hidden lg:block" href="/">FAQ</a>
        </div>
    </nav>

    <div class="flex flex-col lg:hidden">
        <img
            src={Bm}
            on:click={handleClick}
            class="invert w-12 cursor-pointer rotate-180"
            alt=""
        />
        <div
            class="menu w-[150px] h-[150px] bg-white rounded-2xl absolute top-44 right-[205px]"
            class:show
        ></div>
    </div>
</header>

<style lang="postcss">
    li > a,
    li {
        font-family: "Source Code Pro", monospace;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
    }

    li > a:hover {
        text-decoration: underline;
    }

    .show {
        display: none;
    }
</style>
