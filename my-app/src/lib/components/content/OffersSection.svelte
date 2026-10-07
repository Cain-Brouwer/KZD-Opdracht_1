<script>
    const offers = [
        {
            icon: '/horse.png',
            title: 'Clean Modern Code',
            text: 'Phasellus enim libero, blandit vel sapien vitae, condimentum ultricies magna et. Quisque lobortis...'
        },
        {
            icon: '/bear.png',
            title: 'Design To Brag About',
            text: 'Phasellus enim libero, blandit vel sapien vitae, condimentum ultricies magna et. Quisque lobortis...'
        }
    ];
</script>

<section class="w-full flex flex-col lg:flex-row bg-white">
    <div class="w-full lg:w-1/2 shrink-0">
        <img src="/corporate.jpg" alt="" class="w-full h-full object-cover"/>
    </div>

    <div class="w-full lg:w-1/2 px-8 sm:px-16 py-20 lg:py-28 flex flex-col justify-center">
        <p class="text-sm font-bold uppercase tracking-wide text-[#2b64f0]">Elaborated Code and Creative Design</p>

        <h2 class="mt-4 text-4xl sm:text-5xl font-extrabold uppercase tracking-tight text-black">What We Offers</h2>

        <blockquote class="mt-6 border-l-4 border-[#2b64f0] pl-6 text-base italic leading-relaxed text-gray-600">
            Duis sed odio sit amet nibh vulputate cursus a sit amet mauris ipsuy veli. Nam nec tellus a odio tincidunt
            auctor
        </blockquote>

        <div class="mt-14 flex flex-col sm:flex-row gap-12 sm:gap-16">
            {#each offers as offer}
                <div class="flex-1 max-w-xs">
                    <img src={offer.icon} alt="" class="w-16 h-16 opacity-40 grayscale"/>
                    <h3 class="mt-6 text-xl font-bold text-black">{offer.title}</h3>
                    <p class="mt-4 text-sm leading-relaxed text-gray-500">{offer.text}</p>
                    <a href="/" class="mt-6 inline-flex items-center gap-2 text-xs uppercase tracking-widest text-gray-500 hover:text-black">
                        Read More
                        <img src="/right.png" alt="" class="w-3 h-3"/>
                    </a>
                </div>
            {/each}
        </div>

        <div class="mt-16">
            <a href="/" class="inline-flex items-center gap-3 bg-[#2f2f2f] hover:bg-black text-white text-sm font-semibold uppercase tracking-wider px-8 py-5 transition-colors">
                View All Offers
                <img src="/right.png" alt="" class="w-3 h-3 invert"/>
            </a>
        </div>
    </div>
</section>
