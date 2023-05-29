<script>

export default {
  name: "AppMain",
};

</script>

<template>
  <main>

    <section id="heading_section" class="std_flex justify-content-center">
      <div id="heading_title" class="std_flex flex-column">
        <h1>Untold Stories</h1>
        <h2>There is an untold story behind every favorite song.</h2>
      </div>
    </section>

    <div style="width: 100%; height: 2000px; background-color: red"></div>

  </main>
  
</template>

<style scoped lang="scss">
@use "../assets/style/main.scss" as *;

main
    {
        #sticky_section
        {
            
            background-color: black;
            color: white;
            position: relative;
            
        }
        
        #heading_section
        {
            color: green;
            height: 100vh;
            #heading_title
            {

            }
        }
    }

</style>
