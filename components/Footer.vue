<template>
  <div>
    <div class="foot">
      <b-row>
        <b-col>
          <div class="foot">
            <FooterContent />
          </div>
          <p class="copy">&copy; GideonKirimanjaro</p></b-col
        ></b-row
      >
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style>
.foot {
  display: flex;
  justify-content: center;
}
.copy {
  color: black;
  font-size: 20px;
  display: flex;
  justify-content: center;
}
.foot {
  background-color: yellow;
}
</style>
