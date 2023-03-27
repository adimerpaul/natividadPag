<template>
  <q-page>
    <div class="row">
      <div class="col-12 col-md-2"></div>
      <div class="col-12 col-md-8" id="Home">
        <q-carousel arrows animated v-model="slide" height="700px" infinite>
          <q-carousel-slide v-for="s in slides" :key="s.id" :name="s.id" :img-src="`images/slider${conCero(s.id)}.jpg`">
            <div class="absolute-top custom-caption">
              <div class="text-h2">{{ s.titulo }}</div>
              <div class="text-h5">{{ s.subtitulo }}</div>
              <div class="text-body1">{{ s.contenido }}</div>
            </div>
          </q-carousel-slide>
        </q-carousel>
      </div>
      <div class="col-12 col-md-2"></div>
      <div class="col-12 q-pt-lg" id="About">
        <div class="text-subtitle2 text-center text-bold text-primary">OFRECEMOS SERVICIOS</div>
        <div class="text-h3 text-center">Nuestros servicios</div>
      </div>
      <div class="col-6 col-md-4 flex flex-center" v-for="s in services" :key="s.id">
        <q-list>
          <q-item>
            <q-item-section side >
              <q-icon :name="s.icon" color="primary" />
            </q-item-section>
            <q-item-section style="width: 300px">
              <q-item-label>{{s.title}}</q-item-label>
              <q-item-label caption lines="2">{{ s.subtitle }}</q-item-label>
            </q-item-section>
          </q-item>
        </q-list>
      </div>
      <div class="col-12">
        <div class="text-subtitle2 text-center text-bold text-primary">NUESTRO EQUIPO</div>
        <div class="text-h3 text-center">Conoce a nuestro equipo médico</div>
      </div>
      <div class="col-12 col-md-2"></div>
      <div class="col-12 col-md-8" id="Services">
        <q-carousel arrows animated v-model="slide2" height="700px" infinite>
          <q-carousel-slide v-for="s in 11" :key="s" :name="s" :img-src="`images/nos-historia${conCero(s)}.jpg`"/>
        </q-carousel>
      </div>
      <div class="col-12 col-md-2"></div>
      <div class="col-12">
        <div class="text-subtitle2 text-center text-bold text-primary">NUESTRAS INSTALACIONES</div>
        <div class="text-h3 text-center">Conoce nuestras instalaciones</div>
        <div class="text-body1 text-center">Nuestras instalaciones son limpias, seguras y ofrecen comodidad a nuestros pacientes durante su estancia.</div>
      </div>
      <div class="col-12 flex flex-center">
        <q-img  src="images/ind-frontis.jpg" width="400px" />
      </div>
      <div class="col-12">
        <div class="text-subtitle2 text-center text-bold text-primary">NUESTRAS PAGINA DE FACEBOOK</div>
      </div>
      <div class="col-12 flex flex-center">
        <iframe src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FClinica.Natividad.SRL%2Ffollowers&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId=1197266834484792" width="340" height="500" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"></iframe>
      </div>
      <div class="col-12">
        <div class="text-subtitle2 text-center text-bold text-primary">TENEMOS TECNOLOGÍA</div>
        <div class="text-h3 text-center">Conoce nuestra tecnología médica</div>
        <div class="text-body1 text-center">Contamos con tecnología médica avanzada que nos permite ofrecer un diagnóstico preciso y tratamientos efectivos a nuestros pacientes.</div>
      </div>
      <div class="col-12" id="Contact">
        <div class="text-subtitle2 text-center text-bold text-primary">Dirección</div>
        <div class="text-body1 text-center">Bolivar Nº 753, entre Arica e Iquique, Oruro, Bolivia</div>
        <div class="flex flex-center">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2683.544361535934!2d-67.10209399676984!3d-17.97385910908144!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x93e2b0b640c4a4b1%3A0xfb9b2850ef00207d!2sClinica%20Natividad!5e0!3m2!1ses!2sbo!4v1679882636928!5m2!1ses!2sbo" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
      </div>
      <div class="col-12 bg-grey-9">
        <div class="row q-pa-lg">
          <div class="col-6 col-md-4">
            <div class="text-subtitle2 text-center text-bold text-white">Clinica Natividad</div>
            <div class="text-body1 text-justify text-white">Contamos con la mejor infraestructura de Oruro, salas de consulta, habitaciones de internación, Endoscopia, Quirófano, Terapia Intensiva, Ecografía, Rayos X, Laboratorio, con ambientes confortables para la comodidad del paciente.</div>
            <div class="row">
              <div class="col-12 flex flex-center">
                <a href="https://www.facebook.com/Clinica.Natividad.SRL" target="_blank" style="text-decoration: none">
                  <q-icon name="facebook" color="white" size="2.5rem" />
                </a>
              </div>
            </div>
          </div>
          <div class="col-6 col-md-4">
            <div class="text-subtitle2 text-center text-bold text-white">Servicios</div>
            <ul class="text-white">
              <li>Consulta Médica</li>
              <li>Pruebas Diagnósticas</li>
              <li>Tratamientos Especializados</li>
              <li>Atención Urgente</li>
              <li>Internación</li>
              <li>Emergencia</li>
            </ul>
          </div>
          <div class="col-6 col-md-4">
            <div class="text-subtitle2 text-center text-bold text-white">Información</div>
            <ul class="text-white">
              <li>Horario de atención: Lunes a Viernes de 8:00 a 20:00</li>
              <li>Teléfono: 52 54721 - 52 83667</li>
              <li>Correo: clinicanatividad@gmail.com</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage',
  data () {
    return {
      slide: 1,
      slide2: 1,
      slides: [
        {
          id: 1,
          titulo: 'Servicios ofrecidos',
          subtitulo: 'Descubre los diferentes servicios que ofrecemos en nuestra clínica',
          contenido: 'Ofrecemos consultas médicas, pruebas diagnósticas, tratamientos especializados, atención urgente, entre otros.'
        },
        {
          id: 2,
          titulo: 'Equipo médico',
          subtitulo: 'Conoce al equipo de profesionales médicos que trabajan en nuestra clínica',
          contenido: 'Contamos con un equipo de médicos altamente capacitados y con amplia experiencia en diferentes especialidades.'
        },
        {
          id: 3,
          titulo: 'Instalaciones',
          subtitulo: 'Descubre nuestras modernas instalaciones y la comodidad que ofrecemos a nuestros pacientes',
          contenido: 'Nuestras instalaciones son limpias, seguras y ofrecen comodidad a nuestros pacientes durante su estancia.'
        },
        {
          id: 4,
          titulo: 'Tecnología médica',
          subtitulo: 'Conoce nuestra tecnología médica avanzada y cómo nos ayuda en el diagnóstico y tratamiento de nuestros pacientes',
          contenido: 'Contamos con tecnología médica avanzada que nos permite ofrecer un diagnóstico preciso y tratamientos efectivos a nuestros pacientes.'
        },
        {
          id: 5,
          titulo: 'Seguros médicos',
          subtitulo: 'Descubre los diferentes seguros médicos que aceptamos en nuestra clínica',
          contenido: 'Aceptamos una amplia variedad de seguros médicos, para que nuestros pacientes puedan utilizarlos para pagar nuestros servicios.'
        },
        {
          id: 6,
          titulo: 'Testimonios de pacientes',
          subtitulo: 'Lee las experiencias de nuestros pacientes y descubre cómo podemos ayudarte',
          contenido: 'Nuestros pacientes satisfechos comparten sus experiencias con nosotros y cómo han mejorado su salud gracias a nuestros servicios.'
        },
        {
          id: 7,
          titulo: 'Información de contacto',
          subtitulo: 'Contáctanos para más información sobre nuestros servicios',
          contenido: 'Ponte en contacto con nosotros a través de nuestra dirección, número de teléfono, correo electrónico o redes sociales.'
        }
      ],
      services: [
        {
          icon: 'o_medical_services',
          title: 'Consultas médicas',
          subtitle: 'Realizamos consultas médicas en diferentes especialidades'
        },
        {
          icon: 'o_masks',
          title: 'Pruebas diagnósticas',
          subtitle: 'Realizamos pruebas diagnósticas para detectar enfermedades'
        },
        {
          icon: 'o_monitor_heart',
          title: 'Tratamientos especializados',
          subtitle: 'Realizamos tratamientos especializados para diferentes enfermedades'
        },
        {
          icon: 'o_vaccines',
          title: 'Atención urgente',
          subtitle: 'Atendemos casos de urgencia, accidentes de trabajo, entre otros'
        },
        {
          icon: 'o_emergency',
          title: 'Atención emergencia',
          subtitle: 'Ofrecemos atención de emergencia para casos de urgencia, accidentes de trabajo'
        },
        {
          icon: 'o_medical_information',
          title: 'Información médica',
          subtitle: 'Ofrecemos información médica para pacientes y familiares'
        }
      ]
    }
  },
  methods: {
    conCero (i: number) {
      return i < 10 ? `0${i}` : i
    }
  }
})
</script>
<style lang="sass" scoped>
.custom-caption
  text-align: center
  padding: 12px
  color: white
  background-color: rgba(0, 0, 0, .3)
</style>
