<script>
    let currentSlide = $state(1);
    let totalSlides = 2;
    let instant = $state(false);

    function nextSlide() {
        currentSlide += 1;
        if (currentSlide > totalSlides + 1) {
            currentSlide = 1;
            instant = true;
        }
    }

    function prevSlide() {
        currentSlide -= 1;
        if (currentSlide < 0) {
            currentSlide = totalSlides;
            instant = true;
        }
    }

    $effect(() => {
        if (!instant) return;
        let inner = 0;
        const outer = requestAnimationFrame(() => {
            inner = requestAnimationFrame(() => {
                instant = false;
            });
        });
        return () => {
            cancelAnimationFrame(outer);
            cancelAnimationFrame(inner);
        };
    });
</script>

<div id="slider" class="relative h-screen overflow-hidden">
    <div class="flex transition-transform duration-500 ease-in-out"
         class:transition-none={instant}
         style="transform: translateX(-{currentSlide * 100}%)">
        <div class="flex-[0_0_100%] h-screen bg-[url('/money.png')] bg-cover bg-center grid grid-cols-1 sm:grid-cols-[auto_auto] justify-start content-center gap-4 sm:gap-6 lg:gap-8 px-6 sm:px-8 lg:px-[10%]">
            <h1 class="col-span-1 sm:col-span-2 w-fit min-w-0 text-2xl sm:text-3xl font-extrabold uppercase text-white bg-[#2b64f0] px-4 py-3 sm:px-5 lg:text-4xl">Welcome to Our Cmpany</h1>
            <h2 class="col-span-1 sm:col-span-2 w-fit min-w-0 text-sm sm:text-base font-bold text-white bg-black px-4 py-3 sm:px-5 lg:text-xl">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</h2>
            <button class="shrink-0 border border-white text-white uppercase text-xs sm:text-sm font-bold tracking-wider px-5 py-3 sm:px-8 sm:py-4 lg:px-10 lg:py-4 hover:bg-white hover:text-black transition-colors">SERVICES</button>
            <button class="shrink-0 border border-white text-white uppercase text-xs sm:text-sm font-bold tracking-wider px-5 py-3 sm:px-8 sm:py-4 lg:px-10 lg:py-4 hover:bg-white hover:text-black transition-colors">READ MORE</button>
        </div>
        <div class="flex-[0_0_100%] h-screen bg-[url('/computer.jpg')] bg-cover bg-center grid grid-cols-1 sm:grid-cols-[auto_auto] justify-start content-center gap-4 sm:gap-6 lg:gap-8 px-6 sm:px-8 lg:px-[10%]">
            <h1 class="col-span-1 sm:col-span-2 w-fit min-w-0 text-2xl sm:text-3xl font-extrabold uppercase text-white bg-[#2b64f0] px-4 py-3 sm:px-5 lg:text-4xl">Business YOUR SATISFICTION</h1>
            <h2 class="col-span-1 sm:col-span-2 w-fit min-w-0 text-sm sm:text-base font-bold text-white bg-black px-4 py-3 sm:px-5 lg:text-xl">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</h2>
            <button class="shrink-0 border border-white text-white uppercase text-xs sm:text-sm font-bold tracking-wider px-5 py-3 sm:px-8 sm:py-4 lg:px-10 lg:py-4 hover:bg-white hover:text-black transition-colors">LOGIN</button>
            <button class="shrink-0 border border-white text-white uppercase text-xs sm:text-sm font-bold tracking-wider px-5 py-3 sm:px-8 sm:py-4 lg:px-10 lg:py-4 hover:bg-white hover:text-black transition-colors">REGISTER</button>
        </div>
        <div class="flex-[0_0_100%] h-screen bg-[url('/money.png')] bg-cover bg-center grid grid-cols-1 sm:grid-cols-[auto_auto] justify-start content-center gap-4 sm:gap-6 lg:gap-8 px-6 sm:px-8 lg:px-[10%]">
            <h1 class="col-span-1 sm:col-span-2 w-fit min-w-0 text-2xl sm:text-3xl font-extrabold uppercase text-white bg-[#2b64f0] px-4 py-3 sm:px-5 lg:text-4xl">Welcome to Our Cmpany</h1>
            <h2 class="col-span-1 sm:col-span-2 w-fit min-w-0 text-sm sm:text-base font-bold text-white bg-black px-4 py-3 sm:px-5 lg:text-xl">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</h2>
            <button class="shrink-0 border border-white text-white uppercase text-xs sm:text-sm font-bold tracking-wider px-5 py-3 sm:px-8 sm:py-4 lg:px-10 lg:py-4 hover:bg-white hover:text-black transition-colors">SERVICES</button>
            <button class="shrink-0 border border-white text-white uppercase text-xs sm:text-sm font-bold tracking-wider px-5 py-3 sm:px-8 sm:py-4 lg:px-10 lg:py-4 hover:bg-white hover:text-black transition-colors">READ MORE</button>
        </div>
        <div class="flex-[0_0_100%] h-screen bg-[url('/computer.jpg')] bg-cover bg-center grid grid-cols-1 sm:grid-cols-[auto_auto] justify-start content-center gap-4 sm:gap-6 lg:gap-8 px-6 sm:px-8 lg:px-[10%]">
            <h1 class="col-span-1 sm:col-span-2 w-fit min-w-0 text-2xl sm:text-3xl font-extrabold uppercase text-white bg-[#2b64f0] px-4 py-3 sm:px-5 lg:text-4xl">Business YOUR SATISFICTION</h1>
            <h2 class="col-span-1 sm:col-span-2 w-fit min-w-0 text-sm sm:text-base font-bold text-white bg-black px-4 py-3 sm:px-5 lg:text-xl">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</h2>
            <button class="shrink-0 border border-white text-white uppercase text-xs sm:text-sm font-bold tracking-wider px-5 py-3 sm:px-8 sm:py-4 lg:px-10 lg:py-4 hover:bg-white hover:text-black transition-colors">LOGIN</button>
            <button class="shrink-0 border border-white text-white uppercase text-xs sm:text-sm font-bold tracking-wider px-5 py-3 sm:px-8 sm:py-4 lg:px-10 lg:py-4 hover:bg-white hover:text-black transition-colors">REGISTER</button>
        </div>
    </div>
    <button onclick={prevSlide}
            class="absolute left-0 top-1/2 -translate-y-1/2 z-10 w-10 h-10 grid place-items-center bg-black text-white text-xl sm:w-14 sm:h-14 sm:text-2xl font-bold">
        &lt;
    </button>
    <button onclick={nextSlide}
            class="absolute right-0 top-1/2 -translate-y-1/2 z-10 w-10 h-10 grid place-items-center bg-black text-white text-xl sm:w-14 sm:h-14 sm:text-2xl font-bold">
        &gt;
    </button>
</div>