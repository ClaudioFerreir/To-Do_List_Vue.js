<template>
  <ul class="list-group mt-4">
    <li class="list-group-item" v-for="tarefa in getTarefasFiltradas()">
      <input :checked="tarefa.finalizada" @change="evento => tarefa.finalizada = evento.target.checked"
        :id="tarefa.titulo" type="checkbox">
      <label class="ms-3" :class="{ done: tarefa.finalizada }" :for="tarefa.titulo">
        {{ tarefa.titulo }}
      </label>
    </li>
  </ul>
</template>