<template>
    <div class="slide-right w-full rounded-md bg-background sm:p-5 max-sm:p-3 shadow-custom">
        <h1 class="sm:text-xl max-sm:text-lg font-semibold mb-3"><span class="text-title">Project</span></h1>
        <div class="testimonial w-full flex justify-start space-x-4 items-start h-max overflow-x-auto">
            <div v-for="(project, index) in projects" :key="index" class="flex-none sm:w-[85%] max-sm:w-full min-h-44 p-3 bg-black/50 rounded">
                <!-- <div class="w-full flex items-center space-x-2">
                    <figure
                        class="sm:w-12 max-sm:w-10 sm:h-12 max-sm:h-10 rounded-full flex items-center justify-center overflow-hidden bg-background">
                        <span class="mdi mdi-account sm:text-3xl max-sm:text-2xl"></span>
                    </figure>
                    <p class="sm:text-lg max-sm:text-base font-bold">{{ project.firstName }} <span class="text-title">{{ project.latsName }}.</span></p>
                </div> -->
                <p class="sm:text-lg max-sm:text-base font-semibold px-2">{{ project.title }}</p>
                <p class="text-justify leading-relaxed max-sm:text-sm mt-2 px-2 text-sm">{{ project.description }}</p>
                <a :href="project.link" target="_blank" class=" ml-2 my-3 w-28 h-9 text-sm max-sm:text-xs rounded-md bg-background flex items-center justify-center outline-none transition duration-300 ease-in-out border border-background hover:border-title hover:text-title">Lihat Project</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'project-component',
    data() {
        return {
            projects: [
                {
                    title: 'Membuat project dengan flutter',
                    link: '',
                    description: '.',
                },
                {
                    title: '',
                    link: '',
                    description: '.',
                },
                {
                    title: '',
                    link: '',
                    description: '. ',
                },
            ],
        }
    },
}
</script>

<style lang="scss" scoped>
$bg-scrollbar: #29241e;
$color-scrollbar: #333230;
$color-scrollbar-hover: #303233;

.testimonial {
    &::-webkit-scrollbar {
        width: 0;
        height: 8px;
    }

    &::-webkit-scrollbar-track {
        background: $bg-scrollbar;
        border-radius: 5px;
    }

    &::-webkit-scrollbar-thumb {
        background-color: $color-scrollbar;
        border-radius: 8px;

        &:hover {
            background-color: $color-scrollbar-hover;
        }
    }
}
</style>