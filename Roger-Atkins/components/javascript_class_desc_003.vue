<template>
  <div>
    <div class='row'>
      <div class='col l8 m12 s12'>
        <p>
          <img src='../assets/code_ex_002_v001.jpg' class='responsive-img'>
        </p>
      </div>
      <div class='col l4 m12 s12'>
        <p>
          ok so this(above/left) we wish to add the carry_capacity property to trucks. And because we have our own constructor attached to this new
          class that is what will be executed to build the props of this object. If no constructor was present it would
          default back to the parent constructor above that we are extending from. But we need our own constructor because we are adding a special
          property specific to trucks, carry_capacity.
        </p>
        <p>
          The super call inside a constructor simply goes and fetches the parents constructor,
          and if it exists it runs that constructor to set up properties for the object from which it was called. It saves
          copy pasta all the parent classes properties.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'javascript_class_desc_003'
}
</script>

<style scoped>

</style>
