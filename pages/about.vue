<template>
  <v-container class="my-10">
    <h1 class="text-h4 mb-4">About</h1>
    <p class="mb-4">
      Name = Panyakorn Saejao <br />
      Age = 20 <br />
      Department = Computer Technology
    </p>

    <!-- รูปภาพ -->
    <v-img
      src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRGOjLOkcFYKtC-xokP20IHL-9kakxqKSbFyw&s"
      width="50vw"
      height="50vh"
      class="mx-auto mb-6"
      alt="Computer Technology"
    ></v-img>

    <!-- ลิงก์ -->
    <v-btn
      color="red"
      href="https://cdn.readawrite.com/articles/10979/10978393/thumbnail/large.gif?1"
      target="_blank"
      rel="noopener"
    >
      ปุ่มอันตราย
    </v-btn>
  </v-container>
</template>

<script>
export default {
  name: 'AboutPage'
}
</script>
