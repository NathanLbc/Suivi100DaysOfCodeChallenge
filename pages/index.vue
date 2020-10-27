<template>
  <div class="container">
    <div class="title">Nathan's #100DaysOfCode</div>
    <p class="content">
      Here is the website in which I'll post any progress I do while doing the
      <a class="link" target="_blank" href="https://www.100daysofcode.com/">
        100 Days of Code Challenge
      </a>
    </p>
    <p>Main tools :</p>

    <img
      class="images"
      src="1200px-Unofficial_JavaScript_logo_2.svg.png"
      alt="JavaScript Logo"
      height="40px"
      width="50px"
    />
    <img
      class="images"
      src="nuxt-logo-5EF50E1ABD-seeklogo.com.png"
      alt="JavaScript Logo"
      height="40px"
      width="50px"
    />
    <img
      class="images logovue"
      src="Vue_js_logo.png"
      alt="JavaScript Logo"
      height="60px"
      width="80px"
    />
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
.logovue {
  margin-left: -25px;
}
.images {
  display: inline;
}
.p {
  margin-bottom: 10px;
}
.content {
  padding-top: 20px;
}
.link {
  color: black;
}
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: bolder;
  font-size: 70px;
  color: white;
  letter-spacing: 1px;
  text-align: center;
  padding-top: 2%;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
