<template>
  <div
    class="flex flex-col items-center px-10 py-10 mx-auto mb-20 border-3 border-blue-400/50 border-dashed rounded-lg sm:px-20 sm:py-20"
  >
    <div class="overflow-hidden flex items-center justify-center my-4">
      <div
        class="flex items-center justify-center bg-blue-400 p-2 px-3 rounded-lg text-white"
      >
        <Icon class="w-5 h-5" name="lucide:clock" />
        <span class="ml-2 text-sm pt-1 font-semibold">Respuesta en 24 horas</span>
      </div>
    </div>
    <div class="max-w-4xl text-center">
      <h2 class="text-2xl font-bold text-zinc-800 sm:text-5xl">
        ¿Listo para Transformar tu Cocina?
      </h2>

      <p class="mt-4 text-md sm:text-lg text-zinc-500 sm:text-xl">
        Contáctanos para una consulta gratuita y descubre cómo KitchenPro puede optimizar
        las operaciones de tu restaurante.
      </p>
    </div>

    <div class="grid w-full max-w-4xl grid-cols-1 gap-6 mt-8 sm:grid-cols-2">
      <div
        class="flex flex-col border border-gray-200 shadow-md rounded-lg p-6 bg-blue-50"
      >
        <h3 class="text-xl font-semibold">Solicita tu Demo Gratuita</h3>
        <p class="mt-2 text-gray-600">
          Completa el formulario y nuestro equipo se pondrá en contacto contigo
        </p>

        <div>
          <form
            name="contact"
            method="POST"
            data-netlify="true"
            netlify-honeypot="bot-field"
          >
            <input type="hidden" name="form-name" value="contact" />

            <!-- honeypot anti-spam -->
            <p class="hidden">
              <label>No llenar: <input name="bot-field" /></label>
            </p>

            <div class="grid grid-cols-1 gap-4 mt-4 sm:grid-cols-2">
              <div class="relative w-full">
                <input
                  type="text"
                  id="nombre"
                  required
                  name="nombre"
                  placeholder="Nombre"
                  class="peer w-full border-b-2 border-gray-300 bg-transparent pt-5 pb-2 text-sm text-gray-900 placeholder-transparent focus:border-blue-500 focus:outline-none"
                />
                <label
                  for="nombre"
                  class="absolute left-0 top-2.5 text-gray-500 text-sm transition-all peer-placeholder-shown:top-5 peer-placeholder-shown:text-gray-400 peer-placeholder-shown:text-base peer-focus:top-2.5 peer-focus:text-gray-500 peer-focus:text-sm"
                >
                  Nombre *
                </label>
              </div>
              <div class="relative w-full">
                <input
                  type="text"
                  id="apellido"
                  name="apellido"
                  placeholder="Apellido"
                  class="peer w-full border-b-2 border-gray-300 bg-transparent pt-5 pb-2 text-sm text-gray-900 placeholder-transparent focus:border-blue-500 focus:outline-none"
                />
                <label
                  for="apellido"
                  class="absolute left-0 top-2.5 text-gray-500 text-sm transition-all peer-placeholder-shown:top-5 peer-placeholder-shown:text-gray-400 peer-placeholder-shown:text-base peer-focus:top-2.5 peer-focus:text-gray-500 peer-focus:text-sm"
                >
                  Apellido
                </label>
              </div>
            </div>
            <div class="relative w-full">
              <input
                type="text"
                id="email"
                required
                name="email"
                placeholder="Email"
                class="peer w-full border-b-2 border-gray-300 bg-transparent pt-5 pb-2 text-sm text-gray-900 placeholder-transparent focus:border-blue-500 focus:outline-none"
              />
              <label
                for="email"
                class="absolute left-0 top-2.5 text-gray-500 text-sm transition-all peer-placeholder-shown:top-5 peer-placeholder-shown:text-gray-400 peer-placeholder-shown:text-base peer-focus:top-2.5 peer-focus:text-gray-500 peer-focus:text-sm"
              >
                Email *
              </label>
            </div>
            <div class="relative w-full">
              <input
                type="text"
                id="phone"
                required
                name="phone"
                placeholder="Teléfono"
                class="peer w-full border-b-2 border-gray-300 bg-transparent pt-5 pb-2 text-sm text-gray-900 placeholder-transparent focus:border-blue-500 focus:outline-none"
              />
              <label
                for="phone"
                class="absolute left-0 top-2.5 text-gray-500 text-sm transition-all peer-placeholder-shown:top-5 peer-placeholder-shown:text-gray-400 peer-placeholder-shown:text-base peer-focus:top-2.5 peer-focus:text-gray-500 peer-focus:text-sm"
              >
                Teléfono *
              </label>
            </div>
            <div class="relative w-full">
              <input
                type="text"
                id="business_name"
                required
                name="business_name"
                placeholder="Nombre del Negocio"
                class="peer w-full border-b-2 border-gray-300 bg-transparent pt-5 pb-2 text-sm text-gray-900 placeholder-transparent focus:border-blue-500 focus:outline-none"
              />
              <label
                for="business_name"
                class="absolute left-0 top-2.5 text-gray-500 text-sm transition-all peer-placeholder-shown:top-5 peer-placeholder-shown:text-gray-400 peer-placeholder-shown:text-base peer-focus:top-2.5 peer-focus:text-gray-500 peer-focus:text-sm"
              >
                Nombre del Negocio *
              </label>
            </div>
            <div class="relative w-full">
              <input
                type="text"
                id="type_of_business"
                required
                name="type_of_business"
                placeholder="Tipo de Negocio"
                class="peer w-full border-b-2 border-gray-300 bg-transparent pt-5 pb-2 text-sm text-gray-900 placeholder-transparent focus:border-blue-500 focus:outline-none"
              />
              <label
                for="type_of_business"
                class="absolute left-0 top-2.5 text-gray-500 text-sm transition-all peer-placeholder-shown:top-5 peer-placeholder-shown:text-gray-400 peer-placeholder-shown:text-base peer-focus:top-2.5 peer-focus:text-gray-500 peer-focus:text-sm"
              >
                Tipo de Negocio *
              </label>
            </div>
            <div class="relative w-full">
              <textarea
                id="mensaje"
                name="mensaje"
                placeholder="Cuentanos sobre tus necesidades específicas..."
                rows="4"
                class="peer w-full border-b-2 border-gray-300 bg-transparent pt-5 pb-2 text-sm text-gray-900 placeholder-transparent focus:border-blue-500 focus:outline-none resize-none"
              ></textarea>
              <label
                for="mensaje"
                class="absolute left-0 top-2.5 text-gray-500 text-sm transition-all peer-placeholder-shown:top-5 peer-placeholder-shown:text-gray-400 peer-placeholder-shown:text-base peer-focus:top-2.5 peer-focus:text-gray-500 peer-focus:text-sm"
              >
                Cuentanos sobre tus necesidades específicas...
              </label>
            </div>
            <button
              type="submit"
              class="w-full px-4 py-2 mt-6 text-lg text-white bg-blue-500 rounded-sm hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75 flex justify-center items-center"
            >
              Solicitar Demo Gratuita
              <Icon class="w-4 h-4 ml-2" name="lucide:send" />
            </button>
          </form>
        </div>
      </div>
      <div class="flex flex-col gap-4 h-auto">
        <div
          class="flex flex-col border border-gray-200 shadow-md rounded-lg p-6 bg-blue-50 h-full"
        >
          <h3 class="text-xl font-semibold">Información de Contacto</h3>
          <p class="mt-2 text-gray-600">
            Múltiples formas de ponerte en contacto con nosotros
          </p>

          <div class="mt-4 space-y-4">
            <div class="flex items-center gap-5">
              <Icon class="w-6 h-6 text-blue-500" name="lucide:mail" />
              <div class="flex flex-col">
                <span class="text-xl">Email</span>
                <a
                  href="mailto:kemida.dev@gmail.com"
                  class="text-gray-600 hover:text-blue-500 text-md"
                  >kemida.dev@gmail.com</a
                >
              </div>
            </div>
            <div class="flex items-center gap-5">
              <Icon class="w-6 h-6 text-blue-500" name="lucide:phone" />
              <div class="flex flex-col">
                <span class="text-xl">Teléfono</span>
                <a
                  href="tel:+34633895213"
                  class="text-gray-600 hover:text-blue-500 text-md"
                  >+34 633 895 213</a
                >
              </div>
            </div>
          </div>
        </div>
        <div
          class="flex flex-col border border-gray-200 shadow-md rounded-lg p-6 bg-blue-50 h-full"
        >
          <h3 class="text-xl font-semibold">¿Cómo podemos ayudarte?</h3>
          <p class="mt-2 text-gray-600">
            Transformamos restaurantes con soluciones inteligentes de organización y
            gestión de inventario. Contáctanos para descubrir cómo podemos optimizar tu
            cocina.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
