<template>
  <div class="container">
    <div>
      <h1 class="title">
        Sarcastic Text
      </h1>
      <Engine />
      <p class="note">Generate the upper and lower case sarcastic text popularized by the SpongeBob meme</p>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
body {
  background: #2b2044;
  color: #fff;
}

.container {
  margin: 0 auto;
  max-width: 46rem;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  margin: 1em 0;
  font-weight: 300;
  font-size: 32px;
  color: #ffc107;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

p.note {
  margin: 2rem 0;
  color: #c3b79b;
}
</style>
