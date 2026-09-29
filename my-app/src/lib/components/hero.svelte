<script>
    import { onMount } from 'svelte';

    let opacity = 1;

    onMount(() => {
        function veranderOpacity() {
            const fadeStart = 50;
            const fadeLengte = 150;

            opacity = Math.max(
                0,
                1 - (window.scrollY - fadeStart) / fadeLengte
            );
        }

        window.addEventListener('scroll', veranderOpacity);
        veranderOpacity();

        return () => window.removeEventListener('scroll', veranderOpacity);
    });
</script>

<div class="sticky top-0 z-20 grid grid-cols-4 bg-[#424242] text-white py-6 px-10 items-center" style="opacity: {opacity};">
    <div class="flex items-center col-span-1" id="email">
        <p class="absolute justify-center ">infoyoursite@mail.com</p>
    </div>
    <div class="flex items-center col-span-1" id="telefoonnummer">
        <p>+31 6 12345678</p>
    </div>
    <div class="flex items-center col-span-1">
        <ol class="m-0">
            <li class="inline-block" id="facebook">
                <a href="https://www.facebook.com" target="_blank" rel="noopener noreferrer"><img src="/facebook.png" alt="facebook"></a>
            </li>
            <li class="inline-block" id="google">
                <a href="https://www.google.com/" target="_blank" rel="noopener noreferrer"><img src="/google.png" alt="google"></a>
            </li>
            <li class="inline-block" id="linkedin">
                <a href="https://www.linkedin.com" target="_blank" rel="noopener noreferrer"><img src="/linkedin.png" alt="linkedin"></a>
            </li>
        </ol>
    </div>
    <div class="col-span-1 flex items-center justify-end">
        <button class="bg-blue-600 hover:bg-cyan-700 text-white font-bold py-2 px-4 rounded-full mr-10">
            <a href="/quote" target="_blank" rel="noopener noreferrer">Get a Quote >></a>
        </button>
    </div>
</div>