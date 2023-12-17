<script>
    import agni from '../assets/agnios-logo.png';
</script>
<style>
    .line{
        line-height: normal;
    }
</style>
<div>
    <section class="text-gray-600 body-font py-24 px-5 md:px-16 md:h-screen">
        <div
                class="w-11/12 mx-auto flex md:py-16 py-5 md:flex-row flex-col pb-5 items-center md:"
        >
            <div
                    class="absolute z-30 py-0 left-0 w-32 sm:w-80 h-96 bg-gradient-to-r from-red-200 via-orange-500 to-yellow-100 opacity-30 blur-3xl flex-none order-4 rounded-xl transform -rotate-45 pointer-events-none"
            >
            </div>

            <div
                    class="lg:flex-grow lg:pr-0 md:pr-12 flex flex-col md:items-start md:text-left mb-10 md:mb-0 items-center text-start font-title"
            >
                <h1
                        class="line 2xl:text-6xl xl:text-5xl sm:text-4xl text-3xl mb-2 text-white font-semibold sm:text-start"
                >

<!--                    <div-->
<!--&lt;!&ndash;                            class="absolute z-30 -translate-y-1/4 py-0 left-50 w-32 sm:w-80 h-96 bg-gradient-to-r from-red-200 via-orange-500 to-yellow-100 opacity-30 blur-3xl flex-none order-4 rounded-xl transform -rotate-45 pointer-events-none"&ndash;&gt;-->
<!--                    >-->
<!--                    </div>-->
                    Customise your computing experience with AGNI OS          </h1>
                <p class="mb-8 text-center leading-relaxed text-orange-500 sm:text-sm text-xs font-semibold">
                    Agni OS • An Arch Based Linux Distribution • Built for Developers
                </p>
                <p class="mb-8 leading-relaxed text-[#D0D5DD] sm:text-base text-md text-center">
                    Fast and Modern operating system for the busy developer
                </p>
                <div class="flex items-center gap-2 md:gap-4 flex-wrap justify-center">
                    <div class="flex justify-center h-min">
                        <a
                                class="button-gradient inline-flex text-white h-12 bg-[#C81400] shadow-base shadow-gray-500 border-white border-y-2 py-2 px-6 focus:outline-none rounded-3xl text:base md:text-lg hover:bg-orange-700"
                                href="https://www.youtube.com/demonkillerr"
                                target="_blank">Explore</a
                        >
                    </div>

                </div>
            </div>

            <div class="flex sm:w-1/2">
                <div
                        class="hidden md:flex absolute z-30 pt-20 m-14 w-48 h-52 xl:w-[400px] xl:h-[300px] opacity-30 blur-2xl flex-none order-4 rounded-full pointer-events-none"
                >
                </div>
                <div
                        class="absolute z-30 -translate-y-3 py-0 left-50 w-32 sm:w-80 h-96 bg-gradient-to-r from-red-200 via-orange-500 to-yellow-100 opacity-40 blur-3xl flex-none order-4 rounded-xl transform -rotate-45 pointer-events-none"
                >
                </div>

                <div class="sm:z-50 flex align-middle rounded-xl m-2">
                    <img class="w-full object-contain sm:h-80" src={agni} />
                </div>
            </div>
        </div>
    </section>
    <dialog id="requirements" class="w-5/6 md:w-3/4 lg:w-2/4 p-0 rounded-xl bg-[#293b5c] text-white opacity-3" >

        <div id="inside-req" class="p-6 lg:p-8 w-full h-full space-y-2">
            <div class="flex justify-between " >
                <h1 class="text-2xl font-title font-semibold">Requirements</h1>
                <button id="close-req" class="text-2xl font-medium" >X</button>
            </div>
            <ul class="list-disc ml-8" >
                <li>
                    64 bit x86_64 processor (Intel/AMD), with atleast 2 CPU cores. (32-bit
                    not supported)
                </li>
                <li>Any GPU/iGPU with OpenGl 3.3+ support.</li>
                <li>Atleast 2GB DDR3/DDR4 RAM.</li>
                <li>
                    Atleast 10GB HDD/SSD storage. (Although installer will allow min
                    5.5GB)
                </li>
                <li>
                    Basic WPA/WPA2 compatible wifi card or ethernet supported motherboard.
                </li>
            </ul>
        </div>
    </dialog>
</div>

