<template>
    <section class="my-16 mx-10 md:mx-24 lg:mx-24">
        <form>
            <div
                class="bg-white shadow-md w-full md:flex lg:flex items-center justify-between"
            >
                <div
                    class="w-full grid grid-cols-1 md:grid-cols-1 lg:grid-cols-3 gap-4 items-center"
                >
                    <div class="p-6">
                        <div
                            class="flex flex-col border-dashed border-r border-gray-200"
                        >
                            <label>
                                From <span class="text-red-700">*</span>
                            </label>
                            <input
                                type="text"
                                class="w-full focus:outline-none focus:ring focus:ring-violet-300 mt-2 rounded"
                                placeholder="Kelurahan Asal"
                                required
                            />
                        </div>
                    </div>
                    <div class="p-6">
                        <div
                            class="flex flex-col border-dashed border-r border-gray-200"
                        >
                            <label>
                                Destination <span class="text-red-700">*</span>
                            </label>
                            <input
                                type="text"
                                class="w-full focus:outline-none focus:ring focus:ring-violet-300 mt-2 rounded"
                                placeholder="Kelurahan Tujuan"
                                required
                            />
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex flex-col">
                            <label>
                                Berat (Gram) <span class="text-red-700">*</span>
                            </label>
                            <input
                                type="number"
                                class="w-full focus:outline-none focus:ring focus:ring-violet-300 mt-2 rounded"
                                placeholder="1000"
                                required
                            />
                        </div>
                    </div>
                </div>
                <div class="p-6">
                    <div class="flex justify-end">
                        <button
                            class="btn-primary"
                            style="border-radius: 0.3rem !important"
                        >
                            <img src="/search.svg" class="w-6 h6" alt="" />
                        </button>
                    </div>
                </div>
            </div>
        </form>
    </section>
</template>
