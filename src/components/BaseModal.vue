
<template>
    <div class="h-screen w-screen absolute top-0 bg-opacity-75 bg-black flex justify-center items-center z-10">
        <div class="relative h-16 w-96 bg-green-500 flex  justify-center items-center" id="modal-content">
            <slot></slot>
        </div>
    </div>
</template>
