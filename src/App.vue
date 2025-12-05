<!-- V-BIND -->
<!-- <script setup>
import { ref } from 'vue';

const image = ref('https://vuejs.org/images/logo.png');
const link = ref('https://vuejs.org');
</script>

<template>
  <div>
    <a :href="link">
      <img 
        :src="image" 
        alt=""
        width="100"
        >
      </a>
  </div>
</template> -->

<!-- V-FOR -->
<!-- <script setup>
import { ref } from 'vue';

const fruits = ref(['Manga', 'banana', 'morango']);
const users = ref([
  { id: 1, nome: 'Ana', idade: 20},
  { id: 2, nome: 'João', idade: 22},
  { id: 3, nome: 'Maria', idade: 19},
]);
</script>

<template>
  <div>
    <div>
      <ul>
        <li
          v-for="fruit in fruits"
          v-bind:key="fruit"
        >
          {{ fruit }}
        </li>
      </ul>
      <br>
      <table>
        <tr>
          <th>ID</th>
          <th>Nome</th>
          <th>Idade</th>
        </tr>

        <tr 
          v-for="user in users"
          v-bind:key="user.id"  
        >
          <td>{{ user.id }}</td>
          <td>{{ user.nome }}</td>
          <td>{{ user.idade }}</td>
        </tr>
      </table>
    </div>
  </div>
</template> -->

<!-- v-show
<script setup>
import { ref } from 'vue';

const showMore = ref(false);
</script>

<template>
  <div>
    <div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur tempore illo accusantium quis qui laborum dolorum quasi dolor? Saepe, placeat dolorem. Nobis tempore accusantium, laborum nemo ab itaque sunt amet?</p>

      <p v-show="showMore">Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa delectus explicabo repudiandae earum provident dolores accusamus corrupti nesciunt voluptatum numquam? Itaque aperiam quod delectus. Ea ratione similique labore eum laboriosam.</p>

      <a href="">Ver mais</a>
    </div>
  </div>

</template> -->

<!-- v-else
<script setup>
import { ref } from 'vue';
const score = ref(170);
</script>

<template>
  <div>
    <div v-if="score === 0">
      Comece a jogar!
    </div>

    <div v-else-if="score > 0 && score < 50">
      Você está indo no caminho! Continue Assim!
    </div>

    <div v-else-if="score >= 50 && score < 100">
      Ótimo progresso! Quase lá.
    </div>

    <div v-else>
      VOCÊ É UMA LENDA
    </div>
  </div>

</template> -->

<!-- v-if
<script setup>
import { ref } from 'vue';
const title = ref('Hello World 3');
const showTitle = ref(true);
</script>

<template>
  <div>
    <h1 v-if="showTitle">{{ title }}</h1>
  </div>
</template> -->
