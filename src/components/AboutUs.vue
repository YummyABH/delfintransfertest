<script setup>
import { ref } from 'vue';
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
    <section class="py-10 px-4 bg-white">
        <div class="max-w-7xl mx-auto">
            <div class="">
                <!-- Заголовок -->
                <h2 class="text-2xl  md:text-4xl font-bold text-center text-gray-900 mb-4">
                    О компании
                </h2>
                <div class="w-20 h-1 bg-amber-500 mx-auto mb-10 rounded-full"></div>

                <!-- Весь текст одним блоком -->
                <div class="space-y-4 text-[15px]  text-gray-700 leading-relaxed text-base md:text-lg ">

                    <p>
                        <span class="font-semibold text-gray-900">Здравствуйте, друзья!</span><br />
                        Меня зовут Алиас, я основатель компании и уже более
                        <span class="font-semibold">10 лет</span> создаю для путешественников
                        незабываемые впечатления от Абхазии.
                    </p>

                    <p>
                        Отдельное внимание я уделяю <span class="font-semibold text-gray-900">трансферу</span> —
                        ведь именно с него начинается ваш отдых. Никаких очередей на границе, поисков попуток
                        или переживаний «как доехать».
                    </p>

                    <p class="font-semibold text-gray-900 pt-2">Вы получаете:</p>
                    <ul class="space-y-2 pl-4">
                        <li>· личного водителя, который встретит вас прямо у выхода из российского паспортного
                            контроля;
                        </li>
                        <li>· комфортабельный автомобиль (с кондиционером, зарядкой для телефона и водой);</li>
                        <li>· помощь в прохождении границы — я подскажу все нюансы, чтобы вы пересекли её быстро и
                            без
                            нервов;</li>
                        <li>· трансфер «от двери до двери»: из аэропорта Адлера, ж/д вокзала или из любого места в
                            Сочи
                            прямо до вашего отеля или гостевого дома в Абхазии.</li>
                    </ul>

                    <p>
                        Я лично отвечаю за безопасность, пунктуальность и комфорт в каждой детали.
                        Покажу вам удивительные места, стану проводником в мир культуры и традиций моей Родины.
                        Верю, что каждый гость заслуживает лучшего — и обеспечиваю это в каждой поездке.
                    </p>

                    <p>
                        Исследуйте древние места, насладитесь пейзажами, погрузитесь в обычаи гостеприимной Абхазии
                        — и главное, проведите отдых без единой дорожной проблемы.
                    </p>

                    <p class="font-semibold text-center pt-4">
                        Свяжитесь со мной сегодня — и я организую не только трансфер, но и всё путешествие вашей
                        мечты в
                        Абхазию.
                    </p>
                    <!-- Кнопка -->
                    <div
                        class=" w-max max-sm:flex-col max-sm:gap-y-2 flex gap-x-4 justify-self-center overflow-x-hidden">
                        <div @click="isOpen = !isOpen"
                            class="relative box-border border-3 px-10 py-3  border-[#ffde7ba4]  hover:border-[#ffde7ba4]  hover:bg-[#ffde7ba4] duration-200 cursor-pointer">
                            <span>
                                Оставить заявку
                            </span>
                        </div>
                        <div @click="isOpenLink = !isOpenLink"
                            class="relative box-border border-3 px-10 py-3  border-[#ffde7ba4]  hover:border-[#ffde7ba4]  hover:bg-[#ffde7ba4] duration-200 cursor-pointer">
                            <span>
                                Позвонить
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>