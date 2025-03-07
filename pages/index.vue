<script setup lang="ts">
import { Shield } from "lucide-vue-next";
</script>
<template>
  <ScrollArea className=" h-full bg-slate-50 dark:bg-slate-950">
    <header className="bg-gradient-to-r from-blue-900 to-indigo-900 text-white">
      <div className="container mx-auto px-4 py-16 md:py-24">
        <div className="max-w-4xl">
          <h1 className="text-3xl md:text-5xl font-bold mb-4">
            Las Ciencias Informáticas al Servicio de la Seguridad y la Defensa
            Nacional
          </h1>
          <p className="text-xl md:text-2xl text-blue-100 mb-8">
            Innovación, tecnología y protección en la era digital
          </p>
        </div>
      </div>
    </header>

    <main className="container mx-auto px-4 py-12">
      <section className="mb-16">
        <h2
          className="text-3xl font-bold mb-6 text-slate-800 dark:text-slate-100"
        >
          Visión General
        </h2>
        <div className="grid md:grid-cols-2 gap-8">
          <div>
            <p className="text-lg text-slate-700 dark:text-slate-300 mb-4">
              La convergencia entre las ciencias informáticas y la seguridad
              nacional implica el desarrollo y la aplicación de herramientas
              tecnológicas que abarcan desde la ciberseguridad hasta el análisis
              de datos masivos.
            </p>
            <p className="text-lg text-slate-700 dark:text-slate-300">
              Este portal se dedica a explorar cómo la innovación en áreas como
              la inteligencia artificial, el big data, la criptografía y las
              comunicaciones seguras está redefiniendo los métodos tradicionales
              de defensa, adaptándose a los desafíos de un entorno digital en
              constante evolución.
            </p>
          </div>
          <div
            className="bg-blue-800 rounded-lg p-8 text-white flex items-center justify-center"
          >
            <div className="flex flex-col items-center text-center">
              <Shield className="w-32 h-32 mx-auto mb-4" />
              <h3 className="text-xl font-semibold mb-2">Protección Digital</h3>
              <p>
                Soluciones tecnológicas avanzadas para la defensa y seguridad
                nacional en la era digital
              </p>
            </div>
          </div>
        </div>
      </section>

      <section className="mb-16">
        <h2
          className="text-3xl font-bold mb-6 text-slate-800 dark:text-slate-100"
        >
          Principales Conceptos y Herramientas
        </h2>

        <Tabs defaultValue="cybersecurity" className="w-full">
          <TabsList className="grid grid-cols-2 md:grid-cols-4 mb-8">
            <TabsTrigger value="cybersecurity">Ciberseguridad</TabsTrigger>
            <TabsTrigger value="ai">IA y Big Data</TabsTrigger>
            <TabsTrigger value="crypto">Criptografía</TabsTrigger>
            <TabsTrigger value="networks">Redes</TabsTrigger>
          </TabsList>

          <TabsContent value="cybersecurity" className="space-y-4">
            <TabCard
              title="Ciberseguridad y Ciberdefensa"
              description="Protección de sistemas informáticos y redes ante accesos no autorizados"
              content="La ciberseguridad se encarga de proteger los sistemas informáticos y redes ante accesos no autorizados, ataques maliciosos o vulnerabilidades que puedan comprometer la integridad de la información. Dentro de este ámbito, la ciberdefensa se enfoca en la detección, prevención y respuesta ante ciberataques que amenacen infraestructuras críticas, asegurando la continuidad de servicios esenciales en sectores estratégicos como energía, comunicaciones y transporte."
            />
          </TabsContent>

          <TabsContent value="ai" className="space-y-4">
            <TabCard
              title="Inteligencia Artificial y Big Data"
              description="Análisis de grandes volúmenes de información para la toma de decisiones estratégicas"
              content="La inteligencia artificial (IA) y el big data han revolucionado la capacidad para analizar enormes volúmenes de información. Estos avances permiten identificar patrones, predecir comportamientos y facilitar la toma de decisiones estratégicas. En el contexto de la seguridad, la IA se utiliza para: Detectar actividades sospechosas en tiempo real. Automatizar respuestas a incidentes de seguridad. Simular escenarios de conflicto y modelar posibles amenazas."
            />
          </TabsContent>

          <TabsContent value="crypto" className="space-y-4">
            <TabCard
              title="Criptografía y Comunicaciones Seguras"
              description="Garantía de confidencialidad e integridad de la información"
              content="La criptografía es fundamental para garantizar la confidencialidad e integridad de la información, utilizando algoritmos que permiten el cifrado de datos sensibles. Las comunicaciones seguras aseguran que la transmisión de información crítica entre entidades gubernamentales, militares y organizaciones estratégicas se realice sin riesgo de interceptación o manipulación, protegiendo así la soberanía y la seguridad nacional."
            />
          </TabsContent>

          <TabsContent value="networks" className="space-y-4">
            <TabCard
              title="Redes y Sistemas de Información"
              description="Diseño y mantenimiento de infraestructuras de red seguras"
              content="El diseño y mantenimiento de infraestructuras de red seguras es esencial para la defensa nacional. La interconexión de dispositivos y sistemas requiere protocolos robustos y sistemas de monitoreo que detecten y mitiguen vulnerabilidades, garantizando la resiliencia frente a ataques cibernéticos y fallas operativas."
            />
          </TabsContent>
        </Tabs>
      </section>

      <section className="mb-16">
        <h2
          className="text-3xl font-bold mb-6 text-slate-800 dark:text-slate-100"
        >
          Aplicaciones Prácticas en la Seguridad Nacional
        </h2>

        <div className="grid md:grid-cols-3 gap-6">
          <Card>
            <CardHeader>
              <CardTitle className="flex items-center">
                <Building className="mr-2 h-6 w-6 text-blue-600" />
                Protección de Infraestructuras Críticas
              </CardTitle>
            </CardHeader>
            <CardContent>
              <p className="text-slate-700 dark:text-slate-300">
                La tecnología informática permite la supervisión y defensa de
                instalaciones y servicios que son vitales para el funcionamiento
                del país. Desde centrales eléctricas hasta sistemas de
                transporte, la aplicación de técnicas de análisis en tiempo real
                y la implementación de medidas de seguridad digital contribuyen
                a minimizar riesgos y prevenir daños mayores.
              </p>
            </CardContent>
          </Card>

          <Card>
            <CardHeader>
              <CardTitle className="flex items-center">
                <Clock className="mr-2 h-6 w-6 text-blue-600" />
                Gestión de Crisis y Respuesta Rápida
              </CardTitle>
            </CardHeader>
            <CardContent>
              <p className="text-slate-700 dark:text-slate-300">
                Durante situaciones de emergencia o crisis, las plataformas
                digitales integran datos de múltiples fuentes para ofrecer una
                visión unificada del escenario. Esto facilita la coordinación
                interinstitucional, optimizando la respuesta y permitiendo una
                toma de decisiones basada en información precisa y actualizada.
              </p>
            </CardContent>
          </Card>

          <Card>
            <CardHeader>
              <CardTitle className="flex items-center">
                <ChartBar className="mr-2 h-6 w-6 text-blue-600" />
                Simulaciones y Análisis Predictivo
              </CardTitle>
            </CardHeader>
            <CardContent>
              <p className="text-slate-700 dark:text-slate-300">
                El uso de simulaciones y modelos predictivos es una herramienta
                poderosa en la planificación estratégica. A través del análisis
                de datos y la inteligencia artificial, es posible prever
                escenarios de ciberataques o amenazas convencionales,
                permitiendo a las autoridades preparar planes de contingencia y
                estrategias de defensa proactivas.
              </p>
            </CardContent>
          </Card>
        </div>
      </section>

      <section className="mb-16">
        <h2
          className="text-3xl font-bold mb-6 text-slate-800 dark:text-slate-100"
        >
          Nuestro Compromiso y Visión a Futuro
        </h2>

        <Card
          className="bg-gradient-to-r from-blue-50 to-indigo-50 dark:from-blue-950 dark:to-indigo-950 border-0 shadow-md"
        >
          <CardContent className="p-8">
            <p className="text-lg text-slate-700 dark:text-slate-300 mb-4">
              Creemos firmemente que la transformación digital y la integración
              de las ciencias informáticas son clave para construir un futuro
              más seguro y resiliente. Este portal es una invitación a explorar
              y comprender cómo la tecnología puede ser utilizada para
              fortalecer la defensa nacional, anticipar amenazas y promover la
              seguridad en un entorno cada vez más complejo.
            </p>
            <p className="text-lg text-slate-700 dark:text-slate-300 mb-6">
              Con un enfoque en la investigación, la formación y la colaboración
              interinstitucional, aspiramos a ser un punto de referencia para
              estudiantes, profesionales y cualquier persona interesada en la
              intersección de la tecnología y la seguridad. Te invitamos a
              explorar, aprender y sumarte a una comunidad comprometida con la
              innovación y la protección de nuestro país en la era digital.
            </p>
          </CardContent>
        </Card>
      </section>
    </main>

    <footer className="bg-slate-900 text-white py-12">
      <div className="container mx-auto px-4">
        <div className="grid md:grid-cols-3 gap-8">
          <div>
            <h3 className="text-xl font-bold mb-4 items-center">
              Ciencias Informáticas para la Seguridad
            </h3>
            <p className="text-slate-300">
              Innovación, tecnología y protección en la era digital
            </p>
          </div>
          <div>
            <h3 className="text-xl font-bold mb-4">Enlaces Rápidos</h3>
            <ul className="space-y-2">
              <li>
                <a href="#" className="text-slate-300 hover:text-white">
                  Inicio
                </a>
              </li>
              <li>
                <NuxtLink
                  to="/vista2"
                  className="text-slate-300 hover:text-white"
                >
                  Recursos
                </NuxtLink>
              </li>

              <li>
                <NuxtLink
                  to="https://www.uci.cu/"
                  target="_blank"
                  className="text-slate-300 hover:text-white"
                >
                  Enlace a la universidad
                </NuxtLink>
              </li>
            </ul>
          </div>
          <div>
            <h3 className="text-xl font-bold mb-4">Contacto</h3>
            <p className="text-slate-300 mb-2">sailyhg@uci.cu</p>
          </div>
        </div>
        <div
          className="border-t border-slate-700 mt-8 pt-8 text-center text-slate-400"
        >
          <p>
            {{
              `© ${new Date().getFullYear()} Ciencias Informáticas para la Seguridad
            y Defensa Nacional. Todos los derechos reservados.`
            }}
          </p>
        </div>
      </div>
    </footer>
  </ScrollArea>
</template>
