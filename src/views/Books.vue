<template>
  <div>
    <v-list shaped>
      <v-list-item v-for="book in books" :key="book.title">
        <v-list-item-avatar tile>
          <v-img :alt="`${book.title} avatar`" :src="book.img"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title v-text="book.title"></v-list-item-title>
          <v-list-item-subtitle v-text="book.author.name"></v-list-item-subtitle>
          <v-list-item-subtitle v-text="book.pages"></v-list-item-subtitle>
        </v-list-item-content>

        <v-list-item-icon>
          status
        </v-list-item-icon>
      </v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list subheader>
      <v-subheader>Previous chats</v-subheader>

      <v-list-item v-for="chat in previous" :key="chat.title">
        <v-list-item-avatar>
          <v-img :alt="`${chat.title} avatar`" :src="chat.avatar"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title v-text="chat.title"></v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </div>
</template>

<script>
import bookList from "@/data/books.json";

export default {
  data() {
    return {
      books: bookList,
    };
  },
};
</script>

<style lang="scss" scoped></style>
