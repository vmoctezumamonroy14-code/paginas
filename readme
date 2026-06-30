<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Briefing de Requerimientos Web - Premium Consultoría</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            dark: '#0B0F19',
                            card: '#161F30',
                            gold: '#C5A880',
                            goldHover: '#B3946C',
                            textMuted: '#94A3B8'
                        }
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts (Inter & Playfair Display) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0B0F19;
        }
        .font-serif {
            font-family: 'Playfair Display', serif;
        }
        /* Custom scrollbar for premium feel */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0B0F19;
        }
        ::-webkit-scrollbar-thumb {
            background: #1F2937;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #C5A880;
        }
    </style>
</head>
<body class="text-slate-100 min-h-screen flex flex-col justify-between selection:bg-brand-gold selection:text-brand-dark relative">

    <!-- Toast Notifications Container -->
    <div id="toast-container" class="fixed bottom-5 right-5 z-50 flex flex-col gap-3 max-w-sm w-full px-4 sm:px-0"></div>

    <!-- Header -->
    <header class="border-b border-slate-800/80 bg-brand-dark/90 backdrop-blur sticky top-0 z-50 py-4 px-6">
        <div class="max-w-5xl mx-auto flex flex-col sm:flex-row justify-between items-center gap-4">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 rounded-lg bg-gradient-to-tr from-brand-gold to-yellow-600 flex items-center justify-center shadow-lg shadow-brand-gold/10">
                    <span class="font-serif text-brand-dark font-bold text-xl">S</span>
                </div>
                <div>
                    <h1 class="font-serif text-xl font-bold tracking-wide text-white">STRATANCE <span class="text-brand-gold">STYLE</span></h1>
                    <p class="text-[10px] tracking-widest text-brand-gold uppercase font-medium">Briefing & Estrategia Web</p>
                </div>
            </div>
            <div class="text-center sm:text-right">
                <span class="text-xs text-brand-textMuted bg-slate-900 px-3 py-1.5 rounded-full border border-slate-800/50">
                    Paso <span id="current-step-badge">1</span> de 5
                </span>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="flex-grow py-12 px-4 max-w-4xl w-full mx-auto">
        <!-- Progress Bar -->
        <div class="w-full bg-slate-800 h-1.5 rounded-full mb-10 overflow-hidden">
            <div id="progress-bar" class="bg-gradient-to-r from-brand-gold to-yellow-600 h-full transition-all duration-500 ease-out" style="width: 20%;"></div>
        </div>

        <!-- Form Container -->
        <div class="bg-brand-card/60 backdrop-blur-md rounded-2xl border border-slate-800/80 p-8 md:p-10 shadow-2xl relative overflow-hidden">
            <div class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-transparent via-brand-gold/40 to-transparent"></div>

            <form id="brief-form" onsubmit="event.preventDefault();">
                
                <!-- STEP 1: Datos de Contacto -->
                <div class="step-pane" id="step-1">
                    <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 mb-6 pb-4 border-b border-slate-800/60">
                        <div>
                            <h2 class="font-serif text-3xl font-semibold text-white">1. Información de la Empresa</h2>
                            <p class="text-brand-textMuted text-sm">Comencemos con los detalles esenciales para conocer a tu organización.</p>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2" for="client-name">Nombre del Cliente / Empresa</label>
                            <input type="text" id="client-name" class="w-full bg-slate-900/50 border border-slate-800 focus:border-brand-gold rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-1 focus:ring-brand-gold transition duration-200" placeholder="Ej. Stratance Global">
                        </div>
                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2" for="client-contact">Contacto Principal (Nombre y Puesto)</label>
                            <input type="text" id="client-contact" class="w-full bg-slate-900/50 border border-slate-800 focus:border-brand-gold rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-1 focus:ring-brand-gold transition duration-200" placeholder="Ej. Lic. Alejandro Ruiz - CEO">
                        </div>
                        <div class="md:col-span-2">
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2" for="client-email">Correo Electrónico de Contacto del Cliente</label>
                            <input type="email" id="client-email" class="w-full bg-slate-900/50 border border-slate-800 focus:border-brand-gold rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-1 focus:ring-brand-gold transition duration-200" placeholder="Ej. contacto@empresa.com">
                        </div>
                        <div class="md:col-span-2">
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2" for="business-desc">¿A qué se dedica la empresa brevemente?</label>
                            <textarea id="business-desc" rows="3" class="w-full bg-slate-900/50 border border-slate-800 focus:border-brand-gold rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-1 focus:ring-brand-gold transition duration-200" placeholder="Ej. Despacho contable y legal especializado en modelos corporativos y planeación patrimonial."></textarea>
                        </div>
                    </div>
                </div>

                <!-- STEP 2: Objetivos y Audiencia -->
                <div class="step-pane hidden" id="step-2">
                    <h2 class="font-serif text-3xl font-semibold mb-2 text-white">2. Objetivos & Audiencia</h2>
                    <p class="text-brand-textMuted text-sm mb-8">Define qué quieres lograr con este nuevo sitio web y a quién deseas atraer.</p>
                    
                    <div class="space-y-6">
                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2">¿Cuál es el propósito primordial del sitio?</label>
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 mt-2">
                                <label class="flex items-center gap-3 bg-slate-900/30 hover:bg-slate-900/60 border border-slate-800 p-4 rounded-xl cursor-pointer transition">
                                    <input type="radio" name="web-purpose" value="Generación de Leads" class="accent-brand-gold w-4 h-4">
                                    <div>
                                        <p class="text-sm font-medium">Captar Leads / Prospectos</p>
                                        <p class="text-xs text-brand-textMuted">Conseguir datos para ventas</p>
                                    </div>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 hover:bg-slate-900/60 border border-slate-800 p-4 rounded-xl cursor-pointer transition">
                                    <input type="radio" name="web-purpose" value="Credibilidad de Marca" class="accent-brand-gold w-4 h-4" checked>
                                    <div>
                                        <p class="text-sm font-medium">Prestigio e Identidad</p>
                                        <p class="text-xs text-brand-textMuted">Mostrar solidez institucional</p>
                                    </div>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 hover:bg-slate-900/60 border border-slate-800 p-4 rounded-xl cursor-pointer transition">
                                    <input type="radio" name="web-purpose" value="Venta Directa de Servicios" class="accent-brand-gold w-4 h-4">
                                    <div>
                                        <p class="text-sm font-medium">Venta de Servicios</p>
                                        <p class="text-xs text-brand-textMuted">Explicar y cotizar servicios online</p>
                                    </div>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 hover:bg-slate-900/60 border border-slate-800 p-4 rounded-xl cursor-pointer transition">
                                    <input type="radio" name="web-purpose" value="Informativo / Contenidos" class="accent-brand-gold w-4 h-4">
                                    <div>
                                        <p class="text-sm font-medium">Portal Informativo</p>
                                        <p class="text-xs text-brand-textMuted">Blog, noticias o biblioteca legal</p>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2" for="target-audience">¿Quién es el cliente ideal para esta web?</label>
                            <input type="text" id="target-audience" class="w-full bg-slate-900/50 border border-slate-800 focus:border-brand-gold rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-1 focus:ring-brand-gold transition duration-200" placeholder="Ej. Directores de Finanzas, Dueños de Empresas Medianas, Abogados Patrimoniales">
                        </div>

                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2" for="user-action">¿Cuál es la acción clave que el usuario debe realizar?</label>
                            <input type="text" id="user-action" class="w-full bg-slate-900/50 border border-slate-800 focus:border-brand-gold rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-1 focus:ring-brand-gold transition duration-200" placeholder="Ej. Agendar una asesoría diagnóstica en Calendly o llenar el formulario de contacto">
                        </div>
                    </div>
                </div>

                <!-- STEP 3: Identidad Visual e Inspiración -->
                <div class="step-pane hidden" id="step-3">
                    <h2 class="font-serif text-3xl font-semibold mb-2 text-white">3. Identidad Visual & Look</h2>
                    <p class="text-brand-textMuted text-sm mb-8">El diseño entra por los ojos. Definamos la estética que se adecúe al sector.</p>
                    
                    <div class="space-y-6">
                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2">¿Cómo describirías la personalidad del diseño?</label>
                            <div class="grid grid-cols-2 sm:grid-cols-3 gap-3">
                                <label class="flex items-center justify-between bg-slate-900/30 hover:bg-slate-900/60 border border-slate-800 p-3 rounded-lg cursor-pointer transition">
                                    <span class="text-xs font-medium">Corporativo & Serio</span>
                                    <input type="checkbox" name="style-keywords" value="Corporativo/Serio" class="accent-brand-gold w-4 h-4" checked>
                                </label>
                                <label class="flex items-center justify-between bg-slate-900/30 hover:bg-slate-900/60 border border-slate-800 p-3 rounded-lg cursor-pointer transition">
                                    <span class="text-xs font-medium">Premium & Exclusivo</span>
                                    <input type="checkbox" name="style-keywords" value="Premium/Exclusivo" class="accent-brand-gold w-4 h-4" checked>
                                </label>
                                <label class="flex items-center justify-between bg-slate-900/30 hover:bg-slate-900/60 border border-slate-800 p-3 rounded-lg cursor-pointer transition">
                                    <span class="text-xs font-medium">Tecnológico & Moderno</span>
                                    <input type="checkbox" name="style-keywords" value="Tecnológico/Moderno" class="accent-brand-gold w-4 h-4">
                                </label>
                                <label class="flex items-center justify-between bg-slate-900/30 hover:bg-slate-900/60 border border-slate-800 p-3 rounded-lg cursor-pointer transition">
                                    <span class="text-xs font-medium">Minimalista & Limpio</span>
                                    <input type="checkbox" name="style-keywords" value="Minimalista/Limpio" class="accent-brand-gold w-4 h-4">
                                </label>
                                <label class="flex items-center justify-between bg-slate-900/30 hover:bg-slate-900/60 border border-slate-800 p-3 rounded-lg cursor-pointer transition">
                                    <span class="text-xs font-medium">Disruptivo / Atrevido</span>
                                    <input type="checkbox" name="style-keywords" value="Disruptivo" class="accent-brand-gold w-4 h-4">
                                </label>
                                <label class="flex items-center justify-between bg-slate-900/30 hover:bg-slate-900/60 border border-slate-800 p-3 rounded-lg cursor-pointer transition">
                                    <span class="text-xs font-medium">Cercano / Cálido</span>
                                    <input type="checkbox" name="style-keywords" value="Cálido/Humano" class="accent-brand-gold w-4 h-4">
                                </label>
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2" for="brand-colors">Paleta de Colores deseada (o si ya tienen una oficial)</label>
                            <input type="text" id="brand-colors" class="w-full bg-slate-900/50 border border-slate-800 focus:border-brand-gold rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-1 focus:ring-brand-gold transition duration-200" placeholder="Ej. Azul marino profundo, acentos dorados y fondo negro (como Stratance)">
                        </div>

                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2" for="competitor-sites">Páginas de Competencia o Inspiración (URLs separadas por comas)</label>
                            <textarea id="competitor-sites" rows="2" class="w-full bg-slate-900/50 border border-slate-800 focus:border-brand-gold rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-1 focus:ring-brand-gold transition duration-200" placeholder="Ej. https://stratanceglobal.com, https://otrawebconsultoria.com"></textarea>
                        </div>
                    </div>
                </div>

                <!-- STEP 4: Estructura y Características -->
                <div class="step-pane hidden" id="step-4">
                    <h2 class="font-serif text-3xl font-semibold mb-2 text-white">4. Estructura & Funcionalidad</h2>
                    <p class="text-brand-textMuted text-sm mb-8">¿Cómo se organizarán las páginas y qué tecnologías o integraciones usará el sitio?</p>
                    
                    <div class="space-y-6">
                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2">Secciones indispensables para el menú</label>
                            <div class="grid grid-cols-2 gap-3">
                                <label class="flex items-center gap-3 bg-slate-900/30 p-3 rounded-lg border border-slate-800">
                                    <input type="checkbox" name="sections" value="Home" class="accent-brand-gold w-4 h-4" checked disabled>
                                    <span class="text-xs text-white">Inicio (Home Page)</span>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 p-3 rounded-lg border border-slate-800 cursor-pointer">
                                    <input type="checkbox" name="sections" value="Nosotros" class="accent-brand-gold w-4 h-4" checked>
                                    <span class="text-xs text-white">Nosotros / Firma</span>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 p-3 rounded-lg border border-slate-800 cursor-pointer">
                                    <input type="checkbox" name="sections" value="Servicios" class="accent-brand-gold w-4 h-4" checked>
                                    <span class="text-xs text-white">Catálogo de Servicios</span>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 p-3 rounded-lg border border-slate-800 cursor-pointer">
                                    <input type="checkbox" name="sections" value="Blog" class="accent-brand-gold w-4 h-4">
                                    <span class="text-xs text-white">Blog / Artículos Técnicos</span>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 p-3 rounded-lg border border-slate-800 cursor-pointer">
                                    <input type="checkbox" name="sections" value="Contacto" class="accent-brand-gold w-4 h-4" checked>
                                    <span class="text-xs text-white">Página de Contacto dedicada</span>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 p-3 rounded-lg border border-slate-800 cursor-pointer">
                                    <input type="checkbox" name="sections" value="CasosExito" class="accent-brand-gold w-4 h-4">
                                    <span class="text-xs text-white">Casos de Éxito / Alianzas</span>
                                </label>
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2">Requerimientos Técnicos Especiales</label>
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
                                <label class="flex items-center gap-3 bg-slate-900/30 p-3 rounded-lg border border-slate-800 cursor-pointer">
                                    <input type="checkbox" id="req-multilingual" class="accent-brand-gold w-4 h-4">
                                    <div>
                                        <p class="text-xs font-semibold">Multilingüe (Español / Inglés)</p>
                                    </div>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 p-3 rounded-lg border border-slate-800 cursor-pointer">
                                    <input type="checkbox" id="req-whatsapp" class="accent-brand-gold w-4 h-4" checked>
                                    <div>
                                        <p class="text-xs font-semibold">Chat flotante de WhatsApp directo</p>
                                    </div>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 p-3 rounded-lg border border-slate-800 cursor-pointer">
                                    <input type="checkbox" id="req-calendar" class="accent-brand-gold w-4 h-4">
                                    <div>
                                        <p class="text-xs font-semibold">Integración de Agenda (Calendly/Hubspot)</p>
                                    </div>
                                </label>
                                <label class="flex items-center gap-3 bg-slate-900/30 p-3 rounded-lg border border-slate-800 cursor-pointer">
                                    <input type="checkbox" id="req-seo" class="accent-brand-gold w-4 h-4" checked>
                                    <div>
                                        <p class="text-xs font-semibold">Optimización SEO Inicial</p>
                                    </div>
                                </label>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- STEP 5: Plazos e Infraestructura -->
                <div class="step-pane hidden" id="step-5">
                    <h2 class="font-serif text-3xl font-semibold mb-2 text-white">5. Infraestructura y Tiempos</h2>
                    <p class="text-brand-textMuted text-sm mb-8">Último paso. Planifiquemos la puesta en marcha técnica y logística.</p>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2">¿Ya cuentan con Dominio y Hosting?</label>
                            <div class="space-y-2 mt-2">
                                <label class="flex items-center gap-2 text-sm text-white cursor-pointer">
                                    <input type="radio" name="domain-hosting" value="Ya cuento con ambos" class="accent-brand-gold">
                                    <span>Sí, ya los tenemos contratados</span>
                                </label>
                                <label class="flex items-center gap-2 text-sm text-white cursor-pointer">
                                    <input type="radio" name="domain-hosting" value="Dominio contratado sin Hosting" class="accent-brand-gold">
                                    <span>Solo dominio, falta Hosting</span>
                                </label>
                                <label class="flex items-center gap-2 text-sm text-white cursor-pointer">
                                    <input type="radio" name="domain-hosting" value="No cuento con ninguno, requiere asesoria" class="accent-brand-gold" checked>
                                    <span>No, requerimos recomendación y compra</span>
                                </label>
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2" for="deadline">Fecha estimada de Lanzamiento deseada</label>
                            <input type="date" id="deadline" class="w-full bg-slate-900/50 border border-slate-800 focus:border-brand-gold rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-1 focus:ring-brand-gold transition duration-200">
                        </div>

                        <div class="md:col-span-2">
                            <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2" for="extra-notes">Comentarios o requerimientos adicionales de importancia</label>
                            <textarea id="extra-notes" rows="3" class="w-full bg-slate-900/50 border border-slate-800 focus:border-brand-gold rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-1 focus:ring-brand-gold transition duration-200" placeholder="Ej. Necesitamos conectar un sistema de descargas de facturación interna o un portal de clientes en el futuro..."></textarea>
                        </div>
                    </div>
                </div>

                <!-- RESULTS SCREEN -->
                <div class="step-pane hidden" id="results-screen">
                    <div class="text-center mb-6">
                        <div class="w-16 h-16 bg-brand-gold/10 text-brand-gold rounded-full flex items-center justify-center mx-auto mb-3 border border-brand-gold/30">
                            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                        </div>
                        <h2 class="font-serif text-3xl font-semibold text-white">¡Brief Generado Exitosamente!</h2>
                        <p class="text-brand-textMuted text-sm">Tu documento estructurado está listo. Puedes guardarlo, descargarlo o recibirlo en tu correo.</p>
                    </div>

                    <!-- Configuración de Destino del Correo -->
                    <div class="bg-slate-900/60 border border-slate-800 rounded-xl p-5 mb-6">
                        <h3 class="text-xs uppercase tracking-widest font-semibold text-brand-gold mb-3 flex items-center gap-2">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
                            Enviar a tu Correo Electrónico Personal
                        </h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-[10px] text-slate-400 uppercase tracking-wider mb-1" for="personal-email">Tu Email Personal</label>
                                <input type="email" id="personal-email" class="w-full bg-slate-950/80 border border-slate-800 focus:border-brand-gold rounded-lg px-3 py-2 text-xs text-white focus:outline-none transition duration-200" placeholder="tu-correo@ejemplo.com">
                            </div>
                            <div>
                                <label class="block text-[10px] text-slate-400 uppercase tracking-wider mb-1" for="web3forms-key">
                                    Clave Web3Forms (Opcional) 
                                    <a href="https://web3forms.com/" target="_blank" class="text-brand-gold hover:underline font-semibold ml-1">¿Qué es esto?</a>
                                </label>
                                <input type="text" id="web3forms-key" class="w-full bg-slate-950/80 border border-slate-800 focus:border-brand-gold rounded-lg px-3 py-2 text-xs text-white focus:outline-none transition duration-200" placeholder="Ej. aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee">
                            </div>
                        </div>
                        <div class="mt-4 flex flex-col sm:flex-row gap-3 items-center justify-between">
                            <p class="text-[11px] text-brand-textMuted leading-relaxed max-w-md">
                                <span class="text-brand-gold font-medium">Nota:</span> Si no tienes una clave Web3Forms, puedes conseguir una gratis en 5 segundos o, alternativamente, usaremos tu gestor de correos local para el envío automático.
                            </p>
                            <button type="button" id="send-email-btn" onclick="sendViaEmail()" class="w-full sm:w-auto bg-brand-gold hover:bg-brand-goldHover text-brand-dark text-xs font-bold py-2.5 px-5 rounded-lg transition duration-200 flex items-center justify-center gap-2 shadow-md">
                                <span id="email-btn-text">Enviar a mi Correo</span>
                                <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8"></path></svg>
                            </button>
                        </div>
                    </div>

                    <div class="mb-6">
                        <label class="block text-xs uppercase tracking-wider font-semibold text-brand-gold mb-2">Vista previa del Reporte (Markdown)</label>
                        <textarea id="brief-output" readonly class="w-full h-60 bg-slate-900 border border-slate-800 rounded-lg p-4 text-xs font-mono text-slate-300 focus:outline-none focus:ring-1 focus:ring-brand-gold overflow-y-auto"></textarea>
                    </div>

                    <div class="flex flex-col sm:flex-row gap-3 justify-center">
                        <button type="button" onclick="copyToClipboard()" class="bg-slate-800 hover:bg-slate-700 text-white font-medium px-6 py-3 rounded-lg transition duration-200 flex items-center justify-center gap-2 border border-slate-700">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 5H6a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2v-1M8 5a2 2 0 002 2h2a2 2 0 002-2M8 5a2 2 0 012-2h2a2 2 0 012 2m0 0h2a2 2 0 012 2v3m2 4H10m0 0l3-3m-3 3l3 3"></path></svg>
                            Copiar al Portapapeles
                        </button>
                        <button type="button" onclick="downloadMarkdown()" class="bg-gradient-to-r from-brand-gold to-yellow-600 hover:from-brand-goldHover hover:to-brand-gold text-brand-dark font-semibold px-6 py-3 rounded-lg transition duration-200 flex items-center justify-center gap-2 shadow-lg shadow-brand-gold/10">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"></path></svg>
                            Descargar Archivo .md
                        </button>
                    </div>
                </div>

                <!-- Navigation Controls (Hidden in results screen) -->
                <div id="navigation-controls" class="mt-10 pt-6 border-t border-slate-800/80 flex justify-between items-center">
                    <button type="button" id="prev-btn" onclick="navigateStep(-1)" class="text-brand-textMuted hover:text-white font-medium text-sm transition flex items-center gap-2 opacity-50 cursor-not-allowed" disabled>
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path></svg>
                        Anterior
                    </button>
                    
                    <button type="button" id="next-btn" onclick="navigateStep(1)" class="bg-gradient-to-r from-brand-gold to-yellow-600 hover:from-brand-goldHover hover:to-brand-gold text-brand-dark font-semibold px-6 py-3 rounded-lg transition duration-200 flex items-center gap-2 shadow-lg shadow-brand-gold/10">
                        <span>Siguiente</span>
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
                    </button>
                </div>
            </form>
        </div>
    </main>

    <!-- Footer -->
    <footer class="border-t border-slate-900 bg-brand-dark/50 py-4 text-center">
        <p class="text-xs text-brand-textMuted">&copy; 2026 Stratance Inspired Design Agency. Todos los derechos reservados.</p>
    </footer>

    <!-- Form Logic -->
    <script>
        let currentStep = 1;
        const totalSteps = 5;

        // Initialize configuration and fields from localStorage on startup
        document.addEventListener('DOMContentLoaded', () => {
            if (localStorage.getItem('user_personal_email')) {
                document.getElementById('personal-email').value = localStorage.getItem('user_personal_email');
            }
            if (localStorage.getItem('web3forms_key')) {
                document.getElementById('web3forms-key').value = localStorage.getItem('web3forms_key');
            }
        });

        // Elegant Toast Notification System replacing alerts
        function triggerToast(title, message, type = 'success') {
            const container = document.getElementById('toast-container');
            const toast = document.createElement('div');
            
            const bgClass = 'bg-brand-card border border-slate-800';
            const iconColor = type === 'success' ? 'text-brand-gold' : 'text-red-500';
            const iconSvg = type === 'success' 
                ? `<svg class="w-5 h-5 ${iconColor}" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>`
                : `<svg class="w-5 h-5 ${iconColor}" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path></svg>`;

            toast.className = `flex gap-3 p-4 rounded-xl shadow-2xl transition-all duration-300 transform translate-y-2 opacity-0 ${bgClass}`;
            toast.innerHTML = `
                <div class="flex-shrink-0">${iconSvg}</div>
                <div class="flex-grow">
                    <p class="text-xs font-bold text-white tracking-wide">${title}</p>
                    <p class="text-[11px] text-brand-textMuted mt-0.5">${message}</p>
                </div>
            `;
            
            container.appendChild(toast);
            
            // Animate In
            setTimeout(() => {
                toast.classList.remove('translate-y-2', 'opacity-0');
            }, 50);

            // Animate Out & Remove
            setTimeout(() => {
                toast.classList.add('opacity-0', 'scale-95');
                setTimeout(() => {
                    toast.remove();
                }, 300);
            }, 4500);
        }

        function updateUI() {
            // Update step visibility
            document.querySelectorAll('.step-pane').forEach((pane, idx) => {
                if (idx + 1 === currentStep) {
                    pane.classList.remove('hidden');
                } else {
                    pane.classList.add('hidden');
                }
            });

            // Update Header progress
            document.getElementById('current-step-badge').innerText = currentStep <= totalSteps ? currentStep : totalSteps;

            // Update Progress Bar
            const progressPercent = (currentStep / totalSteps) * 100;
            document.getElementById('progress-bar').style.width = `${Math.min(progressPercent, 100)}%`;

            // Navigation Button updates
            const prevBtn = document.getElementById('prev-btn');
            const nextBtn = document.getElementById('next-btn');

            if (currentStep === 1) {
                prevBtn.disabled = true;
                prevBtn.classList.add('opacity-50', 'cursor-not-allowed');
            } else {
                prevBtn.disabled = false;
                prevBtn.classList.remove('opacity-50', 'cursor-not-allowed');
            }

            if (currentStep === totalSteps) {
                nextBtn.innerHTML = `<span>Generar Brief</span> <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>`;
            } else {
                nextBtn.innerHTML = `<span>Siguiente</span> <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>`;
            }

            if (currentStep > totalSteps) {
                document.getElementById('navigation-controls').classList.add('hidden');
                generateMarkdownOutput();
            } else {
                document.getElementById('navigation-controls').classList.remove('hidden');
            }
        }

        function navigateStep(direction) {
            currentStep += direction;
            updateUI();
        }

        function getSelectedCheckboxes(name) {
            const checked = [];
            document.querySelectorAll(`input[name="${name}"]:checked`).forEach((cb) => {
                checked.push(cb.value);
            });
            return checked.join(', ');
        }

        function generateMarkdownOutput() {
            // Fetch inputs
            const clientName = document.getElementById('client-name').value || 'Sin definir';
            const contactName = document.getElementById('client-contact').value || 'Sin definir';
            const clientEmail = document.getElementById('client-email').value || 'Sin definir';
            const businessDesc = document.getElementById('business-desc').value || 'Sin definir';

            const webPurpose = document.querySelector('input[name="web-purpose"]:checked')?.value || 'Sin definir';
            const targetAudience = document.getElementById('target-audience').value || 'Sin definir';
            const userAction = document.getElementById('user-action').value || 'Sin definir';

            const styleKeywords = getSelectedCheckboxes('style-keywords') || 'Sin definir';
            const brandColors = document.getElementById('brand-colors').value || 'Sin definir';
            const competitors = document.getElementById('competitor-sites').value || 'Sin definir';

            const sections = getSelectedCheckboxes('sections') || 'Inicio';
            const multilingual = document.getElementById('req-multilingual').checked ? 'Sí (Inglés/Español)' : 'No (Solo Español)';
            const whatsapp = document.getElementById('req-whatsapp').checked ? 'Sí' : 'No';
            const calendar = document.getElementById('req-calendar').checked ? 'Sí' : 'No';
            const seo = document.getElementById('req-seo').checked ? 'Sí' : 'No';

            const infrastructure = document.querySelector('input[name="domain-hosting"]:checked')?.value || 'Sin definir';
            const deadline = document.getElementById('deadline').value || 'Sin definir';
            const extraNotes = document.getElementById('extra-notes').value || 'Ninguno';

            // Construct Markdown template
            const markdownText = `# 📄 BRIEF DE REQUERIMIENTOS WEB - PREMIUM STYLE

---



            document.getElementById('brief-output').value = markdownText;
            document.getElementById('results-screen').classList.remove('hidden');
        }

        // Email transmission service (Web3Forms API + fallback)
        async function sendViaEmail() {
            const emailTarget = document.getElementById('personal-email').value;
            const w3fKey = document.getElementById('web3forms-key').value;
            const briefContent = document.getElementById('brief-output').value;
            const clientName = document.getElementById('client-name').value || 'Cliente';

            if (!emailTarget) {
                triggerToast('Campo Requerido', 'Por favor, ingresa tu dirección de correo electrónico.', 'error');
                return;
            }

            // Save variables locally so they are persistent
            localStorage.setItem('user_personal_email', emailTarget);
            localStorage.setItem('web3forms_key', w3fKey);

            const sendBtn = document.getElementById('send-email-btn');
            const btnText = document.getElementById('email-btn-text');

            // 1. Direct Web3Forms automatic email delivery (Preferred method)
            if (w3fKey) {
                sendBtn.disabled = true;
                btnText.innerText = "Enviando...";

                try {
                    const response = await fetch("https://api.web3forms.com/submit", {
                        method: "POST",
                        headers: {
                            "Content-Type": "application/json",
                            Accept: "application/json"
                        },
                        body: JSON.stringify({
                            access_key: w3fKey,
                            subject: `Nuevo Briefing de Requerimientos - ${clientName}`,
                            from_name: "Web Briefing Engine",
                            to_email: emailTarget,
                            message: briefContent
                        })
                    });

                    const result = await response.json();

                    if (result.success) {
                        triggerToast('¡Correo Enviado!', `El brief de ${clientName} ha sido enviado exitosamente a ${emailTarget}.`, 'success');
                    } else {
                        triggerToast('Error en Envío', 'Hubo un error al procesar el envío. Revisa tu clave Web3Forms.', 'error');
                    }
                } catch (error) {
                    triggerToast('Error de Red', 'No se pudo conectar con el servidor de correos.', 'error');
                } finally {
                    sendBtn.disabled = false;
                    btnText.innerText = "Enviar a mi Correo";
                }
            } 
            // 2. Direct Mail Client Fallback (If no key is configured)
            else {
                triggerToast('Redireccionando', 'Se abrirá tu gestor de correos local para enviar el documento.', 'success');
                
                const subject = encodeURIComponent(`Briefing de Requerimientos Web - ${clientName}`);
                const body = encodeURIComponent(briefContent);
                const mailtoUrl = `mailto:${emailTarget}?subject=${subject}&body=${body}`;
                
                window.location.href = mailtoUrl;
            }
        }

        function copyToClipboard() {
            const textEl = document.getElementById('brief-output');
            textEl.select();
            textEl.setSelectionRange(0, 99999); // Mobile compatibility
            navigator.clipboard.writeText(textEl.value);
            
            triggerToast('¡Copiado!', 'El documento Markdown se copió correctamente al portapapeles.', 'success');
        }

        function downloadMarkdown() {
            const text = document.getElementById('brief-output').value;
            const clientName = document.getElementById('client-name').value || 'cliente';
            const filename = `brief_web_${clientName.toLowerCase().replace(/\s+/g, '_')}.md`;
            
            const element = document.createElement('a');
            element.setAttribute('href', 'data:text/plain;charset=utf-8,' + encodeURIComponent(text));
            element.setAttribute('download', filename);

            element.style.display = 'none';
            document.body.appendChild(element);
            element.click();
            document.body.removeChild(element);
            
            triggerToast('Descarga Iniciada', `El archivo ${filename} se está guardando localmente.`, 'success');
        }
    </script>
</body>
</html>
