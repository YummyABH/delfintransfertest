<script setup>
import { ref } from 'vue';
import IconDaw from './icons/IconDaw.vue';
import IconTelegramm from './icons/IconTelegramm.vue';
import IconWhatsapp from './icons/IconWhatsapp.vue';

const isOpen = defineModel('isOpen')
const isOpenLink = ref(false)

</script>

<template>
    <div v-show="isOpenLink" @click="isOpenLink = false"
        class="fixed w-screen h-screen bg-black/70 flex justify-center items-center top-1/2 left-1/2 z-100 transform -translate-1/2">
        <div class="bg-white relative border-[#e5c667] w-max  border px-10 pb-6 pt-10 ">
            <button @click="closeModal"
                class="cursor-pointer absolute top-2 right-2 w-8 h-8 flex items-center justify-center text-gray-400 hover:text-gray-600 transition-colors">
                ✕
            </button>
            <div class="flex gap-x-2">
                <a href="tg:@gostevoi_dom_delfine989" target="_blank">
                    <div class="bg-[#0084c6] duration-200 cursor-pointer rounded-lg flex p-2 
                                    transition-all 
                                    hover:bg-[#006a9e]
                                    hover:shadow-[inset_0_4px_10px_rgba(0,0,0,0.35)]
                                    active:scale-95 
                                    active:shadow-[inset_0_8px_16px_rgba(0,0,0,0.5)]">
                        <IconTelegramm />
                    </div>
                </a>
                <a href="https://wa.me/message/5VZS6ZUKG5SSE1" target="_blank">
                    <div class="bg-[#01e675] duration-200 cursor-pointer rounded-lg flex p-2 
                                    transition-all 
                                    hover:bg-[#70d850]
                                    hover:shadow-[inset_0_4px_10px_rgba(0,0,0,0.35)]
                                    active:scale-95 
                                    active:shadow-[inset_0_8px_16px_rgba(0,0,0,0.5)]">
                        <IconWhatsapp />
                    </div>

                </a>
                <a href="https://max.ru/u/f9LHodD0cOJWv4FpXUT5fnw0AlV0XkGw8P7eq1lEXDadg6m1PJNAu9eTCxU" target="_blank">
                    <img class="w-10 h-10" src="/max.png" alt="">
                </a>
            </div>
            <div class="mt-4 hover:text-zinc-500 duration-200">
                <a href="tel:+79409626290">+7 (940) 962-62-90</a>
            </div>
        </div>
    </div>
    <div class="w-full lg:h-auto h-200 max-lg:h-200 overflow-y-hidden relative overflow-hidden" id="transfer">
        <div class="max-lg:hidden absolute bottom-0 right-20 max-xl:right-10 flex max-w-[35%]">
            <div class="text-[15px] rounded-lg bg-white h-min px-2 py-1 max-w-100">
                <span class="font-semibold">Здравствуйте, друзья!</span><br />
                <span class="font-light">Меня зовут Алиас, я основатель компании и уже более <span
                        class="font-semibold">10 лет</span> создаю для путешественников незабываемые впечатления от
                    Абхазии.</span>
            </div>
            <img class="w-60" src="/alias.png" alt="">
        </div>
        <div class="w-full overflow-hidden">
            <!-- <video class="absolute overflow-hidden inset-0 w-full h-full object-cover z-[-1]" autoplay loop muted
                playsinline>

                <source src="/preview.mp4" type="video/mp4">
            </video> -->
            <img src="/preview.png" class="absolute overflow-hidden inset-0 w-full h-full object-cover z-[-1]">
        </div>


        <div class="lg:hidden absolute top-34 left-1/2 -translate-x-1/2 ">
            <div class="text-center mx-2 text-[17px] font-semibold w-max max-w-screen  text-white">
                <div class="w-max max-w-full">
                    ВСТРЕЧА - БЕЗ
                    ОПОЗДАНИЙ.
                    ГРАНИЦА -
                    БЕЗ
                    ХАОСА.
                </div>
                <div class="w-max justify-self-center">
                    ЦЕНА - БЕЗ
                    СЮРПРИЗОВ
                </div>
            </div>
        </div>

        <div
            class="lg:hidden text-[15px] max-sm:px-0 max-sm:py-5  max-w-140 px-10 py-10 rounded-2xl mx-auto max-lg:translate-y-1/2 max-sm:translate-y-3/5  text-white backdrop-blur-md">
            <h1 class="text-center max-sm:text-xl text-2xl  text-white mb-10">ЛИЦЕНЗИРОВАННЫЙ ТРАНСФЕР<br>
                РЕСПУБЛИКИ АБХАЗИЯ
            </h1>
            <div class="flex gap-x-4 border-y max-sm:px-5 max-sm:text-sm px-10 text-lg py-3 ">
                <IconDaw class="mb-0.75" />
                <h2 class="">VIP поездки по Абхазии</h2>
            </div>
            <div class="flex gap-x-4 border-y max-sm:px-5 max-sm:text-sm px-10 text-lg py-3">
                <IconDaw class="mb-0.75" />
                <h2 class="">Встречаем в аэропорту Сочи, Ж/Д вокзале Адлера</h2>
            </div>
            <div class="flex gap-x-4 border-y max-sm:px-5 max-sm:text-sm px-10 text-lg py-3">
                <IconDaw />
                <h2 class="">Встречаем на границе</h2>
            </div>
            <div class="flex gap-x-4 border-y max-sm:px-5 max-sm:text-sm px-10 text-lg py-3">
                <IconDaw />
                <h2 class=" ">Встречаем в аэропорту Сухум</h2>
            </div>
            <div class="w-max gap-x-4 gap-y-2 overflow-x-hidden flex justify-self-center mt-6">
                <div
                    class=" box-border border-3 px-5 py-3  border-white  hover:border-[#ffde7ba4]  hover:bg-[#ffde7ba4] duration-200 cursor-pointer">
                    <span @click="isOpen = !isOpen">
                        Оставить заявку
                    </span>
                </div>
                <div @click="isOpenLink = !isOpenLink"
                    class="text-center w-max relative box-border border-3 px-5 py-3  border-white  hover:border-[#ffde7ba4]  hover:bg-[#ffde7ba4] duration-200 cursor-pointer">
                    <span>
                        Позвонить
                    </span>
                </div>
            </div>
        </div>

        <div class=" flex max-lg:hidden mt-22  w-full relative ">
            <div class="max-w-7xl w-full mx-auto px-10 max-md:px-5">
                <div
                    class="border-x-3 backdrop-blur-md justify-self-start bg-white/1 text-white pb-20 pt-10  border-[#cdad4b]">
                    <div class="mb-2 flex justify-self-center w-max">
                        <h2 class="text-xl  font-bold mb-2 text-center text-white  max-[350px]:text-lg ">Из
                            СОЧИ
                            В АБХАЗИЮ -
                            С
                            КОМФОРТОМ</h2>
                    </div>
                    <div class="mb-6 text-center text-[15px]  w-max justify-self-center  text-white">
                        <div class="text-[17px] w-max max-w-full">
                            ВСТРЕЧА - БЕЗ
                            ОПОЗДАНИЙ.
                            ГРАНИЦА -
                            БЕЗ
                            ХАОСА.
                        </div>
                        <div class="w-max justify-self-center">
                            Цена - без
                            сюрпризов
                        </div>
                    </div>
                    <h1 class="px-0 text-center text-3xl mt-0 text-white mb-6">ЛИЦЕНЗИРОВАННЫЙ ТРАНСФЕР<br>
                        РЕСПУБЛИКИ АБХАЗИЯ
                    </h1>
                    <div class=" flex gap-x-6 border-y px-10 text-xl py-4">
                        <IconDaw class="mb-0.75" />
                        <h2 class="">VIP поездки по Абхазии</h2>
                    </div>
                    <div class=" flex gap-x-6 border-y px-10 text-xl py-4">
                        <IconDaw class="mb-0.75" />
                        <h2 class="">Встречаем в аэропорту Сочи, Ж/Д вокзале Адлера</h2>
                    </div>
                    <div class="flex gap-x-6  px-10 border-y text-xl py-4">
                        <IconDaw />
                        <h2 class="">Встречаем на границе</h2>
                    </div>
                    <div class="flex gap-x-6  px-10 border-y text-xl py-4 mb-10">
                        <IconDaw />
                        <h2 class=" ">Встречаем в аэропорту Сухум</h2>
                    </div>
                    <div class=" w-max flex gap-x-4 justify-self-center overflow-x-hidden">
                        <div @click="isOpen = !isOpen"
                            class="relative box-border border-3 px-10 py-3  border-white  hover:border-[#ffde7ba4]  hover:bg-[#ffde7ba4] duration-200 cursor-pointer">
                            <span>
                                Оставить заявку
                            </span>
                        </div>
                        <div @click="isOpenLink = !isOpenLink"
                            class="relative box-border border-3 px-10 py-3  border-white  hover:border-[#ffde7ba4]  hover:bg-[#ffde7ba4] duration-200 cursor-pointer">
                            <span>
                                Позвонить
                            </span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- <div
                class="h-2/1 max-w-170  text-white absolute border-x-3 border-[#cdad4b] -top-14 left-70 max-lg:left-1/2 max-lg:-translate-x-1/2 z-1 -rotate-8 backdrop-blur-md bg-white/1 py-20 ">
                <h1 class="rotate-8 px-10 text-center text-3xl mt-10 text-white mb-22">ЛИЦЕНЗИРОВАННЫЙ ТРАНСФЕР<br>
                    РЕСПУБЛИКИ АБХАЗИЯ.
                </h1>
                <div class="rotate-8 flex gap-x-6 border-y px-10 text-xl py-4">
                    <IconDaw class="mb-0.75" />
                    <h2 class="">VIP поездки по Абхазии</h2>
                </div>
                <div class="rotate-8 flex gap-x-6 border-y px-10 text-xl py-4">
                    <IconDaw class="mb-0.75" />
                    <h2 class="">Встречаем в аэропорту Сочи, Ж/Д вокзале Адлера</h2>
                </div>
                <div class="flex gap-x-6  rotate-8 px-10 border-y text-xl py-4">
                    <IconDaw />
                    <h2 class="">Встречаем на границе</h2>
                </div>
                <div class="flex gap-x-6 rotate-8 px-10 border-y text-xl py-4 mb-10">
                    <IconDaw />
                    <h2 class=" ">Встречаем в аэропорту Сухум</h2>
                </div>
                <div class=" w-max overflow-x-hidden rotate-8">
                    <div @click="isOpen = !isOpen"
                        class="relative box-border border-3 px-10 py-3 ml-10 border-white  hover:border-[#ffde7ba4]  hover:bg-[#ffde7ba4] duration-200 cursor-pointer">
                        <span>
                            Оставить заявку
                        </span>
                    </div>
                </div>

            </div> -->
        </div>
    </div>
</template>