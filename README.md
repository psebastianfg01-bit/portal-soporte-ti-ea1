# Portal de Soporte TI — Nova Servicios

## EA1 · Desarrollo de Entornos Web

Landing page responsive para el caso ficticio **Nova Servicios**. Permite consultar servicios de TI, revisar preguntas frecuentes y completar una solicitud de soporte simulada.

> El formulario es únicamente académico: no envía ni guarda tickets.

## Ejecución local

Requisitos: Node.js 22 o superior, Git y VS Code.

```bash
npm ci
npm run dev
```

Abre `http://127.0.0.1:5500` o utiliza Live Server sobre `public/index.html`.

Comprobaciones disponibles:

```bash
npm run format
npm run check
npm run check:syntax
npm test
```

## Estructura

- `public/index.html`: contenido, navegación, servicios, formulario, FAQ y contacto.
- `public/assets/css/styles.css`: CSS externo, responsive, Grid, Flexbox, variables y estados de foco.
- `public/assets/js/ui.js`: apoyo entregado para menú responsive y confirmación del formulario.
- `docs/pruebas.md`: registro de pruebas y evidencias.

## Requisitos implementados

- HTML semántico con `header`, `nav`, `main`, `section`, `article` y `footer`.
- Un solo `h1` y jerarquía ordenada de encabezados.
- `lang="es"`, UTF-8, viewport, `title` y `meta description` propia.
- Navegación con Flexbox y tarjetas con CSS Grid.
- Variables CSS reutilizadas en color, espaciado visual y componentes.
- Selector de atributo (`input[type="email"]` se beneficia de las reglas de formularios) y pseudoclases de interacción/validación.
- Diseño mobile first con cambios en 768 px y 1024 px.
- Formulario con etiquetas visibles, `fieldset`, `legend`, validación nativa, `required`, `minlength` y `maxlength`.
- Foco visible y enlace para saltar al contenido.
- Datos ficticios y mensaje explícito de simulación.

## Decisiones de CSS

Se utiliza una base mobile first para evitar depender de un ancho mínimo y permitir que el contenido funcione desde 320 px. A partir de 768 px, la navegación pasa a una fila y las tarjetas se distribuyen en dos columnas; desde 1024 px se utiliza una cuadrícula de cuatro columnas.

La cascada prioriza componentes específicos sobre las reglas generales. Por ejemplo, `.service-card--featured` modifica la tarjeta destacada sin duplicar todas las propiedades de `.service-card`. Los estados `:hover`, `:focus-visible` e `:invalid` se reservan para interacción y validación, manteniendo visible el foco del teclado.

## Aporte individual EA1

Completar con datos reales antes de entregar:

1. **Ampliación de contenido:** se incorporó el caso Nova Servicios con cuatro servicios, FAQ por categorías, contacto y horario ficticio. Archivo: `public/index.html`.
2. **Mejora técnica HTML/CSS:** se implementó una estructura semántica, formulario accesible, Grid/Flexbox, variables CSS y diseño mobile first. Archivos: `public/index.html` y `public/assets/css/styles.css`.
3. **Corrección detectada en pruebas:** registrar aquí el problema real encontrado, su causa y la corrección aplicada después de probar el portal.

### Dos problemas reales corregidos

Registrar después de ejecutar las pruebas, indicando archivo, problema, causa, cambio, evidencia antes/después y commit.

## Uso de IA / apoyos

Se utilizó ChatGPT como apoyo para interpretar los requisitos de la EA1, organizar la implementación y revisar la estructura del código. El estudiante debe verificar personalmente el funcionamiento, modificar la solución cuando corresponda y poder explicar cada parte durante la demostración.

## Entrega

Completar con datos reales:

- Repositorio: **PENDIENTE**
- Pull Request: **PENDIENTE**
- Preview de Vercel: **PENDIENTE**
- SHA completo del commit evaluado: **PENDIENTE**
- Rama: **PENDIENTE**

## Evidencias

No se inventan resultados de pruebas, Lighthouse ni URLs. Completar `docs/pruebas.md` después de ejecutar cada caso y guardar las capturas solicitadas por la EA1.
