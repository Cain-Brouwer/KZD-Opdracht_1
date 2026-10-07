<script>
    let currentSlide = 0;
    let totalSlides = 2;

    function nextSlide() {
        currentSlide = (currentSlide + 1) % totalSlides;
    }

    function prevSlide() {
        currentSlide = (currentSlide - 1 + totalSlides) % totalSlides;
    }
</script>

<div id="slider" class="relative h-screen overflow-hidden">
    <div class="flex transition-transform duration-500 ease-in-out"
         style="transform: translateX(-{currentSlide * 100}%)">
        <div class="flex-[0_0_100%] h-screen bg-[url('/computer.jpg')] bg-cover bg-center"></div>
        <div class="flex-[0_0_100%] h-screen bg-[url('/money.png')] bg-cover bg-center"></div>
    </div>
    <button on:click={prevSlide}
            class="absolute left-4 top-1/2 -translate-y-1/2  z-10 w-12 h-12 flex items-center justify-center bg-black text-white text-2xl text-bold">
        &lt;
    </button>
    <button on:click={nextSlide}
            class="absolute right-4 top-1/2 -translate-y-1/2 z-10 w-12 h-12 flex items-center justify-center bg-black text-white text-2xl text-bold">
        &gt;
    </button>
</div>