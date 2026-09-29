<script>
    import GetQuoteButton from "$lib/components/hero/GetQuoteButton.svelte";
    import Icons from "./Icons.svelte";
</script>

<div class="grid grid-cols-4 bg-[#424242] text-white py-6 px-10 items-center">
    <div class="flex items-center col-span-1" id="email">
        <p class="absolute justify-center ">infoyoursite@mail.com</p>
    </div>
    <div class="flex items-center col-span-1" id="telefoonnummer">
        <p>+31 6 12345678</p>
    </div>
    <div>
        <Icons />
    </div>
    <div>
        <GetQuoteButton />
    </div>
</div>