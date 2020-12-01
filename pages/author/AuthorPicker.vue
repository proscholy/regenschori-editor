<template>
  <v-card class="mb-4 px-4">
    <v-card-title class="p-0">
      <h3>Autoři<span v-if="is_arrangement_layout"> aranže</span>
        <span v-if="!is_original"> překladu</span>
      </h3>
    </v-card-title>

    <v-card-text class="p-0">
      <v-layout row wrap v-for="(author_pivot, i) in model.authors_pivot || []" :key="i">
        <v-flex xs12 sm8>
          <items-combo-box
            v-model="author_pivot.author"
            v-bind:p-items="authors"
            item-text="name"
            label="Jméno autora"
            :multiple="false"
            :enable-custom="true"
            :disabled="model.has_anonymous_author"
          ></items-combo-box>
        </v-flex>
        <v-flex xs10 sm3>
          <!-- <v-text-field label="Číslo písně" required v-model="record.number"></v-text-field> -->
          <v-select v-if="!is_arrangement_layout" :items="enums.authorship_type" v-model="author_pivot.authorship_type" label="Typ autora" :disabled="model.has_anonymous_author"></v-select>
          <v-select v-else :items="[{text: 'Aranžér', value:'GENERIC'}]" v-model="author_pivot.authorship_type" label="Typ autora" :disabled="model.has_anonymous_author"></v-select>
        </v-flex>
        <v-flex xs2 sm1>
          <!-- <v-text-field label="Číslo písně" required v-model="record.number"></v-text-field> -->
          <v-btn icon @click="removeAuthor(i)" :disabled="model.has_anonymous_author" class="text-secondary"><i class="fas fa-trash"></i></v-btn>
        </v-flex>
      </v-layout>
    </v-card-text>

    <v-card-text class="p-0" v-if="model.authors_pivot.filter((el) => el.author != null).length === 0">
                    <span v-if="!model.has_anonymous_author">
                      Zatím k písni nikdo nepřiřadil autora (u písně je označení „autor<span v-if="!is_original"> překladu </span> neznámý“).
                    </span>
      <span v-else>U písně je označení „anonymní autor“.</span>
    </v-card-text>

    <v-card-actions class="p-0">
      <!-- <v-flex shrink mr-1>
        <v-btn
          :disabled="model.has_anonymous_author"
          color="info"
          outline
          @click="addEmptyAuthor()"
        >Přidat autora</v-btn>
      </v-flex> -->
      <v-flex grow mb-3>
        <v-checkbox
          :disabled="model.authors_pivot.filter((el) => el.author != null).length > 0"
          class="mt-1"
          v-model="model.has_anonymous_author"
          label="Píseň má anonymního autora"
          :hide-details="true"
        ></v-checkbox>
      </v-flex>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  name: "AuthorPicker"
}
</script>

<style scoped>

</style>
