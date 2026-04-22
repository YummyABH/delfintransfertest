<script setup>
import IconDaw from '../icons/IconDaw.vue';
import IconCicle from '../icons/IconCicle.vue';
import IconArrow from '../icons/IconArrow.vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { ref } from 'vue';
import { Navigation } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/navigation'

const isOpen = defineModel('isOpen')
const isOpenPreview = ref(false)
const isActivePreview = ref(null)

defineProps({
    list: Object,
})
</script>

<template>
    <div v-show="isOpenPreview" @click="isOpenPreview = false, isActivePreview = null"
        class="w-screen h-screen fixed left-0 top-0 z-100 bg-[#00000074]">
        <img :src="'/' + isActivePreview" alt="Тур 1"
            class="max-w-screen max-h-screen z-101 fixed left-1/2 top-1/2 transform -translate-1/2">
    </div>
    <div
        class="group bg-white rounded-3xl overflow-hidden flex-1 flex flex-col shadow-lg hover:shadow-2xl transition-all duration-300 border border-zinc-100 max-w-lg mx-auto">

        <!-- Слайдер / Изображение -->
        <div class="relative overflow-hidden">
            <swiper class="mySwiper2" :slides-per-view="1" :space-between="10" :loop="true" :modules="[Navigation]"
                :navigation="{
                    nextEl: '.custom-next',
                    prevEl: '.custom-prev'
                }">
                <swiper-slide v-for="item in list.slidesImg" :key="item">
                    <img @click="isOpenPreview = true, isActivePreview = item"
                        class="cursor-pointer w-full h-84 object-cover transition-transform duration-500 group-hover:scale-105"
                        :src="'/' + item" alt="Тур 1">
                </swiper-slide>
            </swiper>
            <button
                class="custom-prev absolute left-2 top-1/2 -translate-y-1/2 z-10 w-8 h-12 flex items-center justify-center transition-all duration-200">
                <IconArrow class="cursor-pointer text-white hover:opacity-50 duration-200" />
            </button>

            <button
                class="custom-next absolute right-2 top-1/2 -translate-y-1/2 z-10 w-8 h-12 flex items-center justify-center transition-all duration-200">
                <IconArrow class="cursor-pointer hover:opacity-50 duration-200 text-white rotate-180" />
            </button>

            <div
                class="absolute top-4 left-4 bg-white/90 backdrop-blur-sm text-xs font-semibold px-3 py-1 rounded-full shadow-sm">
                Популярный тур
            </div>
        </div>

        <!-- Контент -->
        <div class="p-6 max-lg:p-3 max-sm:px-1 flex-1 flex-col justify-between flex">
            <!-- Преимущества -->
            <ul class="space-y-4 sm:space-y-3 mb-6">
                <li class="flex font-semibold justify-self-center items-start gap-3 text-gray-700">
                    Гостевой дом «Дельфин» —<br>
                    Ваш тихий уголок в Агудзере
                </li>
                <li class=" items-start sm:flex gap-3 text-gray-700">
                    <span class="text-[15px] leading-relaxed">Всего в 7–8 минутах от моря, через тенистый парк имени
                        Смецкого, вас ждёт место, где отдых становится по-настоящему полным.</span>
                </li>
                <li class=" items-start sm:flex gap-3 text-gray-700">
                    <span class="text-[15px] leading-relaxed">4 уютных дома для комфортной жизни</span>
                </li>
                <li class=" items-start sm:flex gap-3 text-gray-700">
                    <span class="text-[15px] leading-relaxed">В каждом доме:</span>
                </li>
                <div class="">
                    <li class=" items-start sm:flex gap-3 text-gray-700">
                        <span class="text-[15px] leading-relaxed">• качественная мебель</span>
                    </li>
                    <li class=" items-start sm:flex gap-3 text-gray-700">
                        <span class="text-[15px] leading-relaxed">• современные ортопедические матрасы для здорового
                            сна</span>
                    </li>
                    <li class=" items-start sm:flex gap-3 text-gray-700">
                        <span class="text-[15px] leading-relaxed">• бытовая техника — всё под рукой</span>
                    </li>
                    <li class=" items-start sm:flex gap-3 text-gray-700">
                        <span class="text-[15px] leading-relaxed">• детские кроватки для самых юных гостей
                            (предоставляются по запросу)</span>
                    </li>
                </div>
                <li class=" items-start sm:flex gap-3 text-gray-700">
                    <span class="text-[15px] leading-relaxed">Общее пространство для вашего удобства:</span>
                </li>
                <div class="">
                    <li class=" items-start sm:flex gap-3 text-gray-700">
                        <span class="text-[15px] leading-relaxed">• Просторная общая кухня — есть плита, посуда и всё
                            необходимое, чтобы готовить с удовольствием.</span>
                    </li>
                    <li class=" items-start sm:flex gap-3 text-gray-700">
                        <span class="text-[15px] leading-relaxed">• Мангальная зона — для вечеров с шашлыками и душевных
                            разговоров.</span>
                    </li>
                </div>
                <li class=" items-start sm:flex gap-3 text-gray-700">
                    <span class="text-[15px] leading-relaxed">Особое внимание — каждому гостю.</span>
                </li>
                <li class=" items-start sm:flex gap-3 text-gray-700">
                    <span class="text-[15px] leading-relaxed">Наш дружелюбный лабрадор Рокки уже готов познакомиться и
                        подарить вам свою любовь.<br>
                        Он — живая душа «Дельфина», и дети, и взрослые уезжают отсюда с тёплыми воспоминаниями о
                        нём.</span>
                </li>
                <li class=" items-start sm:flex gap-3 text-gray-700">
                    <span class="text-[15px] leading-relaxed">Локация</span>
                </li>
                <li class=" items-start sm:flex gap-3 text-gray-700">
                    <span class="text-[15px] leading-relaxed">Агудзера, Гулрыпшский район. Тишина, близость к природе и
                        лёгкий доступ к морю через живописный парк.</span>
                </li>
                <li class="text-gray-700 font-base">Агудзера, Гулрыпшский район. Тишина, близость к природе и
                    лёгкий доступ к морю через живописный парк.</li>
                <li class="text-gray-700 italic font-light">Приезжайте в «Дельфин».<br>
                    Мы встречаем не как гостей,<br>
                    а как старых друзей.<br>
                    Уверены: вы будете приятно удивлены радушием, чистотой и настоящим домашним комфортом.</li>
            </ul>
            <!-- Цена -->
            <div class="">
                <div class="flex items-baseline gap-1 mb-5">
                    <span class="text-sm text-zinc-500">от</span>
                    <span class="text-3xl font-bold text-zinc-900">{{ list.price }}</span>
                    <span class="text-zinc-500">руб.</span>
                </div>

                <!-- Кнопка -->
                <button @click="isOpen = !isOpen"
                    class="text-[15px] w-full cursor-pointer bg-[#ddb642] hover:bg-[#e5c667] active:bg-[#baa35e] transition-colors text-white font-semibold py-4 rounded-2xl text-base shadow-sm flex items-center justify-center gap-2">
                    Забронировать
                </button>
            </div>
        </div>
    </div>
</template>