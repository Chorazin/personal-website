<template>
  <div>
    <div class='row top_margin_100'>
      <div class='col l8 m12 s12'>
        <p>
          <img src='../assets/code_ex_003_v001.jpg' class='responsive-img' alt='example code'>
        </p>
      </div>
      <div class='col l4 m12 s12'>
        <p>
          Ok now lets wind the clock back and look at how javascript actually sets up objects under the hood with the prototype model
          and the __proto__ you will see greyed out in the console with the methods attached.

        </p>
        <p>
          Every object in Javascript has a prototype.
          And prototypes contain all the methods for that object type. Ok, so why? Well think of it like this, array methods
          would be stored multiple times for each array you create, users array, fruit array, vehicle array. Seems a bit clunky when you can just attach the array prototype to an array and store
          every method once on the prototype. Then attach that array prototype to every individual array.
        </p>
        <p>
          The __proto__ you see is merely
          a pointer to the relevant prototype, array prototype, date prototype, etc. This brings me to my next point, when using a constructor
          you can just create a method inside that constructor, but it attaches the method to each individual vehicle. Wouldn't it be better
          to create the method on the vehicle prototype that javascript has ready for us to go?
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
