<template>
    <div class="box-border mx-auto w-full px-0 min-h-[700px] bg-[#f5f5f5]">
        <div class="flex flex-col box-content md:w-full sm:w-full px-5">
            <div class="flex-none relative my-4 text-header ">
                <div class="setionarea__component__content w-[84%] p-8">
                    <h2 class="text-3xl font-semibold">{{$t('Upcoming_events')}}</h2>
                </div>
            </div>
            <div class="flex-auto h-auto min-h-[500px]">
                <div class="relative block">
                    <div class="relative flex flex-row float-left gap-4">
                        <!-- one column starts -->
                        <div v-for="option in news" class="col-span-3 sm:col-span-12 md:col-span-3 gap-4">
                            <div class="flex flex-col h-[200px] object-cover w-full mt-2 float-left relative">
                                <picture>
                                    <source :srcset="option.image">
                                    <img :src="option.image">
                                </picture>
                                <h3 class="text-2xl text-header">{{ option.name }}</h3>
                                <div class="flex flex-col items-center">
                                    <el-icon>
                                        <Calendar />
                                    </el-icon>
                                    <span class="text-base">{{ formatDate(option.date_release) }}</span>
                                </div>
                                <p>{{ option.description }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="my-6 flex-auto justify-center self-center lg:mt-12">
                <button class="bg-header text-slate-100 px-4 py-2 rounded-sm">{{$t('view_all_events')}}</button>
            </div>
        </div>
    </div>
</template>
<script setup>
import { Calendar } from '@element-plus/icons-vue';
const news = ref([
    {
        name: "Nhà phát minh tuổi teen về robot phân loại rác AI giành học bổng RMIT",
        image: 'https://picsum.photos/seed/picsum/200/300',
        date_release: '19/10/2002',
        description: 'Là một học sinh giỏi, một nhà phát minh trẻ và một người yêu nhạc jazz – tài năng và sở thích của Đào Hiếu Phong cũng rộng lớn như sự tò mò của anh'
    },
    {
        name: "Nghiên cứu cho thấy tác động hai chiều của AI đối với thông tin sức khỏe",
        image: 'https://picsum.photos/seed/picsum/200/300',
        date_release: '19/10/2002',
        description: 'Là một học sinh giỏi, một nhà phát minh trẻ và một người yêu nhạc jazz – tài năng và sở thích của Đào Hiếu Phong cũng rộng lớn như sự tò mò của anh'
    },
    {
        name: "RMIT Việt Nam tôn vinh tác động thay đổi cuộc sống của học bổng",
        image: 'https://picsum.photos/seed/picsum/200/300',
        date_release: '19/10/2002',
        description: 'Là một học sinh giỏi, một nhà phát minh trẻ và một người yêu nhạc jazz – tài năng và sở thích của Đào Hiếu Phong cũng rộng lớn như sự tò mò của anh'
    },
    {
        name: "Sinh viên RMIT Việt Nam phát triển hệ thống thông tin y tế ứng dụng AI",
        image: 'https://picsum.photos/seed/picsum/200/300',
        date_release: '19/10/2002',
        description: 'Là một học sinh giỏi, một nhà phát minh trẻ và một người yêu nhạc jazz – tài năng và sở thích của Đào Hiếu Phong cũng rộng lớn như sự tò mò của anh'
    }

])
</script>
<style scoped></style>