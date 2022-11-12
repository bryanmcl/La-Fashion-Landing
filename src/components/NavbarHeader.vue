<template>
    <header>
        <a href="#" class="logo"><span>La</span>'Fashion</a>

        <ul>
            <li><a href="#about-us">About</a></li>
            <li><a href="#value-section">Value</a></li>
            <li><a href="">Contact</a></li>
        </ul>
    </header>
</template>


<script>


</script>


<style scoped>
    header {
        box-sizing: border-box;

        background-image: linear-gradient(to bottom, rgba(0,0,0,1), rgba(0,0,0,0.6), rgba(0,0,0,0));
        color: white;
        height: 4rem;

        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 2rem;
        position: fixed;
        width: 100%;
        height: 5rem;
        z-index: 10;
    }
      
    .logo {
      font-size: 2rem;
    }

    .logo span {
      background-color: white;
      color: black;
    }
    
    ul {
      display: flex;
      
      list-style: none;
      font-size: 1.5rem;
      gap: 4rem;
      height: 100%;
    }

    li {
      display: flex;
      align-items: center;

      position: relative;
      transition: all 0.2s ease;
      height: 100%;
      overflow: hidden;
    }
    
    li::before {
      content: "";
      position: absolute;
      bottom: 1rem;
      left: 0;
      background-color: white;
      width: 100%;
      height: 4px;
      
      z-index: -1;
      transform: translateX(-100%);
      transition: all 0.2s ease;
    }
    
    li:hover::before {
      transform: translateX(0);
    }

    a {
      color: white;
      text-decoration: none;
    }
</style>
