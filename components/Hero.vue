<template>
    <section class="relative overflow-hidden my-8 rounded-xl">
        <div class="absolute inset-0 -z-10">
            <div class="absolute inset-0 bg-gradient-to-br from-white via-sky-50 to-sky-100"></div>
            <svg class="absolute right-0 top-0 transform translate-x-20 -translate-y-20 opacity-30" width="420"
                height="420" viewBox="0 0 420 420" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden>
                <defs>
                    <linearGradient id="g1" x1="0" x2="1">
                        <stop offset="0%" stop-color="#60a5fa" />
                        <stop offset="100%" stop-color="#06b6d4" />
                    </linearGradient>
                </defs>
                <circle cx="210" cy="210" r="180" fill="url(#g1)" />
            </svg>
        </div>

        <div class="container mx-auto px-6 lg:px-12 py-12">
            <div class="flex flex-col-reverse lg:flex-row items-center gap-10">
                <div class="flex-1 text-center lg:text-left">
                    <div
                        class="inline-flex items-center justify-center bg-white/80 backdrop-blur-sm shadow-md px-3 py-2 rounded-full mb-6">
                        <Icon class="w-5 h-5 text-yellow-400" name="lucide:star" />
                        <span class="ml-3 text-sm font-semibold text-zinc-700">Aplicación en Desarrollo</span>
                    </div>

                    <h1 class="text-3xl sm:text-5xl lg:text-6xl font-extrabold text-zinc-900 leading-tight">
                        Transforma tu Cocina en un
                        <span class="bg-gradient-to-r from-blue-600 to-cyan-400 bg-clip-text text-transparent"> Centro
                            de Excelencia</span>
                    </h1>

                    <p class="mt-4 text-zinc-600 text-lg sm:text-xl max-w-2xl mx-auto lg:mx-0">
                        Optimiza la organización de tu cocina y gestiona tu inventario con nuestra
                        solución integral diseñada para restaurantes modernos.
                    </p>

                    <div class="flex flex-wrap gap-4 mt-8 items-center justify-center lg:justify-start">
                        <NuxtLink to="#contact"
                            class="inline-flex items-center gap-3 px-6 py-3 text-base font-medium text-white rounded-lg shadow-lg bg-gradient-to-r from-blue-600 to-cyan-500 hover:from-blue-700 hover:to-cyan-600 transition-transform transform hover:-translate-y-0.5">
                            Solicitar demo gratuita
                            <Icon class="w-4 h-4" name="lucide:arrow-right" />
                        </NuxtLink>

                        <NuxtLink to="#features"
                            class="inline-flex items-center gap-3 px-6 py-3 text-base font-medium rounded-lg border border-zinc-200 bg-white hover:bg-zinc-50 transition">
                            Ver características
                        </NuxtLink>
                    </div>

                    <div class="flex justify-center lg:justify-start gap-6 mt-8 text-zinc-500">
                        <span class="flex items-center gap-2">
                            <Icon class="w-4 h-4 text-blue-500" name="lucide:circle-small" />
                            <span class="text-sm">Sin instalación compleja</span>
                        </span>
                        <span class="flex items-center gap-2">
                            <Icon class="w-4 h-4 text-blue-500" name="lucide:headphones" />
                            <span class="text-sm">Soporte 24/7</span>
                        </span>
                        <span class="flex items-center gap-2">
                            <Icon class="w-4 h-4 text-blue-500" name="lucide:zap" />
                            <span class="text-sm">Resultados inmediatos</span>
                        </span>
                    </div>
                </div>

                <div class="flex-1 flex items-center justify-center lg:justify-end">
                    <div class="relative w-64 h-64 sm:w-80 sm:h-80 lg:w-96 lg:h-96">
                        <svg class="absolute inset-0 w-full h-full blob-orbit" viewBox="0 0 600 600"
                            xmlns="http://www.w3.org/2000/svg" aria-hidden>
                            <defs>
                                <linearGradient id="b1" x1="0" x2="1">
                                    <stop offset="0%" stop-color="#60a5fa" />
                                    <stop offset="100%" stop-color="#06b6d4" />
                                </linearGradient>
                            </defs>
                            <g class="orbit-group" transform="translate(300,300)">
                                <circle class="blob-shape" cx="0" cy="0" r="110" fill="url(#b1)" />
                            </g>
                        </svg>

                        <div class="absolute right-3 top-3 flex flex-col gap-3">
                        </div>

                        <div
                            class="absolute bottom-4 left-4 w-24 h-12 rounded-xl bg-gradient-to-r from-white/60 to-white/10 blur-lg opacity-60">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.animate-blob {
    transform-origin: center;
    animation: blob 9s infinite ease-in-out;
    filter: drop-shadow(0 18px 36px rgba(6, 182, 212, 0.12));
}

@keyframes blob {
    0% {
        transform: translate(-4%, -2%) scale(1);
    }

    33% {
        transform: translate(6%, 4%) scale(1.05);
    }

    66% {
        transform: translate(-6%, 6%) scale(0.98);
    }

    100% {
        transform: translate(-4%, -2%) scale(1);
    }
}

.animate-float {
    animation: float 6s ease-in-out infinite;
}

@keyframes float {
    0% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-6px);
    }

    100% {
        transform: translateY(0);
    }
}

.hero-badges span {
    backdrop-filter: blur(6px);
}

h1 {
    word-break: keep-all;
}

@media (prefers-reduced-motion: reduce) {

    .animate-blob,
    .animate-float {
        animation: none !important;
    }
}

.blob-orbit {
    overflow: visible;
}

.orbit-group {
    transform-origin: center;
}

.blob-shape {
    filter: drop-shadow(0 18px 36px rgba(6, 182, 212, 0.12));
    transform-origin: center;
    animation: blobFloat 7s ease-in-out infinite;
}

@keyframes blobFloat {
    0% {
        transform: translateY(0) scale(1);
    }

    25% {
        transform: translateY(-6px) scale(1.02);
    }

    50% {
        transform: translateY(0) scale(1);
    }

    75% {
        transform: translateY(4px) scale(0.99);
    }

    100% {
        transform: translateY(0) scale(1);
    }
}
</style>