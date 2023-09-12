<script setup>
</script>

<template>
    <main class="contenedor-principal">

        <header class="header-carrito">
            <h2>Tu carrito →</h2>
            <a href="">🛒</a>
        </header>

        <section class="seccion-titulo">
            <h2>Nuestros HotWheels</h2>
        </section>

        <section class="contenedor-hotwheels">

            <article class="hotwheel">
                <img src="../assets/img/hotwheel_01.png" alt="" class="hotwheel-imagen">
                    <div class="hotwheel-descripcion">
                        <h1>Dodge Charger</h1>
                        <p>$42.000</p>
                    </div>
                    <div class="hotwheel-funcionalidad">
                        <button>+</button>
                        <p>5</p>
                        <button>-</button>
                    </div>
            </article>

            <article class="hotwheel">
                <img src="../assets/img/hotwheel_01.png" alt="" class="hotwheel-imagen">
                    <div class="hotwheel-descripcion">
                        <h1>Dodge Charger</h1>
                        <p>$42.000</p>
                    </div>
                    <div class="hotwheel-funcionalidad">
                        <button>+</button>
                        <p>5</p>
                        <button>-</button>
                    </div>
            </article>

        </section>
    </main>
</template>


<style scoped>
.contenedor-principal {
    width: 100%;
    display: flex;
    flex-direction: column;
    border: 1px solid red;
}

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

.seccion-titulo {
    width: 100%;
    padding: 3rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border: 1px solid orange;
}

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
    background-color: var(--bg-hotwheels-blue);
}

.hotwheel-imagen {
    grid-area: hotwheel-imagen;
}

.hotwheel-descripcion {
    grid-area: hotwheel-descripcion;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.hotwheel-funcionalidad {
    grid-area: hotwheel-funcionalidad;
    display: flex;
    align-items: center;
    justify-content: center;
}


</style>