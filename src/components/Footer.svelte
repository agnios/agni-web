<script>
    import agni from "../assets/agnios-logo.png"
</script>

<footer class=" rounded-lg shadow dark:bg-orange-900 m-4">
    <div class="w-full max-w-screen-xl mx-auto p-4 md:py-8">
        <div class="sm:flex sm:items-center sm:justify-between">
            <a href="https://agnios.org/" class="flex items-center mb-4 sm:mb-0 space-x-3 rtl:space-x-reverse">
                <img src={agni} class="h-8" alt="AgniOS Logo" />
                <span class="self-center text-2xl font-semibold whitespace-nowrap text-white">AGNI OS</span>
            </a>
            <ul class="flex flex-wrap items-center mb-6 text-sm font-medium text-gray-200 sm:mb-0 dark:text-gray-400">
                <li>
                    <a href="#" class="hover:underline me-4 md:me-6">About</a>
                </li>
                <li>
                    <a href="#" class="hover:underline me-4 md:me-6">Privacy Policy</a>
                </li>
                <li>
                    <a href="#" class="hover:underline me-4 md:me-6">Licensing</a>
                </li>
                <li>
                    <a href="#" class="hover:underline">Contact</a>
                </li>
            </ul>
        </div>
        <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
        <span class="block text-sm text-gray-300 sm:text-center dark:text-gray-400">© 2023 <a href="https://agnios.org/" class="hover:underline">Agni OS</a>. All Rights Reserved.</span>
    </div>
</footer>

