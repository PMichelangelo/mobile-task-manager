<script>
  export let checked = false;
  export let label = "";
  export let separated = false;

  function toogle(event) {
    checked = checked == true ? false : true;
  }
</script>

<div class="wrapper">
  <div class="checkbox" class:checked on:click={toogle}>
    {#if checked}
      <span>✓</span>
    {/if}
  </div>
  <div class="content" class:separated>
    <div class="label" class:checked>
      {label}
    </div>
  </div>
</div>

<style>
  .wrapper {
    display: flex;
    align-items: center;

    color: #0b113c;
    font-weight: 500;
    margin: 0 46px;
  }

  .wrapper:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 40px rgba(85, 69, 69, 0.2);
    border-radius: 100px;
    transition: all 0.2s;
  }

  .wrapper:hover::after {
    transform: scaleX(1.4) scaleY(1.6);
    opacity: 0;
    animation: moveInBottom 5s ease-out;
    animation-fill-mode: backwards;
  }

  .content {
    display: flex;
    align-items: center;
    flex-grow: 1;
    height: 57px;
    margin-left: 20px;
  }

  .separated {
    border-bottom: 1px solid #e1e1e1;
  }
  .checkbox {
    display: flex;
    align-items: center;
    justify-content: center;
    min-width: 30px;
    max-width: 30px;
    height: 30px;
    border-radius: 100%;
    border: 2px solid #0b113c;
    color: #fff;
  }
  .checkbox.checked {
    background-color: #0b113c;
  }

  .label {
    align-items: center;
    justify-content: center;
  }

  .label.checked {
    text-decoration: line-through;
  }
</style>
