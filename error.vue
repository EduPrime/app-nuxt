<script setup lang="ts">
import { useRouter } from 'vue-router'
import type { NuxtError } from '#app'

// Importar a imagem do diretório assets
import error404Image from '~/assets/img/404-eduprime.webp'
import error500Image from '~/assets/img/500-eduprime.webp'
import errorDefaultImage from '~/assets/img/default-error-page.webp'

const props = defineProps<{ error: NuxtError }>()
const router = useRouter()

const errorImage = computed(() => {
  const statusCode = props.error.statusCode || 0
  if (statusCode === 404)
    return error404Image
  else if (statusCode >= 500 && statusCode < 600)
    return error500Image
  else
    return errorDefaultImage
})

function goHome() {
  router.push('/')
}
</script>

<template>
  <v-container class="fill-height d-flex justify-center align-center text-center ">
    <v-row>
      <v-col cols="12" md="8" lg="6">
        <v-card class="pt-4">
          <v-img
            v-if="errorImage"
            :src="errorImage"
            height="300"
            class="mb-4"
            :alt="`Error ${error.statusCode}`"
          />
          <v-card-text>
            <transition name="scale-transition">
              <div v-if="error.statusCode === 404">
                <h1 class="display-3">
                  Oops! Página não encontrada
                </h1>
                <p class="headline mb-3">
                  Oops! Você encontrou um caminho desconhecido. Não se preocupe, até os melhores exploradores se perdem às vezes!
                </p>
                <v-btn color="primary" @click="goHome">
                  Vamos voltar para casa!
                </v-btn>
              </div>
              <div v-else>
                <h1 class="display-3">
                  Ah não! Algo deu errado
                </h1>
                <p class="headline mb-3">
                  Ops! Algo deu errado nos bastidores. Estamos trabalhando para resolver isso rapidinho. Que tal tentar novamente em instantes?
                </p>
                <v-btn color="error" @click="goHome">
                  Tentar Novamente
                </v-btn>
              </div>
            </transition>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
