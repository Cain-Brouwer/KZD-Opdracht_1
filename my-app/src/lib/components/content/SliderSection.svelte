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
        <div class="flex-[0_0_100%] h-screen bg-[url('/money.png')] bg-cover bg-center grid grid-cols-[auto_auto] justify-start content-center gap-8 px-[10%]">
            <h1 class="col-span-2 w-fit min-w-0 text-4xl font-extrabold uppercase text-white bg-[#2b64f0] px-5 py-3">Welcome to Our Cmpany</h1>
            <h2 class="col-span-2 w-fit min-w-0 text-xl font-bold text-white bg-black px-5 py-3">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</h2>
            <button class="shrink-0 border border-white text-white uppercase text-sm font-bold tracking-wider px-10 py-4 hover:bg-white hover:text-black transition-colors">SERVICES</button>
            <button class="shrink-0 border border-white text-white uppercase text-sm font-bold tracking-wider px-10 py-4 hover:bg-white hover:text-black transition-colors">READ MORE</button>
        </div>
        <div class="flex-[0_0_100%] h-screen bg-[url('/computer.jpg')] bg-cover bg-center grid grid-cols-[auto_auto] justify-start content-center gap-8 px-[10%]">
            <h1 class="col-span-2 w-fit min-w-0 text-4xl font-extrabold uppercase text-white bg-[#2b64f0] px-5 py-3">Business YOUR SATISFICTION</h1>
            <h2 class="col-span-2 w-fit min-w-0 text-xl font-bold text-white bg-black px-5 py-3">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</h2>
            <button class="shrink-0 border border-white text-white uppercase text-sm font-bold tracking-wider px-10 py-4 hover:bg-white hover:text-black transition-colors">LOGIN</button>
            <button class="shrink-0 border border-white text-white uppercase text-sm font-bold tracking-wider px-10 py-4 hover:bg-white hover:text-black transition-colors">REGISTER</button>
        </div>
        <div class="flex-[0_0_100%] h-screen bg-[url('/money.png')] bg-cover bg-center grid grid-cols-[auto_auto] justify-start content-center gap-8 px-[10%]">
            <h1 class="col-span-2 w-fit min-w-0 text-4xl font-extrabold uppercase text-white bg-[#2b64f0] px-5 py-3">Welcome to Our Cmpany</h1>
            <h2 class="col-span-2 w-fit min-w-0 text-xl font-bold text-white bg-black px-5 py-3">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</h2>
            <button class="shrink-0 border border-white text-white uppercase text-sm font-bold tracking-wider px-10 py-4 hover:bg-white hover:text-black transition-colors">SERVICES</button>
            <button class="shrink-0 border border-white text-white uppercase text-sm font-bold tracking-wider px-10 py-4 hover:bg-white hover:text-black transition-colors">READ MORE</button>
        </div>
        <div class="flex-[0_0_100%] h-screen bg-[url('/computer.jpg')] bg-cover bg-center grid grid-cols-[auto_auto] justify-start content-center gap-8 px-[10%]">
            <h1 class="col-span-2 w-fit min-w-0 text-4xl font-extrabold uppercase text-white bg-[#2b64f0] px-5 py-3">Business YOUR SATISFICTION</h1>
            <h2 class="col-span-2 w-fit min-w-0 text-xl font-bold text-white bg-black px-5 py-3">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</h2>
            <button class="shrink-0 border border-white text-white uppercase text-sm font-bold tracking-wider px-10 py-4 hover:bg-white hover:text-black transition-colors">LOGIN</button>
            <button class="shrink-0 border border-white text-white uppercase text-sm font-bold tracking-wider px-10 py-4 hover:bg-white hover:text-black transition-colors">REGISTER</button>
        </div>
    </div>
    <button onclick={prevSlide}
            class="absolute left-0 top-1/2 -translate-y-1/2 z-10 w-14 h-14 grid place-items-center bg-black text-white text-2xl font-bold">
        &lt;
    </button>
    <button onclick={nextSlide}
            class="absolute right-0 top-1/2 -translate-y-1/2 z-10 w-14 h-14 grid place-items-center bg-black text-white text-2xl font-bold">
        &gt;
    </button>
</div>