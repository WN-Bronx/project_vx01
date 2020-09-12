<template>
    <div class="tile flex-centered">
        <div class="tile-icon">
            <i class="icon icon-people"></i>
        </div>
        <div class="title-content">
            <div class="title-subtitle">
                {{ info.description }}
            </div> 
        </div>
        <div class="title-action"> <!-- Para executar minha ação -->
            <button class="btn btn-link">OK</button>
            <button class="btn btn-link">
                <span class="text-error">Remover</span>
            </button>
        </div>    
    </div> 
</template>

<script>
export default {
    props: {
        info: {type: Object, required: true}
    }
}
</script>