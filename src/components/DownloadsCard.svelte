<script>
    import { onMount } from "svelte";
    import info from "../assets/infoIcon.png";

    let requirements;
    let insideReq;

    onMount(() => {
        const reqBtn = document.getElementById("req-btn");
        const closeReq = document.getElementById("close-req");

        reqBtn.addEventListener("click", () => {
            requirements.showModal();
        });

        closeReq.addEventListener("click", () => {
            requirements.close();
        });

        window.onclick = (event) => {
            if (event.target.contains(insideReq) && event.target !== insideReq) {
                requirements.close();
            }
        };
    });
</script>

<style>
    .gradient {
        background: linear-gradient(0deg, rgba(0, 0, 0, 0.30) 0%, rgba(0, 0, 0, 0.30) 100%),
        linear-gradient(145deg, rgba(75, 72, 72, 0.20) 13.28%, rgba(187, 180, 180, 0.14) 87.52%);
    }
</style>

<div class="flex justify-center items-center">
    <div class="gradient w-full p-6 sm:mx-24 mx-5 mb-12 bg-white border-b border-gray-500 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
        <h5 class="mb-2 text-4xl font-semibold tracking-tight text-white dark:text-white">Downloads</h5>
        <p class="mb-3 font-normal text-[#D0D5DD] dark:text-gray-400">AGNI OS source code and installers are available for download for all versions!! </p>
        <div class="flex sm:flex-row flex-col gap-4">
            <div class="flex items-center gap-2 md:gap-4 flex-wrap justify-start">
                <div class="flex justify-center h-min">
                    <a
                            class="button-gradient inline-flex text-white h-12 bg-[#C81400] shadow-base shadow-gray-500 border-white border-y-2 py-2 px-6 focus:outline-none rounded-3xl text:base md:text-lg hover:bg-orange-700"
                            href="https://www.youtube.com/watch?v=8kL1NEtSIi4"
                            target="_blank"
                    >
                        Downloads
                    </a>
                </div>
            </div>
            <button
                    class="flex flex-row w-fit p-2 h-12 px-4 cursor-pointer gap-2 items-center justify-center border rounded-full border-white hover:bg--50 hover:bg-opacity-20 text-white"
                    id="req-btn"
            >
                <span class="h-6 md:font-semibold">Requirements</span>
                <span class="p-1 ml-1 bg-custom-btn rounded-full">
                    <img
                            class="w-full h-full"
                            src={info}
                            alt=""
                    />
                </span>
            </button>
            <a class="flex flex-row items-center p-2 gap-2 text-white" href="/#verify">
                <i
                        class="font-semibold text-base underline underline-offset-4 not-italic"
                >
                    Verify your download &rarr;
                </i>
            </a>
        </div>
    </div>
    <dialog bind:this={requirements} class="w-5/6 md:w-3/4 lg:w-2/4 p-0 rounded-xl bg-gradient-to-b from-orange-500/80 to-black text-white opacity-3">
        <div bind:this={insideReq} class="p-6 lg:p-8 w-full h-full space-y-2">
            <div class="flex justify-between ">
                <h1 class="text-2xl font-title font-semibold">Requirements</h1>
                <button id="close-req" class="text-2xl font-medium">X</button>
            </div>
            <ul class="list-disc ml-8">
                <li>
                    64 bit x86_64 processor (Intel/AMD), with at least 2 CPU cores. (32-bit not supported)
                </li>
                <li>Any GPU/iGPU with OpenGL 3.3+ support.</li>
                <li>At least 2GB DDR3/DDR4 RAM.</li>
                <li>
                    At least 10GB HDD/SSD storage. (Although installer will allow min 5.5GB)
                </li>
                <li>
                    Basic WPA/WPA2 compatible wifi card or ethernet supported motherboard.
                </li>
            </ul>
        </div>
    </dialog>
</div>
