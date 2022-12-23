<script>
    const title = "My App";
    const image = "https://www.freecodecamp.org/news/content/images/2021/06/w-qjCHPZbeXCQ-unsplash.jpg";

    let update = () => {
        requestAnimationFrame(update);
        // @ts-ignore
        this.style.backgroundPositionY = -scrollY * 0.5 + 'px';
    };

    let scrollY = 0;
    if (typeof window !== 'undefined') {
        window.addEventListener('scroll', () => {
            scrollY = window.scrollY;
        });
        update();
    }
</script>
<style>
    .parallax {
      height: 200vh;
      background-position: center;
      background-repeat: no-repeat;
      background-size: cover;
    }
  
    .content {
      height: 25%;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
    }
  
    h1 {
      color: white;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
    }
  </style>
  
  <section class="parallax relative bg-black" style="background-image: url({image});">
    <div class="content bg-slate-400">
      <h1>{title}</h1>
    </div>
  </section>
