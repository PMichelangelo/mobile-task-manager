<script>
  let size = 22;
</script>

<div class="wrapper">
  <div class="background">
    <div class="home"><img src="img/house-solid.svg" alt="home" /></div>
    <p>Home</p>
    <div class="file"><img src="img/file-solid.svg" alt="" /></div>
    <div class="glass"><img src="img/magnifying-glass-solid.svg" alt="" /></div>
  </div>
  <button class="add-new">+</button>
</div>

<style>
  .wrapper {
    display: flex;
    align-items: center;
    height: 81px;
    color: #0b113c;
    font-weight: 500;
  }
  .background {
    display: flex;
    align-items: center;
    height: 81px;
    background-color: #f1f2f8;
    margin-left: 8px;
    border-radius: 31px;
  }

  img {
    width: 22px;
    height: 22px;
  }

  .home {
    padding-left: 38px;
  }

  .file {
    padding-left: 50px;
  }

  .glass {
    padding-left: 50px;
    padding-right: 35px;
  }

  p {
    padding-left: 20px;
    color: #0b113c;
  }

  button {
    background-color: #0b113c;
    color: #fff;
    height: 58px;
    width: 58px;
    border-radius: 21px;
    font-size: 28px;
    align-items: center;
  }
</style>
