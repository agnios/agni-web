<script>
    // import { CopyToClipboard } from 'your-copy-to-clipboard-component'; // Import the CopyToClipboard component

    const stepOne = [
        {
            id: 1,
            nameOfOS: "Windows",
            description: "Open windows terminal (powershell) in the Downloads folder or wherever the ISO is and type:",
            downloadableFileName: "certutil -hashfile iso-name.iso sha256",
        },
        {
            id: 2,
            nameOfOS: "MacOS",
            description: "open terminal in the Downloads folder or wherever the ISO is and type:",
            downloadableFileName: "shasum -a 256 iso-name.iso",
        },
        {
            id: 3,
            nameOfOS: "Linux",
            description: "Open terminal in the Downloads folder or wherever the ISO is and type:",
            downloadableFileName: "sha256sum iso-name.iso",
        },
    ];

    // const sha256Sum = "30591aa836142638e8990f8d856c037b556067f7670e702ddda2ff2abd35671a";
</script>

<style>
    .verify-download-gradient {
        /* Define your gradient styles here */
    }

    .gradient{
        /*border: 1px solid white;*/
        background: linear-gradient(0deg, rgba(0, 0, 0, 0.30) 0%, rgba(0, 0, 0, 0.30) 100%),
        linear-gradient(145deg, rgba(75, 72, 72, 0.20) 13.28%, rgba(187, 180, 180, 0.14) 87.52%);
    }

</style>

<div id="verify" class="w-full block px-5 md:px-16">
    <p class="font-title text-center text-[#FCFCFD] text-2xl md:text-4xl pt-2 pb-2">Verify Your Download</p>
    <div class="pt-4">
        <div class="bg-gradient-to-r from-orange-800 to-orange-600 w-fit m-4 p-2 rounded-2xl">
            <p class="text-[#FFFFFF] w-max">Steps 1</p>
        </div>
        <div class="flex mt-6 flex-col xl:flex-row md:flex-row">
            {#each stepOne as step (step.id)}
                <div class="m-4 rounded-2xl mt-2 mb-2 bg-gradient-to-b from-orange-500/50 to-black">
                    <div class="p-4 rounded-t-xl">
                        <p class="font-title text-[#FCFCFD] text-xl md:text-2xl pt-2 pb-2">{step.nameOfOS}</p>
                        <p class="text-[#E4E7EC]">{step.description}</p>
                    </div>
                    <div class="w-full relative mt-2 overflow-hidden">
                        <div class="absolute top-0 left-0 verify-download-gradient h-20 w-full" />
                        <span class="w-full h-fit flex justify-around align-middle p-3">
              <p class="text-[#E4E7EC] flex-1 mt-1 break-all text-center border-t border-orange-950 rounded-2xl border-2 p-2">{step.downloadableFileName}</p>
<!--              <CopyToClipboard {text}={step.downloadableFileName} />-->
            </span>
                    </div>
                </div>
            {/each}
        </div>
    </div>



    <div class="pt-4">
        <div class="bg-orange-700 w-fit m-4 p-2 rounded-2xl">
            <p class="text-[#FFFFFF] w-max">Steps 2</p>
        </div>
        <div class="w-full mt-6">
            <p class="text-[#FFFFFF] ml-4 mb-4">
                In all the above cases, if the returned value matches with the sha256sum
                given below, your download is authentic.
            </p>
            <div class="m-4 rounded-2xl mt-2 mb-2 bg-gradient-to-b from-orange-500/50 to-black">
                <div class="p-4 rounded-t-xl">
                    <p class="font-title text-[#FCFCFD] text-xl md:text-2xl pt-2 pb-2">
                        SHA256SUMS Below:
                    </p>
                    <p class="text-[#E4E7EC]">IMAGE: agnios-2023.08.16-x86_64.iso</p>
                </div>

                <div class="w-full relative mt-2 overflow-hidden rounded-b-xl">
                    <div
                            class="absolute top-0 left-0 rounded-b-xl h-24 w-full opacity-50 blur-lg pointer-events-none"
                    >
                    </div>
                    <span class="z-20 w-full  h-auto flex justify-around align-middle p-3">
            <div class="text-[#E4E7EC] flex-1 break-all border-t border-orange-950 rounded-2xl border-2 p-2">
              30591aa836142638e8990f8d856c037b556067f7670e702ddda2ff2abd35671a
            </div>
          </span>
                </div>
            </div>
        </div>
    </div>
</div>
