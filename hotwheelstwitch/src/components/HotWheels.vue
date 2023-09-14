<script setup>
    const props = defineProps({
        hotwheel: {
            type: Object,
            required: true
        }
    })
</script>

<template>
    <main class="contenedor-principal">

        <!-- <header class="header-carrito">
            <h2 class="header-title">Tu carrito →</h2>
            <a class="header-emoji" href="">🛒</a>
        </header> -->

        <!-- <section class="seccion-titulo">
            <h2 class="seccion-title">Nuestros HotWheels</h2>
        </section> -->

        <section class="contenedor-hotwheels">

            <article class="hotwheel">
                <img 
                :src="'/img/' + hotwheel.imagen + '.png'"
                :alt="'Imagen HotWheel ' + hotwheel.nombre"
                class="hotwheel-imagen">
                    <div class="hotwheel-descripcion">
                        <h1 class="hotwheel-title">{{ hotwheel.nombre }}</h1>
                        <p class="hotwheel-price">{{hotwheel.precio }}</p>
                    </div>
                    <div class="hotwheel-funcionalidad">
                        <button class="hotwheel-btn">-</button>
                        <p class="hotwheel-cantidad">5</p>
                        <button class="hotwheel-btn">+</button>
                    </div>
            </article>

        </section>
    </main>
</template>


<style scoped>

/* Contenedor principal */
.contenedor-principal {
    width: 100%;
    display: flex;
    flex-direction: column;
    border: 1px solid red;
}
/* Header */
.header-carrito {
    width: 100%;
    padding: 2rem;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    border: 1px solid green;
    background: var(--bg-hotwheels-blue);
    position: sticky;
    top: 0;
}
.header-title {
    font-size: 3rem;
}
.header-emoji {
    font-size: 3rem;
}

/* Titulo */
.seccion-titulo {
    width: 100%;
    padding: 3rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border: 1px solid orange;
}

.seccion-title {
    font-size: 2rem;
}
/* HotWheels */
.contenedor-hotwheels {
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 1px solid blue;
    padding: 40px;
    gap: 40px;
}
.hotwheel {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr auto;
    gap: 0px 0px;
    grid-template-areas:
        "hotwheel-imagen hotwheel-imagen"
        "hotwheel-descripcion hotwheel-funcionalidad";
    box-shadow: rgba(9, 30, 66, 0.25) 0px 4px 8px -2px, rgba(9, 30, 66, 0.08) 0px 0px 0px 1px;
    border-radius: 1.4rem;
}
.hotwheel-imagen {
    grid-area: hotwheel-imagen;
    /* filter: drop-shadow(0 0 0.75rem rgb(220, 183, 20)); Usar para el hover */
    border-top-left-radius: 1.4rem;
    border-top-right-radius: 1.4rem;
}
.hotwheel-descripcion {
    grid-area: hotwheel-descripcion;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 12px 0;
}
.hotwheel-title {
    font-size: 1.5rem;
    color: var(--bg-hotwheels-blue);
}
.hotwheel-price {
    font-size: 1.2rem;
    color: var(--fnt-color-titles-red);
    font-weight: 700;
}
.hotwheel-funcionalidad {
    grid-area: hotwheel-funcionalidad;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
}

.hotwheel-btn {
    font-size: 1.5rem;
}

.hotwheel-cantidad {
    font-size: 1.5rem;
}
</style>