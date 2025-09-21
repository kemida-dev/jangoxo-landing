<template>
    <section id="features">
        <h2 class="text-4xl font-bold text-center text-zinc-800 sm:text-6xl" v-if="title">{{ title }}</h2>
        <p class="max-w-3xl mx-auto my-10 text-xl text-center text-zinc-500" v-if="description">{{ description }}</p>

        <div class="grid gap-6 mt-10 mb-20 md:grid-cols-3">
            <div v-for="(item, i) of items" :key="i" ref="itemsRef"
                class="feature-item p-4 border-2 rounded-lg shadow-xl border-zinc-300 sm:p-8 bg-blue-100/30">
                <div class="flex items-center justify-between mb-4 gap-x-3">
                    <Icon class="w-8 h-8" v-if="item.icon" :name="item.icon" />
                    <span class="text-md text-white bg-blue-500/70 rounded-md px-2 py-1" v-if="item.label">{{ item.label
                    }}</span>
                </div>
                <h3 class="text-2xl font-semibold text-zinc-800" v-if="item.title">{{ item.title }}</h3>
                <p class="mt-2 leading-relaxed text-zinc-500" v-if="item.description">{{ item.description }}</p>
            </div>
        </div>
    </section>
</template>

<script setup>
import { nextTick, onMounted, ref } from 'vue';

const props = defineProps({
    title: String,
    description: String,
    items: Array,
});

const itemsRef = ref([]);

onMounted(async () => {
    await nextTick();
    let els = Array.isArray(itemsRef.value) && itemsRef.value.length ? itemsRef.value.filter(Boolean) : Array.from(document.querySelectorAll('.feature-item'));
    if (!els || !els.length) return;

    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('visible');
                observer.unobserve(entry.target);
            }
        });
    }, { threshold: 0.12 });

    els.forEach((el, idx) => {
        el.style.setProperty('--delay', `${idx * 120}ms`);
        observer.observe(el);
    });
});
</script>

<style scoped>
.feature-item {
    position: relative;
    opacity: 0;
    transform-origin: center bottom;
    transform: perspective(900px) rotateX(20deg) translateY(18px) scale(.98);
    transition: opacity 420ms cubic-bezier(.2, .9, .2, 1) var(--delay), transform 520ms cubic-bezier(.18, .85, .32, 1) var(--delay), box-shadow 260ms ease;
    will-change: opacity, transform, box-shadow;
    border-radius: 12px;
}

.feature-item::before {
    content: '';
    position: absolute;
    inset: -14px;
    z-index: -1;
    border-radius: 14px;
    background: radial-gradient(closest-side, rgba(59, 130, 246, 0.08), transparent 45%);
    opacity: 0;
    transform: scale(.92);
    transition: opacity 420ms ease var(--delay), transform 520ms cubic-bezier(.18, .85, .32, 1) var(--delay);
}

.feature-item.visible {
    opacity: 1;
    transform: perspective(900px) rotateX(0deg) translateY(0) scale(1);
    box-shadow: 0 18px 40px rgba(8, 20, 50, 0.08), 0 6px 20px rgba(8, 20, 50, 0.04);
}

.feature-item.visible::before {
    opacity: 1;
    transform: scale(1.02);
}

.feature-item:hover {
    transform: translateY(-6px) scale(1.02);
    box-shadow: 0 30px 60px rgba(8, 20, 50, 0.12);
}

@media (prefers-reduced-motion: reduce) {

    .feature-item,
    .feature-item.visible {
        transition: none !important;
        transform: none !important;
        opacity: 1 !important;
        box-shadow: none !important;
    }

    .feature-item::before {
        display: none !important;
    }
}
</style>
