# Guía Completa de Librerías React

## 🚀 Decisiones Rápidas

### ¿Qué usar si necesitas...?

| **Necesidad** | **Recomendación Principal** | **Alternativa** | **Para Expertos** |
|---------------|----------------------------|-----------------|-------------------|
| **UI Components** | Material-UI (@mui/material) | Ant Design (antd) | Radix UI + Tailwind |
| **Styling** | Tailwind CSS | Styled Components | Emotion |
| **Estado Global** | Zustand | Redux Toolkit | Jotai |
| **Formularios** | React Hook Form | Formik | React Final Form |
| **Routing** | React Router | Next.js Router | Tanstack Router |
| **Fetching Datos** | Tanstack Query | SWR | Apollo Client |
| **Animaciones** | Framer Motion | React Spring | Lottie React |
| **Testing** | Testing Library | Vitest | Playwright |
| **Fechas** | date-fns | Day.js | Luxon |
| **Gráficos** | Recharts | Chart.js | D3.js |

### 📊 Por Tipo de Proyecto

- **🏢 Aplicación Empresarial**: Ant Design + Redux Toolkit + React Router + Axios
- **🎨 Portfolio/Landing**: Next.js + Tailwind + Framer Motion + Headless UI
- **📱 App Móvil**: React Native + React Navigation + Zustand + React Hook Form
- **🛒 E-commerce**: Next.js + Material-UI + Tanstack Query + Stripe
- **📊 Dashboard**: Tremor + Recharts + Tanstack Table + React Hook Form

### 🎯 Por Nivel de Experiencia

**🟢 Principiante**
```bash
npm i react react-dom react-router-dom @mui/material axios react-hook-form
```

**🟡 Intermedio**
```bash
npm i @tanstack/react-query zustand framer-motion @headlessui/react tailwindcss
```

**🔴 Avanzado**
```bash
npm i @radix-ui/react-dialog @tanstack/react-table viem wagmi @react-three/fiber
```

---

## 📋 Índice
- [UI Components & Design Systems](#ui-components--design-systems)
- [Styling](#styling)
- [State Management](#state-management)
- [Routing](#routing)
- [Forms & Validation](#forms--validation)
- [HTTP Client & API](#http-client--api)
- [Animation](#animation)
- [Icons](#icons)
- [Dates & Time](#dates--time)
- [Charts & Data Visualization](#charts--data-visualization)
- [Testing](#testing)
- [Development Tools](#development-tools)
- [File Upload & Handling](#file-upload--handling)
- [Internationalization (i18n)](#internationalization-i18n)
- [Security](#security)
- [Performance](#performance)
- [Mobile & PWA](#mobile--pwa)
- [Server-Side Rendering (SSR/SSG)](#server-side-rendering-ssrssg)
- [Game Development](#game-development)
- [Cross-Platform](#cross-platform)
- [AI/ML Integration](#aiml-integration)
- [Blockchain/Web3](#blockchainweb3)
- [Business Intelligence](#business-intelligence)
- [Utilities](#utilities)

---

## 🎨 UI Components & Design Systems

### Material-UI (MUI)
Sistema de componentes basado en Material Design de Google. Ofrece componentes pre-construidos con tema personalizable.

**✅ Cuándo usar**: Aplicaciones empresariales, dashboards, cuando necesitas componentes robustos out-of-the-box.
**❌ Cuándo NO usar**: Diseños muy personalizados, aplicaciones que requieren bundle size mínimo.

```bash
npm i @mui/material @emotion/react @emotion/styled  # Componentes principales
npm i @mui/icons-material  # Iconos de Material Design
npm i @mui/lab  # Componentes experimentales
npm i @mui/x-data-grid  # Tabla de datos avanzada
npm i @mui/x-date-pickers  # Selectores de fecha y hora
```

**📦 Enlaces npm**:
- [@mui/material](https://www.npmjs.com/package/@mui/material)
- [@emotion/react](https://www.npmjs.com/package/@emotion/react)
- [@emotion/styled](https://www.npmjs.com/package/@emotion/styled)
- [@mui/icons-material](https://www.npmjs.com/package/@mui/icons-material)
- [@mui/lab](https://www.npmjs.com/package/@mui/lab)
- [@mui/x-data-grid](https://www.npmjs.com/package/@mui/x-data-grid)
- [@mui/x-date-pickers](https://www.npmjs.com/package/@mui/x-date-pickers)

**Ejemplo básico**:
```jsx
import { Button, TextField, Box } from '@mui/material';

function LoginForm() {
  return (
    <Box sx={{ display: 'flex', flexDirection: 'column', gap: 2 }}>
      <TextField label="Email" variant="outlined" />
      <TextField label="Password" type="password" variant="outlined" />
      <Button variant="contained" color="primary">Login</Button>
    </Box>
  );
}
```

### Ant Design
Librería de componentes empresariales con diseño profesional y consistente. Ideal para aplicaciones de administración.
```bash
npm i antd  # Librería principal de componentes
npm i @ant-design/icons  # Iconos oficiales de Ant Design
npm i @ant-design/charts  # Gráficos integrados
npm i @ant-design/pro-components  # Componentes avanzados para aplicaciones pro
```

**📦 Enlaces npm**:
- [antd](https://www.npmjs.com/package/antd)
- [@ant-design/icons](https://www.npmjs.com/package/@ant-design/icons)
- [@ant-design/charts](https://www.npmjs.com/package/@ant-design/charts)
- [@ant-design/pro-components](https://www.npmjs.com/package/@ant-design/pro-components)

### Chakra UI
Sistema de componentes modulares, accesibles y simples. Fácil personalización con tokens de diseño.
```bash
npm i @chakra-ui/react @emotion/react @emotion/styled framer-motion  # Core + animaciones
npm i @chakra-ui/icons  # Iconos integrados
```

**📦 Enlaces npm**:
- [@chakra-ui/react](https://www.npmjs.com/package/@chakra-ui/react)
- [@emotion/react](https://www.npmjs.com/package/@emotion/react)
- [@emotion/styled](https://www.npmjs.com/package/@emotion/styled)
- [framer-motion](https://www.npmjs.com/package/framer-motion)
- [@chakra-ui/icons](https://www.npmjs.com/package/@chakra-ui/icons)

### Mantine
Librería moderna con muchos hooks útiles y componentes personalizables. Excelente experiencia de desarrollo.
```bash
npm i @mantine/core @mantine/hooks  # Componentes principales y hooks
npm i @mantine/dates  # Componentes de fecha
npm i @mantine/notifications  # Sistema de notificaciones
npm i @mantine/modals  # Sistema de modales
npm i @mantine/spotlight  # Búsqueda tipo comando palette
```

**📦 Enlaces npm**:
- [@mantine/core](https://www.npmjs.com/package/@mantine/core)
- [@mantine/hooks](https://www.npmjs.com/package/@mantine/hooks)
- [@mantine/dates](https://www.npmjs.com/package/@mantine/dates)
- [@mantine/notifications](https://www.npmjs.com/package/@mantine/notifications)
- [@mantine/modals](https://www.npmjs.com/package/@mantine/modals)
- [@mantine/spotlight](https://www.npmjs.com/package/@mantine/spotlight)

### Headless UI
Componentes sin estilos pero con lógica completa. Perfectos para usar con Tailwind CSS y máxima personalización.
```bash
npm i @headlessui/react  # Componentes headless
npm i @headlessui/tailwindcss  # Integración con Tailwind
```

**📦 Enlaces npm**:
- [@headlessui/react](https://www.npmjs.com/package/@headlessui/react)
- [@headlessui/tailwindcss](https://www.npmjs.com/package/@headlessui/tailwindcss)

### React Bootstrap
Implementación de Bootstrap para React. Familiar para desarrolladores que conocen Bootstrap.
```bash
npm i react-bootstrap bootstrap  # Componentes Bootstrap para React
npm i react-bootstrap-icons  # Iconos de Bootstrap
```

**📦 Enlaces npm**:
- [react-bootstrap](https://www.npmjs.com/package/react-bootstrap)
- [bootstrap](https://www.npmjs.com/package/bootstrap)
- [react-bootstrap-icons](https://www.npmjs.com/package/react-bootstrap-icons)

### Semantic UI React
Implementación de Semantic UI para React. Enfoque en HTML semántico y clases CSS intuitivas.
```bash
npm i semantic-ui-react semantic-ui-css  # Componentes y estilos
```

**📦 Enlaces npm**:
- [semantic-ui-react](https://www.npmjs.com/package/semantic-ui-react)
- [semantic-ui-css](https://www.npmjs.com/package/semantic-ui-css)

### Blueprint
Librería de componentes para aplicaciones web complejas y de escritorio. Optimizada para densidad de información.
```bash
npm i @blueprintjs/core @blueprintjs/icons  # Componentes principales
npm i @blueprintjs/select  # Componentes de selección avanzados
npm i @blueprintjs/table  # Tablas complejas
```

**📦 Enlaces npm**:
- [@blueprintjs/core](https://www.npmjs.com/package/@blueprintjs/core)
- [@blueprintjs/icons](https://www.npmjs.com/package/@blueprintjs/icons)
- [@blueprintjs/select](https://www.npmjs.com/package/@blueprintjs/select)
- [@blueprintjs/table](https://www.npmjs.com/package/@blueprintjs/table)

### Arco Design
Sistema de diseño empresarial de ByteDance. Componentes de alta calidad para aplicaciones profesionales.
```bash
npm i @arco-design/web-react  # Componentes principales
npm i @arco-design/web-react-icon  # Iconos integrados
```

**📦 Enlaces npm**:
- [@arco-design/web-react](https://www.npmjs.com/package/@arco-design/web-react)
- [@arco-design/web-react-icon](https://www.npmjs.com/package/@arco-design/web-react-icon)

### Radix UI
Primitivos de UI headless de alta calidad con accesibilidad completa.
```bash
npm i @radix-ui/react-dialog  # Modales y diálogos accesibles
npm i @radix-ui/react-dropdown-menu  # Menús desplegables
npm i @radix-ui/react-select  # Selectores accesibles
npm i @radix-ui/react-toast  # Notificaciones toast
npm i @radix-ui/react-tooltip  # Tooltips accesibles
```

**📦 Enlaces npm**:
- [@radix-ui/react-dialog](https://www.npmjs.com/package/@radix-ui/react-dialog)
- [@radix-ui/react-dropdown-menu](https://www.npmjs.com/package/@radix-ui/react-dropdown-menu)
- [@radix-ui/react-select](https://www.npmjs.com/package/@radix-ui/react-select)
- [@radix-ui/react-toast](https://www.npmjs.com/package/@radix-ui/react-toast)
- [@radix-ui/react-tooltip](https://www.npmjs.com/package/@radix-ui/react-tooltip)

### React Aria
Hooks de accesibilidad y comportamiento de Adobe para componentes personalizados.
```bash
npm i react-aria  # Hooks de comportamiento y accesibilidad
npm i react-stately  # Hooks de estado para componentes
npm i @react-aria/interactions  # Interacciones táctiles y de teclado
```

**📦 Enlaces npm**:
- [react-aria](https://www.npmjs.com/package/react-aria)
- [react-stately](https://www.npmjs.com/package/react-stately)
- [@react-aria/interactions](https://www.npmjs.com/package/@react-aria/interactions)

### Shadcn/ui
Componentes copiables construidos con Radix UI y Tailwind CSS.
```bash
npx shadcn-ui@latest init  # Inicializar shadcn/ui en el proyecto
npx shadcn-ui@latest add button  # Agregar componentes específicos
npx shadcn-ui@latest add dialog  # Ejemplo: agregar componente dialog
```

---

## 🎭 Styling

### CSS-in-JS
Soluciones para escribir CSS dentro de JavaScript con scope automático y temas dinámicos.
```bash
npm i styled-components  # La librería CSS-in-JS más popular
npm i @emotion/styled @emotion/react  # Alternative moderna a styled-components
npm i @stitches/react  # CSS-in-JS con performance optimizada
npm i goober  # Librería CSS-in-JS ultra ligera (menos de 1KB)
```

**📦 Enlaces npm**:
- [styled-components](https://www.npmjs.com/package/styled-components)
- [@emotion/styled](https://www.npmjs.com/package/@emotion/styled)
- [@emotion/react](https://www.npmjs.com/package/@emotion/react)
- [@stitches/react](https://www.npmjs.com/package/@stitches/react)
- [goober](https://www.npmjs.com/package/goober)

### CSS Frameworks Integration
Integración de frameworks CSS populares con React.
```bash
npm i tailwindcss  # Framework CSS utility-first
npm i bootstrap  # Framework CSS más popular
npm i bulma  # Framework CSS moderno basado en Flexbox
npm i @twind/core @twind/preset-autoprefix @twind/preset-tailwind  # Tailwind-in-JS
```

**📦 Enlaces npm**:
- [tailwindcss](https://www.npmjs.com/package/tailwindcss)
- [bootstrap](https://www.npmjs.com/package/bootstrap)
- [bulma](https://www.npmjs.com/package/bulma)
- [@twind/core](https://www.npmjs.com/package/@twind/core)
- [@twind/preset-autoprefix](https://www.npmjs.com/package/@twind/preset-autoprefix)
- [@twind/preset-tailwind](https://www.npmjs.com/package/@twind/preset-tailwind)

### CSS Modules & PostCSS
Herramientas para manejo de CSS modular y procesamiento de estilos.
```bash
npm i classnames  # Utilidad para combinar clases CSS condicionalmente
npm i clsx  # Alternativa más ligera y rápida a classnames
npm i postcss  # Procesador de CSS con plugins
npm i autoprefixer  # Plugin para agregar prefijos CSS automáticamente
```

**📦 Enlaces npm**:
- [classnames](https://www.npmjs.com/package/classnames)
- [clsx](https://www.npmjs.com/package/clsx)
- [postcss](https://www.npmjs.com/package/postcss)
- [autoprefixer](https://www.npmjs.com/package/autoprefixer)

---

## 🗃️ State Management

### Redux Ecosystem
Librería de gestión de estado predecible con herramientas modernas y middleware.
```bash
npm i @reduxjs/toolkit react-redux  # Redux moderno con menos boilerplate
npm i redux-persist  # Persistencia del estado en localStorage/sessionStorage
npm i redux-thunk  # Middleware para acciones asíncronas (incluido en RTK)
npm i reselect  # Selectores memoizados para performance
```

**📦 Enlaces npm**:
- [@reduxjs/toolkit](https://www.npmjs.com/package/@reduxjs/toolkit)
- [react-redux](https://www.npmjs.com/package/react-redux)
- [redux-persist](https://www.npmjs.com/package/redux-persist)
- [redux-thunk](https://www.npmjs.com/package/redux-thunk)
- [reselect](https://www.npmjs.com/package/reselect)

### Context & Hooks
Librerías de estado ligeras basadas en hooks y context de React.
```bash
npm i zustand  # Gestión de estado simple y sin boilerplate
npm i jotai  # Gestión de estado atómica (bottom-up)
npm i valtio  # Estado proxy-based con mutaciones directas
npm i hookstate  # Estado local y global con hooks simples
```

**📦 Enlaces npm**:
- [zustand](https://www.npmjs.com/package/zustand)
- [jotai](https://www.npmjs.com/package/jotai)
- [valtio](https://www.npmjs.com/package/valtio)
- [hookstate](https://www.npmjs.com/package/hookstate)

### Zustand
Gestión de estado simple y sin boilerplate.

**✅ Cuándo usar**: Proyectos pequeños a medianos, cuando quieres simplicidad, estado compartido mínimo.
**❌ Cuándo NO usar**: Aplicaciones muy complejas con muchos desarrolladores, cuando necesitas time-travel debugging.

**Ejemplo básico**:
```jsx
import { create } from 'zustand';

const useStore = create((set) => ({
  count: 0,
  increment: () => set((state) => ({ count: state.count + 1 })),
  decrement: () => set((state) => ({ count: state.count - 1 })),
}));

function Counter() {
  const { count, increment, decrement } = useStore();
  return (
    <div>
      <span>{count}</span>
      <button onClick={increment}>+</button>
      <button onClick={decrement}>-</button>
    </div>
  );
}
```

### Zustand
Gestión de estado simple y sin boilerplate.

**✅ Cuándo usar**: Proyectos pequeños a medianos, cuando quieres simplicidad, estado compartido mínimo.
**❌ Cuándo NO usar**: Aplicaciones muy complejas con muchos desarrolladores, cuando necesitas time-travel debugging.

**Ejemplo básico**:
```jsx
import { create } from 'zustand';

const useStore = create((set) => ({
  count: 0,
  increment: () => set((state) => ({ count: state.count + 1 })),
  decrement: () => set((state) => ({ count: state.count - 1 })),
}));

function Counter() {
  const { count, increment, decrement } = useStore();
  return (
    <div>
      <span>{count}</span>
      <button onClick={increment}>+</button>
      <button onClick={decrement}>-</button>
    </div>
  );
}
```

### Server State
Especializado en caché y sincronización de datos del servidor.

#### Tanstack Query (React Query)
**✅ Cuándo usar**: APIs REST, caché inteligente, sincronización automática, optimistic updates.
**❌ Cuándo NO usar**: Aplicaciones completamente estáticas, cuando no necesitas caché.

```bash
npm i @tanstack/react-query  # Caché, sincronización y gestión de estado del servidor
```

**Ejemplo básico**:
```jsx
import { useQuery, useMutation, useQueryClient } from '@tanstack/react-query';

function UserProfile({ userId }) {
  const queryClient = useQueryClient();
  
  const { data: user, isLoading, error } = useQuery({
    queryKey: ['user', userId],
    queryFn: () => fetch(`/api/users/${userId}`).then(res => res.json()),
    staleTime: 5 * 60 * 1000, // 5 minutos
  });

  const updateUserMutation = useMutation({
    mutationFn: (userData) => fetch(`/api/users/${userId}`, {
      method: 'PUT',
      body: JSON.stringify(userData),
    }),
    onSuccess: () => {
      queryClient.invalidateQueries(['user', userId]);
    },
  });

  if (isLoading) return <div>Loading...</div>;
  if (error) return <div>Error: {error.message}</div>;

  return (
    <div>
      <h1>{user.name}</h1>
      <button onClick={() => updateUserMutation.mutate({ name: 'New Name' })}>
        Update Name
      </button>
    </div>
  );
}
```

#### Otras librerías de server state
```bash
npm i swr  # Fetching de datos con caché y revalidación
npm i apollo-client @apollo/client graphql  # Cliente GraphQL completo
npm i urql  # Cliente GraphQL ligero y extensible
```

**📦 Enlaces npm**:
- [@tanstack/react-query](https://www.npmjs.com/package/@tanstack/react-query)
- [swr](https://www.npmjs.com/package/swr)
- [apollo-client](https://www.npmjs.com/package/apollo-client)
- [@apollo/client](https://www.npmjs.com/package/@apollo/client)
- [graphql](https://www.npmjs.com/package/graphql)
- [urql](https://www.npmjs.com/package/urql)

---

## 🛣️ Routing

### React Router
El estándar de facto para routing en aplicaciones React SPA.
```bash
npm i react-router-dom  # Router principal para aplicaciones web
# @reach/router está deprecated - usar React Router v6 que incluye sus funcionalidades
npm i history  # Manejo del historial del navegador
```

**📦 Enlaces npm**:
- [react-router-dom](https://www.npmjs.com/package/react-router-dom)
- [history](https://www.npmjs.com/package/history)

### Next.js Router
Routing basado en archivos para aplicaciones Next.js con SSR/SSG.
```bash
npm i next  # Framework full-stack con routing integrado
```

**📦 Enlaces npm**:
- [next](https://www.npmjs.com/package/next)

### Alternative Routers
Alternativas ligeras y modernas para routing.
```bash
npm i @tanstack/react-router  # Router type-safe con validación de rutas
npm i wouter  # Router minimalista (menos de 2KB)
npm i reach-router  # Router simple (ahora parte de React Router v6)
npm i @remix-run/router  # Router core usado por React Router v6
```

**📦 Enlaces npm**:
- [@tanstack/react-router](https://www.npmjs.com/package/@tanstack/react-router)
- [wouter](https://www.npmjs.com/package/wouter)
- [reach-router](https://www.npmjs.com/package/reach-router)
- [@remix-run/router](https://www.npmjs.com/package/@remix-run/router)

---

## 📝 Forms & Validation

### Form Libraries
Librerías para manejo eficiente de formularios con validación y performance optimizada.

#### React Hook Form
**✅ Cuándo usar**: Formularios performantes, validación compleja, integración con librerías de validación.
**❌ Cuándo NO usar**: Formularios muy simples donde el estado local es suficiente.

```bash
npm i react-hook-form  # Formularios performantes con mínimas re-renders
npm i @hookform/resolvers  # Adaptadores para validadores
```

**Ejemplo con validación**:
```jsx
import { useForm } from 'react-hook-form';
import { yupResolver } from '@hookform/resolvers/yup';
import * as yup from 'yup';

const schema = yup.object({
  email: yup.string().email().required(),
  password: yup.string().min(6).required(),
});

function LoginForm() {
  const { register, handleSubmit, formState: { errors } } = useForm({
    resolver: yupResolver(schema)
  });

  const onSubmit = (data) => console.log(data);

  return (
    <form onSubmit={handleSubmit(onSubmit)}>
      <input {...register('email')} placeholder="Email" />
      {errors.email && <span>{errors.email.message}</span>}
      
      <input {...register('password')} type="password" placeholder="Password" />
      {errors.password && <span>{errors.password.message}</span>}
      
      <button type="submit">Submit</button>
    </form>
  );
}
```

#### Otras librerías de formularios
```bash
npm i formik  # Librería popular para formularios complejos
npm i react-final-form final-form  # Formularios con subscripción granular
npm i @mantine/form  # Formularios integrados con Mantine
```

**📦 Enlaces npm**:
- [react-hook-form](https://www.npmjs.com/package/react-hook-form)
- [@hookform/resolvers](https://www.npmjs.com/package/@hookform/resolvers)
- [formik](https://www.npmjs.com/package/formik)
- [react-final-form](https://www.npmjs.com/package/react-final-form)
- [final-form](https://www.npmjs.com/package/final-form)
- [@mantine/form](https://www.npmjs.com/package/@mantine/form)

### Validation
Esquemas de validación para datos de formularios y APIs.
```bash
npm i yup  # Validación de esquemas con sintaxis fluida
npm i zod  # Validación TypeScript-first con inferencia de tipos
npm i joi  # Validación potente para objetos JavaScript
npm i @hookform/resolvers  # Adaptadores para usar validadores con react-hook-form
```

**📦 Enlaces npm**:
- [yup](https://www.npmjs.com/package/yup)
- [zod](https://www.npmjs.com/package/zod)
- [joi](https://www.npmjs.com/package/joi)
- [@hookform/resolvers](https://www.npmjs.com/package/@hookform/resolvers)

### Form Components
Componentes especializados para inputs complejos en formularios.
```bash
npm i react-select  # Select avanzado con búsqueda, multi-select, async
npm i react-datepicker  # Selector de fechas personalizable
npm i react-dropzone  # Área de drag & drop para archivos
npm i react-slider  # Sliders y range inputs personalizables
```

**📦 Enlaces npm**:
- [react-select](https://www.npmjs.com/package/react-select)
- [react-datepicker](https://www.npmjs.com/package/react-datepicker)
- [react-dropzone](https://www.npmjs.com/package/react-dropzone)
- [react-slider](https://www.npmjs.com/package/react-slider)

---

## 🌐 HTTP Client & API

### HTTP Clients
Clientes HTTP para realizar peticiones a APIs con interceptores y configuración.
```bash
npm i axios  # Cliente HTTP más popular con interceptores
npm i ky  # Cliente HTTP moderno basado en fetch
npm i got  # Cliente HTTP para Node.js (no para browser)
npm i node-fetch  # Implementación de fetch para Node.js
```

### GraphQL
Clientes y herramientas para trabajar con APIs GraphQL.
```bash
npm i @apollo/client graphql  # Cliente GraphQL completo con caché normalizado
npm i urql  # Cliente GraphQL más ligero y modular
npm i graphql-request  # Cliente GraphQL minimalista
npm i relay-runtime react-relay  # Cliente GraphQL de Facebook (complejo pero potente)
```

### Mock & Testing
Herramientas para simular APIs durante desarrollo y testing.
```bash
npm i msw  # Service Worker para interceptar requests HTTP
npm i json-server  # API REST falsa desde archivo JSON
npm i miragejs  # Servidor de API simulada para frontend
```

---

## ✨ Animation

### Animation Libraries
Librerías para crear animaciones fluidas y transiciones en React.
```bash
npm i framer-motion  # Librería de animación más potente y popular
npm i react-spring  # Animaciones basadas en spring physics
npm i react-transition-group  # Transiciones para componentes que se montan/desmontan
npm i lottie-react  # Reproduce animaciones Lottie (After Effects)
npm i react-reveal  # Animaciones de entrada al scroll
npm i aos  # Animate On Scroll - animaciones simples al hacer scroll
```

### CSS Animation Utilities
Utilidades y helpers para animaciones CSS.
```bash
npm i animate.css  # Librería CSS con animaciones predefinidas
npm i react-animate-height  # Animación de altura automática
npm i react-flip-move  # Animaciones FLIP para listas que cambian
```

---

## 🎯 Icons

### Icon Libraries
Colecciones de iconos como componentes React listos para usar.
```bash
npm i @heroicons/react  # Iconos Heroicons diseñados por creadores de Tailwind
npm i react-icons  # Mega librería con iconos de Font Awesome, Material, etc.
npm i @tabler/icons-react  # Iconos Tabler minimalistas y consistentes
npm i lucide-react  # Fork de Feather icons con más iconos
npm i @phosphor-icons/react  # Familia de iconos flexible con pesos variables
npm i react-feather  # Iconos Feather simples y elegantes
```

### Brand Icons
Iconos de marcas y redes sociales.
```bash
npm i @fortawesome/fontawesome-svg-core  # Core de Font Awesome
npm i @fortawesome/free-solid-svg-icons  # Iconos sólidos gratuitos
npm i @fortawesome/react-fontawesome  # Componente React para Font Awesome
```

---

## 📅 Dates & Time

### Date Libraries
Librerías para manipulación, formateo y cálculo de fechas.
```bash
npm i date-fns  # Librería moderna y modular para fechas
npm i dayjs  # Alternativa ligera a Moment.js (2KB)
npm i moment  # Librería clásica para fechas (pesada, no recomendada para nuevos proyectos)
npm i luxon  # Librería moderna por el creador de Moment.js
```

### Date Pickers
Componentes para selección de fechas y horarios.
```bash
npm i react-datepicker  # Date picker más popular y customizable
npm i react-day-picker  # Date picker ligero y flexible
npm i @mui/x-date-pickers  # Date pickers de Material-UI
npm i react-calendar  # Calendario completo y customizable
```

---

## 📊 Charts & Data Visualization

### Chart Libraries
Librerías para crear gráficos y visualizaciones de datos interactivas.
```bash
npm i recharts  # Librería de gráficos composable y declarativa
npm i chart.js react-chartjs-2  # Wrapper de Chart.js para React
npm i @nivo/core @nivo/bar @nivo/line  # Gráficos D3-based con gran customización
npm i plotly.js react-plotly.js  # Gráficos científicos y estadísticos avanzados
npm i react-circular-progressbar  # Barras de progreso circulares personalizables
npm i d3  # Librería de visualización de datos más potente (requiere más setup)
```

### React Circular Progressbar
Librería ligera y altamente personalizable para crear barras de progreso circulares animadas en aplicaciones React. Perfecta para dashboards, métricas de progreso y KPIs.

**✅ Cuándo usar**: Para mostrar métricas de progreso, estadísticas KPI, porcentajes de completitud, dashboards de usuario.
**❌ Cuándo NO usar**: Para grandes cantidades de datos, gráficos complejos de series temporales o cuando necesitas gráficos estadísticos avanzados.

```bash
npm i react-circular-progressbar
```

**📦 Enlace npm**:
- [react-circular-progressbar](https://www.npmjs.com/package/react-circular-progressbar)

**Ejemplo básico**:
```jsx
import { CircularProgressbar } from 'react-circular-progressbar';
import 'react-circular-progressbar/dist/styles.css';

function ProgressIndicator() {
  return (
    <div style={{ width: 200, height: 200 }}>
      <CircularProgressbar
        value={66}
        text={`${66}%`}
        styles={{
          path: {
            stroke: `#00bcd4`,
            strokeLinecap: 'round',
          },
          text: {
            fill: '#333',
            fontSize: '16px',
          },
        }}
      />
    </div>
  );
}
```

**Ejemplo con varios estilos**:
```jsx
import { CircularProgressbar, buildStyles } from 'react-circular-progressbar';

function AdvancedProgress({ value, maxValue }) {
  return (
    <CircularProgressbar
      value={value}
      maxValue={maxValue}
      text={`${value}/${maxValue}`}
      styles={buildStyles({
        rotation: 0.25,
        strokeLinecap: 'butt',
        textSize: '16px',
        pathTransitionDuration: 0.5,
        pathColor: value > 50 ? `rgba(62, 152, 199, ${value / 100})` : 'red',
        textColor: '#333',
        trailColor: '#d6d6d6',
        backgroundColor: '#3e98c7',
      })}
    />
  );
}
```

**Props principales**:
- `value`: Valor actual del progreso
- `maxValue`: Valor máximo para el cálculo del porcentaje (por defecto 100)
- `text`: Texto a mostrar dentro del círculo
- `strokeWidth`: Grosor del trazo del círculo
- `styles`: Objeto de estilos personalizados
- `className`: Clases CSS personalizadas

### Data Tables
Componentes para mostrar y manipular grandes cantidades de datos tabulares.
```bash
npm i @tanstack/react-table  # Tabla headless potente y flexible
npm i react-data-grid  # Tabla con performance optimizada para grandes datasets
npm i ag-grid-react ag-grid-community  # Tabla empresarial con funciones avanzadas
```

---

## 🧪 Testing

### Testing Frameworks
Herramientas para testing unitario, integración y componentes React.
```bash
npm i @testing-library/react  # Librería estándar para testing de componentes
npm i @testing-library/jest-dom  # Matchers adicionales para Jest
npm i @testing-library/user-event  # Simulación de eventos de usuario
npm i jest  # Framework de testing JavaScript
npm i vitest  # Alternativa moderna y rápida a Jest
```

### E2E Testing
Testing end-to-end para probar la aplicación completa como usuario final.
```bash
npm i @playwright/test  # Testing E2E moderno y cross-browser
npm i cypress  # Framework E2E popular con debugging visual
npm i puppeteer  # Control automatizado de Chrome para testing
```

---

## 🛠️ Development Tools

### Code Quality
Herramientas para mantener código consistente y libre de errores.
```bash
npm i eslint eslint-plugin-react  # Linter para JavaScript/React
npm i prettier  # Formateador de código automático
npm i husky  # Git hooks para ejecutar scripts en commits
npm i lint-staged  # Ejecuta linters solo en archivos staged
```

### Storybook
Herramienta para desarrollar componentes UI en aislamiento.
```bash
npx storybook@latest init  # Inicialización automática de Storybook
npm i @storybook/addon-essentials  # Addons esenciales para Storybook
```

### Type Checking
Herramientas para verificación de tipos y mejor experiencia de desarrollo.
```bash
npm i typescript  # Superset tipado de JavaScript
npm i @types/react @types/react-dom  # Definiciones de tipos para React
npm i prop-types  # Validación de props en tiempo de ejecución
```

---

## 📁 File Upload & Handling

### File Upload
Componentes y utilities para subida y manejo de archivos.
```bash
npm i react-dropzone  # Área drag & drop para archivos con preview
npm i react-image-crop  # Recorte de imágenes interactivo
npm i react-avatar-editor  # Editor de avatares con zoom y rotación
npm i filepond react-filepond  # Uploader elegante con progress y preview
```

### Image Handling
Componentes especializados en mostrar y manipular imágenes.
```bash
npm i react-image-gallery  # Galería de imágenes con thumbnails
npm i react-image-zoom  # Zoom de imágenes con lupa
npm i react-photo-view  # Visor de fotos tipo lightbox
```

---

## 🌍 Internationalization (i18n)

### i18n Libraries
Librerías para internacionalización y soporte multi-idioma.
```bash
npm i react-i18next i18next  # Librería i18n más completa para React
npm i react-intl  # Internacionalización por Facebook (ahora FormatJS)
npm i @formatjs/intl-polyfill  # Polyfills para APIs de internacionalización
```

---

## 🔐 Security

### Authentication
Servicios y librerías para autenticación y autorización.
```bash
npm i @auth0/auth0-react  # Integración con Auth0 para React
npm i firebase  # Backend-as-a-Service de Google con auth
npm i @supabase/supabase-js  # Alternativa open source a Firebase
npm i next-auth  # Autenticación para Next.js
```

### Security Utilities
Herramientas para encriptación y seguridad en el frontend.
```bash
npm i helmet  # Middleware de seguridad para Express (backend)
npm i crypto-js  # Librería de criptografía para JavaScript
npm i bcryptjs  # Hashing de passwords (mejor usarlo en backend)
```

---

## ⚡ Performance

### Performance Monitoring
Herramientas para monitorear y mejorar el rendimiento de la aplicación.
```bash
npm i @sentry/react  # Monitoreo de errores y performance
npm i web-vitals  # Métricas de experiencia de usuario de Google
# react-loadable está deprecated - usar React.lazy() y Suspense
```

### Code Splitting
Librerías para dividir el código y mejorar tiempos de carga.
```bash
npm i @loadable/component  # Code splitting avanzado con SSR
# react-loadable deprecated - usar React.lazy() con Suspense para code splitting
```

---

## 📱 Mobile & PWA

### Mobile Development
Frameworks para desarrollo móvil con React.
```bash
npm i react-native  # Framework para apps móviles nativas
npm i @ionic/react  # Framework híbrido para móviles
npm i capacitor  # Bridge para convertir web apps en móviles
```

### Mobile Touch & Gestures
Librerías para interacción táctil y gestos en interfaces móviles.
```bash
npm i react-swipeable  # Detección de gestos de swipe
npm i react-swipeable-list  # Listas deslizables con swipe gestures
```

**Librerías de gestos móviles**:
- [`react-swipeable`](https://www.npmjs.com/package/react-swipeable): Hook para detectar gestos de swipe (izquierda, derecha, arriba, abajo)
- [`react-swipeable-list`](https://www.npmjs.com/package/react-swipeable-list): Componentes de lista con soporte para swipe actions (eliminar, marcar, etc.)

**Ejemplos de uso**:
```jsx
// react-swipeable
import { useSwipeable } from 'react-swipeable';

const handlers = useSwipeable({
  onSwipedLeft: () => console.log('swiped left'),
  onSwipedRight: () => console.log('swiped right'),
});

// react-swipeable-list
import { SwipeableList, SwipeableListItem } from 'react-swipeable-list';

<SwipeableList>
  <SwipeableListItem swipeLeft={{ content: <div>Eliminar</div> }}>
    <div>Item deslizable</div>
  </SwipeableListItem>
</SwipeableList>
```

### PWA
Herramientas para crear Progressive Web Apps.
```bash
npm i workbox-webpack-plugin  # Service worker para PWA
npm i react-pwa-install-prompt  # Prompt personalizado para instalar PWA
```

---

## 🔄 Server-Side Rendering (SSR/SSG)

### Next.js
Framework full-stack de React con SSR, SSG y App Router moderno.
```bash
npm i next react react-dom  # Framework Next.js completo
npm i @next/font  # Optimización de fuentes
npm i @next/image  # Componente de imagen optimizada
npm i @vercel/analytics  # Analytics para aplicaciones Vercel
```

### Remix
Framework full-stack centrado en estándares web y performance.
```bash
npm i @remix-run/node @remix-run/react  # Core de Remix
npm i @remix-run/serve  # Servidor de desarrollo
npm i @remix-run/dev  # Herramientas de desarrollo
```

### Gatsby
Generador de sitios estáticos con GraphQL integrado.
```bash
npm i gatsby react react-dom  # Core de Gatsby
npm i gatsby-plugin-image gatsby-plugin-sharp  # Optimización de imágenes
npm i gatsby-source-filesystem  # Source plugin para archivos
npm i gatsby-transformer-remark  # Transformador de Markdown
```

### Astro
Framework multi-framework para sitios estáticos ultra-rápidos.
```bash
npm i astro  # Core de Astro
npm i @astrojs/react  # Integración con React
npm i @astrojs/tailwind  # Integración con Tailwind CSS
npm i @astrojs/sitemap  # Generación de sitemap
```

---

## 🎮 Game Development

### React Three Fiber
Renderer de Three.js para React con componentes declarativos.
```bash
npm i @react-three/fiber three  # Renderer React para Three.js
npm i @react-three/drei  # Helpers y abstracciones útiles
npm i @react-three/cannon  # Física con Cannon.js
npm i @react-three/rapier  # Física con Rapier (más moderna)
```

### Game Libraries
Librerías especializadas para desarrollo de juegos.
```bash
npm i phaser  # Framework de juegos 2D completo
npm i babylonjs @babylonjs/core  # Motor 3D potente
npm i matter-js  # Motor de física 2D
npm i howler  # Librería de audio para juegos
```

---

## 📱 Cross-Platform

### Desktop Applications
Frameworks para crear aplicaciones de escritorio con React.
```bash
npm i @tauri-apps/api @tauri-apps/cli  # Tauri - apps desktop con Rust
npm i electron  # Electron - apps desktop con Node.js
npm i @electron/forge  # Herramientas de desarrollo para Electron
npm i electron-builder  # Empaquetado de aplicaciones Electron
```

### Mobile Hybrid
Soluciones para aplicaciones móviles híbridas.
```bash
npm i @capacitor/core @capacitor/cli  # Capacitor - bridge nativo
npm i @capacitor/android @capacitor/ios  # Plataformas móviles
npm i @ionic/react @ionic/react-router  # Ionic con React
npm i react-native-web  # React Native para web
```

---

## 🤖 AI/ML Integration

### Machine Learning
Librerías para integrar IA y ML en aplicaciones React.
```bash
npm i @tensorflow/tfjs @tensorflow/tfjs-react-native  # TensorFlow.js
npm i @huggingface/transformers  # Transformers de Hugging Face
npm i ml5  # Librería ML amigable para creativos
npm i @mediapipe/tasks-vision  # MediaPipe para visión por computadora
```

### AI Services Integration
SDKs para servicios de IA populares.
```bash
npm i openai  # SDK oficial de OpenAI
npm i @anthropic-ai/sdk  # SDK de Anthropic (Claude)
npm i @google-ai/generativelanguage  # Google AI SDK
npm i replicate  # Plataforma para modelos de IA
```

---

## 🔗 Blockchain/Web3

### Ethereum Integration
Librerías para integración con blockchain Ethereum.
```bash
npm i wagmi viem  # Hooks React para Ethereum (reemplaza ethers)
npm i @rainbow-me/rainbowkit  # Wallet connection UI
npm i @web3modal/wagmi @web3modal/react  # Modal de conexión Web3
npm i @tanstack/react-query  # Requerido para wagmi
```

### Blockchain Utilities
Herramientas adicionales para desarrollo Web3.
```bash
npm i ethers  # Librería Ethereum (legacy, usar viem)
npm i web3  # Librería Web3 alternativa
npm i @solana/web3.js  # SDK para Solana
npm i @near-wallet-selector/core  # Selector de wallet NEAR
```

---

## 📊 Business Intelligence

### Advanced Charts
Librerías especializadas en visualización de datos empresariales.
```bash
npm i @observablehq/plot  # Gramática de gráficos moderna
npm i vega-lite vega  # Visualización declarativa potente
npm i apache-echarts echarts-for-react  # Gráficos empresariales
npm i @tremor/react  # Componentes de dashboard modernos
```

### Dashboard Components
Componentes especializados para dashboards y BI.
```bash
npm i @visx/visx  # Primitivos de visualización de Airbnb
npm i victory  # Componentes de gráficos modulares
npm i @nivo/core @nivo/calendar @nivo/heatmap  # Gráficos especializados
npm i react-grid-layout  # Layouts de dashboard arrastrables
```

---

## 🔧 Utilities

### General Utilities
Librerías de utilidades generales para programación funcional y helpers.
```bash
npm i lodash  # Librería de utilidades más completa
npm i ramda  # Programación funcional pura
npm i uuid  # Generación de identificadores únicos
npm i nanoid  # Generador de IDs más pequeño y seguro
```

### String & Text
Utilidades para manipulación de texto y renderizado de contenido.
```bash
npm i slugify  # Convertir texto a URL-friendly slugs
npm i string-similarity  # Comparar similitud entre strings
npm i react-markdown  # Renderizar Markdown en React
npm i @uiw/react-md-editor  # Editor de Markdown completo
```

### Development Utilities
Hooks y componentes útiles para desarrollo React.
```bash
npm i react-helmet  # Manejo del <head> del documento
npm i react-hot-toast  # Notificaciones toast elegantes
npm i react-toastify  # Sistema de notificaciones completo
npm i use-debounce  # Hook para debounce de valores
npm i react-use  # Colección de hooks útiles
```

### Local Storage & Cookies
Manejo de almacenamiento local y cookies en el navegador.
```bash
npm i js-cookie  # Manejo simple de cookies
npm i react-cookie  # Hooks para cookies en React
npm i use-local-storage-state  # Hook para localStorage con estado sincronizado
```

---

## 📚 Comandos de Instalación Rápida por Categoría

### Stack Completo Básico
Configuración mínima para una aplicación React moderna con routing, fetching de datos, formularios y UI.
```bash
npm i react react-dom  # Core de React
npm i react-router-dom  # Routing para SPA
npm i @tanstack/react-query axios  # Estado del servidor y HTTP client
npm i react-hook-form yup @hookform/resolvers  # Formularios y validación
npm i @headlessui/react @heroicons/react  # Componentes headless e iconos
npm i tailwindcss  # CSS utility-first
```

### Stack con Material-UI
Stack completo usando Material-UI como sistema de componentes principal.
```bash
npm i @mui/material @emotion/react @emotion/styled  # Componentes Material-UI
npm i @mui/icons-material  # Iconos de Material Design
npm i react-router-dom  # Routing
npm i @tanstack/react-query axios  # Gestión de datos del servidor
npm i react-hook-form yup  # Formularios y validación
```

### Stack con Ant Design
Stack empresarial usando Ant Design para aplicaciones de administración.
```bash
npm i antd @ant-design/icons  # Componentes y iconos Ant Design
npm i react-router-dom  # Routing
npm i @reduxjs/toolkit react-redux  # Gestión de estado global
npm i axios  # Cliente HTTP
npm i dayjs  # Manejo de fechas (compatible con Ant Design)
```

### Stack Next.js Full-Stack
Stack completo para aplicaciones full-stack con Next.js.
```bash
npm i next react react-dom  # Framework Next.js
npm i @next/font  # Optimización de fuentes
npm i next-auth  # Autenticación
npm i prisma @prisma/client  # ORM para base de datos
npm i @tanstack/react-query  # Estado del servidor
npm i react-hook-form zod @hookform/resolvers  # Formularios con validación TypeScript
```

### Stack Minimalista
Stack ultra-ligero para aplicaciones simples.
```bash
npm i react react-dom  # Core de React
npm i wouter  # Router minimalista (2KB)
npm i swr  # Fetching simple de datos
npm i react-hook-form  # Formularios ligeros
npm i clsx  # Utility para clases CSS
```

### Stack para Apps Móviles (React Native)
```bash
npm i react react-native  # React Native core
npm i @react-navigation/native  # Navegación para móviles
npm i @react-navigation/native-stack  # Stack navigator
npm i react-native-screens react-native-safe-area-context  # Dependencias de navegación
npm i @tanstack/react-query  # Estado del servidor
npm i react-hook-form  # Formularios
```

---

## 💡 Tips de Instalación

### Para proyectos con TypeScript
Agrega las definiciones de tipos necesarias para mejor experiencia de desarrollo:
```bash
npm i -D @types/react @types/react-dom  # Tipos para React
npm i -D @types/node  # Tipos para Node.js APIs
npm i -D typescript  # Compilador TypeScript
npm i -D @types/lodash  # Si usas Lodash
npm i -D @types/uuid  # Si usas UUID
```

### Para desarrollo y calidad de código
Herramientas esenciales para mantener código limpio y consistente:
```bash
npm i -D eslint prettier  # Linting y formateo
npm i -D @testing-library/react @testing-library/jest-dom  # Testing
npm i -D husky lint-staged  # Git hooks y formateo automático
npm i -D @typescript-eslint/eslint-plugin  # ESLint para TypeScript
```

### Bundle Analyzer
Herramientas para analizar el tamaño del bundle y optimizar performance:
```bash
npm i -D webpack-bundle-analyzer  # Analizador visual para Webpack
npm i -D @next/bundle-analyzer  # Analizador específico para Next.js
npm i -D rollup-plugin-analyzer  # Analizador para Rollup
npm i -D vite-bundle-analyzer  # Analizador para Vite
npm i -D source-map-explorer  # Explora el código fuente desde source maps
```