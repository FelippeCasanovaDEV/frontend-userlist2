<template>
    <div class="dialog">
        <div class="dialog_content">
            <div class="dialog_head">
                <h2>Add nova Tarefa</h2>
                    
                <button @click="onClickCancel">
                    <img src="../assets/icons/cancel.png" width="25">
                </button>
                
            </div>
            <div class="dialog_body">
                <label for="title">Título da Tarefa</label>
                <input type="text" id="title">
                <label for="description">Descrição</label>
                <input type="text" id="description">
                <label for="date">Data de Expiração</label>
                <input type="date" id="date">
                
                <div class="form_btn" >
                    <button class="btn">Enviar</button>
                </div>
            </div>
        </div>

    </div>
</template>
<script lang="ts" setup>
import { defineComponent } from 'vue'

const emit = defineEmits(['close']);

function onClickCancel(){
    emit("close", true);
}

</script>